# ДЗ 2

1. Собираю образ с помощью docker compose up -d, предварительно актуализировала образы в Dockerfile и docker-compose.yaml

```bash
WARN[0000] /Users/aleksandramusina/Documents/system-design-practice-hse-miem-25-26/hw2/kafka-kraft-cluster/docker-compose.yaml: the attribute `version` is obsolete, it will be ignored, please remove it to avoid potential confusion 
[+] Running 5/10
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s                                                        0.0s 
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s                                                        0.0s 
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s                                                        0.1s 
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s                                                        0.1s 
 ⠹ Container kafka-kouncil                                                                                          [+] Running 5/10                            Starting0.2s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s  
 ⠸ Container kafka-kouncil                                                                                          [+] Running 5/10                            Starting0.3s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s  
 ⠼ Container kafka-kouncil                                                                                          [+] Running 5/10                            Starting0.4s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s  
 ⠴ Container kafka-kouncil                                                                                          [+] Running 5/10                            Starting0.5s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s  
 ⠦ Container kafka-kouncil                                                                                          [+] Running 5/10                            Starting0.6s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s  
 ⠧ Container kafka-kouncil                                                                                          [+] Running 5/10                            Starting0.7s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s  
 ⠇ Container kafka-kouncil                                                                                          [+] Running 5/10                            Starting0.8s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s  
 ⠏ Container kafka-kouncil                                                                                          [+] Running 5/10                            Starting0.9s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s  
 ⠋ Container kafka-kouncil                                                                                          [+] Running 5/10                            Starting1.0s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s  
 ⠙ Container kafka-kouncil                                                                                          [+] Running 5/10                            Starting1.1s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s  
 ⠹ Container kafka-kouncil                                                                                          [+] Running 5/10                            Starting1.2s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s  
 ⠸ Container kafka-kouncil                                                                                          [+] Running 5/10                            Starting1.3s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s  
 ⠼ Container kafka-kouncil                                                                                          [+] Running 5/10                            Starting1.4s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s  
 ⠴ Container kafka-kouncil                                                                                          [+] Running 5/10                            Starting1.5s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s  
 ⠦ Container kafka-kouncil                                                                                          [+] Running 5/10                            Starting1.6s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s  
 ⠧ Container kafka-kouncil                                                                                          [+] Running 5/10                            Starting1.7s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s  
 ⠇ Container kafka-kouncil                                                                                          [+] Running 5/10                            Starting1.8s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s  
 ⠏ Container kafka-kouncil                                                                                          [+] Running 5/10                            Starting1.9s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s  
 ⠋ Container kafka-kouncil                                                                                          [+] Running 9/10                            Starting2.0s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s  
 ✔ Container kafka-kouncil                                                                                          [+] Running 10/10                           Started2.1s 
 ✔ Network kafka-kraft-cluster_default                                                                                                                          Created0.0s  
 ✔ Volume kafka-kraft-cluster_data_kafka_01                                                                                                                     Created0.0s 
 ✔ Volume kafka-kraft-cluster_data_kafka_02                                                                                                                     Created0.0s 
 ✔ Volume kafka-kraft-cluster_data_kafka_03                                                                                                                     Created0.0s 
 ✔ Container kafka-kouncil                                                                                                                                      Started2.1s 
 ✔ Container my-kafka-ui                                                                                                                                        Started2.1s 
 ✔ Container kafka01                                                                                                                                            Started2.1s 
 ✔ Container kafka03                                                                                                                                            Started2.1s 
 ✔ Container kafka02                                                                                                                                            Started2.1s 
 ! kafka-kouncil The requested image's platform (linux/amd64) does not match the detected host platform (linux/arm64/v8) and no specific platform was requested 0.0s                                                             
 ```

2. UI успешно открывается

<img width="1256" height="388" alt="image" src="https://github.com/user-attachments/assets/74cb6034-f3fb-424d-ac6f-9f48c88d9172" />

3. Создаю test_topic

```bash
docker run -it --rm --network kafka-kraft-cluster_default confluentinc/cp-kafka:latest kafka-topics \
--create \
--topic test_topic \
--bootstrap-server kafka01:9092,kafka02:9092,kafka03:9092 \
--partitions 8 \
--replication-factor 3 \
--if-not-exists
```
<img width="1259" height="307" alt="image" src="https://github.com/user-attachments/assets/366481ff-16d6-4e88-ae8b-60beab7d7adf" />

