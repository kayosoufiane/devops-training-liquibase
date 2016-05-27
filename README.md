# DevOps Training - Liquibase - Practical - using Docker compose

[![Build Status](https://travis-ci.org/ykandrirody/devops-training-liquibase.svg?branch=master)](https://travis-ci.org/ykandrirody/devops-training-liquibase)

## Usage

###  1 - Start all services

```
cd devops-training-liquibase

docker-compose up -d
```

###  2 - Test phpmyadmin :
http://localhost:8081/
http://localhost:8082/

### 3 - Run Liquibase
```
docker exec -it myliqui.global bash -c 'cd $BUILDENV; exec "/app/run_init_1.sh"'
docker exec -it myliqui.global bash -c 'cd $BUILDENV; exec "/app/run_init_2.sh"'
docker exec -it myliqui.global bash -c 'cd $BUILDENV; exec "/app/run_all_1.sh"'
docker exec -it myliqui.global bash -c 'cd $BUILDENV; exec "/app/run_all_2.sh"'
```


### 4 - Deallocate resources
```
docker-compose kill
docker-compose rm
```

