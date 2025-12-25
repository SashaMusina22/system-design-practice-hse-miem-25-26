# Домашнее задание 3

1. Собрала образ согласно инструкции, только поменяла порты, потому что на маке они заняты какой-то системной службой

<img width="832" height="147" alt="image" src="https://github.com/user-attachments/assets/693bf41c-8788-418d-9c49-817191dc8d5e" />

Получившийся кластер состоит из двух реплик и одного лидера (patroni2)

2. UI HAproxy успешно открывается

<img width="1271" height="597" alt="image" src="https://github.com/user-attachments/assets/5e33d0c4-8a87-4bec-af8a-dfd97124b829" />

Видим что на фронтенд пока ничего не поступало, соответственно и в БД ничего не отдавалось

В primary у реплик статус down, а в replicas, соответственно, up

3. Загружаю данные в бд с помощью скрипта и запускаю traffic-generator.py

```bash
❯ python3 traffic-generator.py

--- STARTING LOAD GENERATOR ON PORT 5500 ---

[23:56:21] CONNECTED to Master Node
[23:56:21] INSERT: purchase by Иван Петров
READ check (Last 3 IDs): [3, 2, 1]
[23:56:22] INSERT: login by Иван Петров
[23:56:23] INSERT: click by Мария Сидорова
READ check (Last 3 IDs): [5, 4, 3]
[23:56:24] INSERT: click by Мария Сидорова
[23:56:25] INSERT: click by Алексей Козлов
READ check (Last 3 IDs): [7, 6, 5]
```

Выключаю лидера, запись прерывается с ошибкой, но позже кластер восстанавливается, т.к происхоидт переизбрание лидера

```bash

[23:57:42] CONNECTION LOST (Failover in progress?): server closed the connection unexpectedly
        This probably means the server terminated abnormally
        before or while processing the request.

[23:57:55] Connection failed: connection to server at "localhost" (::1), port 5500 failed: server closed the connection unexpectedly
        This probably means the server terminated abnormally
        before or while processing the request.

[23:58:49] CONNECTED to Master Node
[23:58:49] INSERT: click by Алексей Козлов
READ check (Last 3 IDs): [91, 82, 81]
[23:58:50] INSERT: purchase by Алексей Козлов
[23:58:51] INSERT: click by Иван Петров
READ check (Last 3 IDs): [93, 92, 91]
[23:58:52] INSERT: login by Алексей Козлов
[23:58:53] INSERT: view_page by Мария Сидорова
READ check (Last 3 IDs): [95, 94, 93]
[23:58:54] INSERT: logout by Мария Сидорова
[23:58:55] INSERT: click by Мария Сидорова

```

Лидером становится patroni3
<img width="1265" height="565" alt="image" src="https://github.com/user-attachments/assets/974c941a-fa6d-4c8c-93ae-be5808f90512" />

Отключаю нового лидера

```bash
[00:00:05] CONNECTION LOST (Failover in progress?): server closed the connection unexpectedly
        This probably means the server terminated abnormally
        before or while processing the request.

[00:00:18] Connection failed: connection to server at "localhost" (::1), port 5500 failed: server closed the connection unexpectedly
        This probably means the server terminated abnormally
        before or while processing the request.
```

Лидер снова переизбирается и даже с одной нодой запись продолжается

```bash
[00:01:50] INSERT: error by Мария Сидорова
READ check (Last 3 IDs): [248, 247, 246]
[00:01:51] INSERT: login by Иван Петров
[00:01:52] INSERT: logout by Мария Сидорова
READ check (Last 3 IDs): [250, 249, 248]
[00:01:53] INSERT: login by Мария Сидорова
[00:01:54] INSERT: view_page by Мария Сидорова
READ check (Last 3 IDs): [252, 251, 250]
[00:01:55] INSERT: purchase by Алексей Козлов
[00:01:56] INSERT: login by Алексей Козлов
READ check (Last 3 IDs): [254, 253, 252]
[00:01:57] INSERT: click by Алексей Козлов
[00:01:58] INSERT: click by Мария Сидорова
READ check (Last 3 IDs): [256, 255, 254]
[00:01:59] INSERT: click by Иван Петров
[00:02:00] INSERT: error by Алексей Козлов
READ check (Last 3 IDs): [258, 257, 256]
[00:02:01] INSERT: login by Алексей Козлов
[00:02:02] INSERT: error by Алексей Козлов
READ check (Last 3 IDs): [260, 259, 258]
[00:02:03] INSERT: error by Мария Сидорова
```