4. Начинаю нагрузочное тестирование

```bash
docker run -it --rm --network kafka-kraft-cluster_default confluentinc/cp-kafka /bin/kafka-producer-perf-test \
--topic test_topic \
--num-records 1000000 \
--throughput -1 \
--producer-props bootstrap.servers=kafka01:9092,kafka02:9092,kafka03:9092 batch.size=16384 acks=1 linger.ms=50 \
--record-size 1000
```

Результат

```bash
505154 records sent, 101030.8 records/sec (96.35 MB/sec), 287.7 ms avg latency, 565.0 ms max latency.
1000000 records sent, 128534.7 records/sec (122.58 MB/sec), 178.93 ms avg latency, 600.00 ms max latency, 197 ms 50th, 434 ms 95th, 500 ms 99th, 581 ms 99.9th.
```

99.9 перцентиль по latency составляет 581 мс, а rps 128534

5. Запуск example.py и отключение контроллера

Запускаю скрипт, ищу брокера, который является контроллером. В моем случае это второй

<img width="1062" height="471" alt="image" src="https://github.com/user-attachments/assets/bbcf6188-2a9c-4c85-b5c0-846bc7937ee4" />

Отключаю контейнер с этим брокером. На несколько секунд кластер умирает, но отправка быстро возобновляется

```bash
Sent: 129
Sent: 130
Sent: 131
Sent: 132
Sent: 133
Sent: 134
Sent: 135
Error sending 136: KafkaTimeoutError: Timeout after waiting for 2 secs.
Sent: 136
Sent: 137
Sent: 138
Sent: 139
Sent: 140
Error sending 141: KafkaTimeoutError: Timeout after waiting for 2 secs.
Sent: 141
Sent: 142
Error sending 143: KafkaTimeoutError: Timeout after waiting for 2 secs.
Error sending 143: KafkaTimeoutError: Timeout after waiting for 2 secs.
Sent: 143
Sent: 144
Sent: 145
Sent: 146
Sent: 147
Sent: 148
Sent: 149
Sent: 150
Sent: 151
Sent: 152
Sent: 153
Sent: 154
Sent: 155
Sent: 156
Sent: 157
Sent: 158
Sent: 159
```
Третий брокер становится лидером

<img width="1260" height="486" alt="image" src="https://github.com/user-attachments/assets/1d1d1ef5-9704-4f74-9a7a-916d4e070a8d" />

В UI появляются красные показатели, это из-за того, что replication_factor был выставлен в значение три, но из-за отсутствия одного из трех брокеров невозможно в полной мере производить репликацию

6. Отключение 2 из 3 нод

Теперь отключаю контейнер с новым лидером

```bash
Sent: 465
Sent: 466
Sent: 467
Sent: 468
Sent: 469
Sent: 470
Error sending 471: KafkaTimeoutError: Timeout after waiting for 2 secs.
Sent: 471
Error sending 472: KafkaTimeoutError: Timeout after waiting for 2 secs.
Error sending 472: KafkaTimeoutError: Timeout after waiting for 2 secs.
Error sending 472: KafkaTimeoutError: Timeout after waiting for 2 secs.
```
Кластер погибает, а последний контейнер в логах показывает кучу ошибок соединения. Из-за того, что два из трех брокеров умерли, кворум потерян и кластер недоступен

<img width="1382" height="832" alt="image" src="https://github.com/user-attachments/assets/2098b9ca-2f2b-4d7d-957c-5eccc0abe565" />

7. Восстановление

По одному включаю контейнеры. Достаточно было вернуть 2 из 3, как сообщения стали долетать

```bash
Sent: 528
Sent: 529
Sent: 530
Sent: 531
Sent: 532
Sent: 533
Sent: 534
```

После оживления 3 из 3 нод произошла синхронизация и теперь ISR 48 из 48

<img width="1257" height="528" alt="image" src="https://github.com/user-attachments/assets/c4fe02a3-fa4a-4f64-8908-41bdea65cd39" />
