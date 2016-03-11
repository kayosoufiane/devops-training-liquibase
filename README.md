# DevOps Training - Liquibase - Practical - using Docker compose

[![Build Status](https://travis-ci.org/ykandrirody/devops-training-liquibase.svg?branch=master)](https://travis-ci.org/ykandrirody/devops-training-liquibase)

## Usage

### Start all services

```
cd devops-training-liquibase

docker-compose up -d
```

### Test phpmyadmin :
http://localhost:8081/
http://localhost:8082/

### Run Liquibase
```
docker exec -it myliqui.global bash -c 'cd $BUILDENV; exec "/app/run_init_1.sh"'
docker exec -it myliqui.global bash -c 'cd $BUILDENV; exec "/app/run_init_2.sh"'
docker exec -it myliqui.global bash -c 'cd $BUILDENV; exec "/app/run_all_1.sh"'
docker exec -it myliqui.global bash -c 'cd $BUILDENV; exec "/app/run_all_2.sh"'
```


### Deallocate resources
```
docker-compose kill
docker-compose rm
```
