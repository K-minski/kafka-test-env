# Kafka Quick Test Enviroment Setup

### Description 
Main purpose for this repository is to set up quickly Kafka Zookeeper, Broker, SchamaRegistry for local proof of principle tests. 
Additionally, kafka-ui is included for easier tinkering

### How to Run
Simply use belwo command in project folder:
```
docker compose up
```

### Helpful commands
##### Initialize Setup:
```
docker compose -f docker-compose.yaml up
```
##### Destroy(Delete) initialized Setup:
```
docker compose -f docker-compose.yaml down
```
##### Start initialiezed Setup (Only if terminated earlier):
```
docker compose -f docker-compose.yaml start
```
##### Terminate and stop initialiezed Setup:
```
docker compose -f docker-compose.yaml stop
```
##### Enter container’s (<containers name>) internal CLI:
```
docker exec -it $(docker ps | grep <container name> | cut -d" " -f 1) /bin/sh
```


### Open default endpoints

| Service         | Container name  | Endpoint & Port |
|-----------------|-----------------|-----------------|
| Kafka Broker    | broker0         | localhost:9092  |
| Schema-Registry | schemaregistry  | localhost:8085  |
| Kafka-UI        | kafka-ui        | localhost:8081  |