<img width="1259" height="539" alt="image" src="https://github.com/user-attachments/assets/4f433c36-e4a1-4a73-8925-b39343b30714" />

Включаю еще одну ноду patroni, она становится репликой. Если ее отключить, запись не прерывается, т.к primary узел живой

<img width="1264" height="558" alt="image" src="https://github.com/user-attachments/assets/a1ebbe38-a3cd-4dbb-bbc8-2525a4c4a8db" />

```bash
[00:03:18] INSERT: purchase by Мария Сидорова
[00:03:19] INSERT: purchase by Мария Сидорова
READ check (Last 3 IDs): [336, 335, 334]
[00:03:20] INSERT: view_page by Иван Петров
[00:03:21] INSERT: purchase by Иван Петров
READ check (Last 3 IDs): [338, 337, 336]
[00:03:22] INSERT: view_page by Алексей Козлов
[00:03:23] INSERT: logout by Иван Петров
READ check (Last 3 IDs): [340, 339, 338]
[00:03:24] INSERT: logout by Мария Сидорова
[00:03:25] INSERT: logout by Иван Петров
READ check (Last 3 IDs): [342, 341, 340]
[00:03:26] INSERT: logout by Алексей Козлов
[00:03:27] INSERT: login by Иван Петров
READ check (Last 3 IDs): [344, 343, 342]
[00:03:28] INSERT: logout by Мария Сидорова
[00:03:29] INSERT: click by Алексей Козлов
READ check (Last 3 IDs): [346, 345, 344]
```

Теперь etcd: отключаю один контейнери ничего не происходит

```bash
[00:04:11] INSERT: logout by Иван Петров
[00:04:12] INSERT: purchase by Алексей Козлов
READ check (Last 3 IDs): [388, 387, 386]
[00:04:13] INSERT: purchase by Мария Сидорова
[00:04:14] INSERT: click by Мария Сидорова
READ check (Last 3 IDs): [390, 389, 388]
[00:04:15] INSERT: view_page by Мария Сидорова
[00:04:16] INSERT: view_page by Иван Петров
READ check (Last 3 IDs): [392, 391, 390]
[00:04:17] INSERT: logout by Мария Сидорова
[00:04:18] INSERT: purchase by Мария Сидорова
READ check (Last 3 IDs): [394, 393, 392]
[00:04:19] INSERT: click by Иван Петров
[00:04:20] INSERT: view_page by Иван Петров
READ check (Last 3 IDs): [396, 395, 394]
[00:04:21] INSERT: click by Мария Сидорова
[00:04:22] INSERT: view_page by Алексей Козлов
READ check (Last 3 IDs): [398, 397, 396]
[00:04:23] INSERT: click by Иван Петров
```

Отключаю вторую и кластер переходит в read-only

```bash

[00:04:51] CONNECTION LOST (Failover in progress?): server closed the connection unexpectedly
        This probably means the server terminated abnormally
        before or while processing the request.

[00:04:52] Connection failed: connection to server at "localhost" (::1), port 5500 failed: session is read-only
```

Отключение третьей приведет к полной смерти кластера

Если отключить ноду с HAProxy, то обратиться к кластеру невозможно, потому что эта нода является входной точкой любого запроса

<img width="942" height="341" alt="image" src="https://github.com/user-attachments/assets/959dbeb0-6ee2-4d0f-a551-0c37b91d9198" />

```bash


[00:06:50] Connection failed: connection to server at "localhost" (::1), port 5500 failed: Connection refused
        Is the server running on that host and accepting TCP/IP connections?
connection to server at "localhost" (127.0.0.1), port 5500 failed: Connection refused
        Is the server running on that host and accepting TCP/IP connections?

[00:06:51] Connection failed: connection to server at "localhost" (::1), port 5500 failed: Connection refused
        Is the server running on that host and accepting TCP/IP connections?
connection to server at "localhost" (127.0.0.1), port 5500 failed: Connection refused
        Is the server running on that host and accepting TCP/IP connections?

[00:06:53] Connection failed: connection to server at "localhost" (::1), port 5500 failed: Connection refused
        Is the server running on that host and accepting TCP/IP connections?
connection to server at "localhost" (127.0.0.1), port 5500 failed: Connection refused
        Is the server running on that host and accepting TCP/IP connections?
```
