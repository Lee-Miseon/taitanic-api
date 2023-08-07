# taitanic-api
taitanic ML service

# Alchitecture
![image](https://github.com/Lee-Miseon/taitanic-api/assets/128139621/dadaa303-9439-4eb1-aecf-ddb025b4a17c)

# DEV
### stack
- java 17
- gradle 8.2.1
- spring boot 3.1.2
- docker

### build
- gradle clean build

### test
- gradle test

### package
- gradle bootjar

### package & run
- gradle bootjar
- java -jar /build/libs/taitanic-api-0.0.1-SNAPSHOT.jar

# DEPLOY
- docker 
```
$ docker build -t taitanic-api:0.0.1 .
$ docker images taitanic-api
REPOSITORY      TAG      IMAGE ID       CREATED          SIZE
taitanic-api    0.0.1    9b27c25c0fc6   14 seconds ago   324MB

$ docker run -d --name taitanic-api-001 -p 9010:9876 taitanic-api:0.0.1

$ docker ps
CONTAINER ID   IMAGE                COMMAND                CREATED              STATUS              PORTS                                       NAMES
4bcffa7a01c3   taitanic-api:0.0.1   "java -jar /app.jar"   About a minute ago   Up About a minute   0.0.0.0:9010->9876/tcp, :::9010->9876/tcp   taitanic-api-001
```

### REFERENCE
- https://spring.io/guides/topicals/spring-boot-docker/