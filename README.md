# kafka-docker-setup

- clone this repository

- cd into the directory

- execute the following commands (Make sure docker is running)

```
docker compose up -d
```

- once kafa container is running use the following command to interact with kafka shell running inside the container

  ```
  docker exec -it -w /opt/kafka/bin broker sh
  ```

- To add topic in kafka

  ```
  ./kafka-topics.sh --create --topic sample-topic --bootstrap-server broker:29092
  ```

- To start a producer in kafka

  ```
  ./kafka-console-producer.sh --topic sample-topic --bootstrap-server broker:29092
  ```

- To start a consumer in kafka

  ```
  ./kafka-console-consumer.sh --topic sample-topic --from-beginning --bootstrap-server broker:29092
  ```
