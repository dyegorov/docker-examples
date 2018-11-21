# docker-examples
# Mongo + express
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