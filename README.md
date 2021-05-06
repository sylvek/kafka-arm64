# KAFKA for Apple M1

This hack is an horrible thing allowing to run Kafka 0.10 on my Apple M1.

I used spotify/kafka code and modified the Dockerfile to be compatible with ARM64. (https://docs.ligato.io/en/latest/user-guide/arm64/)

```
> docker build -t kafka-arm64
> docker run -p 2181:2181 -p 9092:9092 --name kafka --rm \
 --env ADVERTISED_HOST=<your ip> --env ADVERTISED_PORT=9092 kafka-arm64
```
