# Kafka Connect to Spring Boot Using Docker
## Setup
1. `git pull`
2. Install Docker-desktop for Mac and start it with `docker-compose up -d`
3. Have a JAVA IDE (IntelliJ) and open the repository in this.
4. `./mvnw spring-boot:run` to Run it - automatically builds and installs dependencies
6. Yup, you done it!

## Create kafka Topics
1. Enter the docker containter after running it - `docker exec -it <kafka-container-name> bash` , use `docker ps` to list the running containers.
2. Inside the container, to create topic with name `my-topic`, `kafka-topics --create --topic my-topic --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1`
3. Now you have created your topic.

## Sending Messages
1. Open the container terminal...
2. To produce your topic `kafka-console-producer --topic my-topic --bootstrap-server localhost:9092`
3. Now you can write anything in the terminal and it shall appear on the terminal where you have run Spring boot!
4. TO close,  `Ctrl + C`

## Afterwards
1. Dont forget to close your docker `docker-compose down`
