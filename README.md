# docker-examples
# Mongo + express
IMPORTANT: Express should be used for development only
## Start
```
$ docker stack deploy -c mongo-express.yml mongo
```
## Info
```
$ docker service ls
```
## View logs
```
$ docker service logs mongo_mongo
```
## Stop
```
$ docker stack rm mongo
```
## Cleanup
```
$ docker rm -f $(docker ps -aq)
$ sudo docker rm -f $(sudo docker ps -aq)
$ docker volume prune
```
## View web admin
http://192.168.89.139:8081/

## Shell login to db
$ mongo -u root -p example --authenticationDatabase admin

# Node simple example
[node on docker hub](https://hub.docker.com/_/node/)
[docker node best practices](https://github.com/nodejs/docker-node/blob/master/docs/BestPractices.md)
## Start node express server
```
$ node index
```
## Check via curl
```
$ curl -XGET -H 'Content-type: application/json' http://localhost:4000
Hello world
```
or via included script
```
$ . getIndex.sh
Hello world
```
## Build image
```
$ sudo docker build -t mynode .
```
## View built image
```
$ sudo docker image ls
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
mynode              latest              3fe0ad65a7a2        3 minutes ago       894MB
```