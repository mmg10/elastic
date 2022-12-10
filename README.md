# elastic


## Installation

Intended for testing purposes only; has security disabled.

```bash
docker pull docker.elastic.co/elasticsearch/elasticsearch:7.9.2
docker pull docker.elastic.co/kibana/kibana:7.9.2
```


Inside `setup` folder, run
```bash
docker-compose up
```

(Note: you might need to change the systemwide parameter via `sudo sysctl -w vm.max_map_count=262144` or remove the ulimits parameters)

To test Elasticsearch, execute
```bash
curl http://localhost:9200
```


To add node to this cluster, inside the `setup/second` folder, run
```bash
docker-compose up
```


To test kibana, simply open the url [http://localhost:5601](http://localhost:5601).
