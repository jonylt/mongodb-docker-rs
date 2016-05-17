# mongodb-docker-rs
docker compose yml to setup a mongodb replicaset

#### Prerequisites ####
* docker
* docker-compose
* mongodb (client, no need to be running locally mongodb)

#### Use ####
* Update "volumes" with your local db data directories
* Run docker-compose up
* Connect to mongo primary instance (probably will be mongo1) 
```
mongo mongo1:27017

> rs.initiate()
> rs.add("mongo2:27017")
> rs.add("mongo3:27017")
```
