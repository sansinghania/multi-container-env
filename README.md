# multi-container-env
creates a containerised enviorment with collection of containers serving different aspects of software

Intention of this project is to do a PoC and create a containerised environment with three containers that communicate with each other on the defualt network. 
- Service container - running elastic search service
- Tools container - running observability tools like Kibana
- Application container - running application code in python

Each of these containers are self contained. The source code and application data sits on the host system and is mounted on to the containers.

Kibana UI: Open http://localhost:5601
ElasticSearch: http://localhost:9200


Cammands on the host machine
------------------------------------
```
//Build and boot up the containers in detached mode.

docker-compose up -d
```

```
//stoppig and removing all the containers

docker-compose down
```

```
//attaching terminal to the running container

docker exec -it <appserver-py> /bin/sh
```