## Description
Jaeger tracing system with non clustered elasticsearch as a storage backend with nginx as a reverse proxy.

## Prerequisites
- Docker swarm cluster 

## Installation
Add label to node, where will be deployed elasticsearch
```
docker node update --label-add elasticsearch=test $NODE_NAME
```

Next step will be deploy to cluster
```
docker stack deploy -c docker-compose.yaml $STACK_NAME
```

Then Jaeger UI should be available via http://node_ip_address