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

2. 