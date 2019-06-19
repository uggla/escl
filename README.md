#  Cluster with three Elasticsearch nodes

This example brings up a cluster comprising three Elasticsearch nodes, using three docker-compose for each node.


### Prerequisites

1.	Docker-Compose.version = v1.24.0
2.	Docker for Linux.version = v18.09.6
3.	Elasticsearch.version = v6.4.1
4.	The following ports must be free on the host: 9200,9300



### Instructions
*	Set the vm.max_map_count kernel to at least 262144
```
sysctl -w vm.max_map_count=262144
```

*	Ensuring the network publish host is configured in docker-compose for each node
```
network.publish_host=es1.uggla.fr
```

*	Starts the containers
```
docker-compose up
```

*	Inspect status of cluster
```
curl http://127.0.0.1:9200/_cat/health
```


### Links for help

For more information, see the two following links:
https://www.elastic.co/guide/en/elasticsearch/reference/6.4/docker.html

https://www.elastic.co/guide/en/elasticsearch/reference/6.4/modules-network.html#common-network-settings
