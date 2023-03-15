# Airflow code
This repo contains tips and code for Airflow

## For installing
- Download the yaml file and run:
``` 
docker compose up -d
```

## For testing a task
```
$ docker exec -it NAME_OF_AIRFLOW_SCHEDULER_CONTAINER /bin/bash
$ airflow tasks test DAG_ID TASK_ID
```

## For fetching a Postgres table
```
$ docker exec -it NAME_OF_POSTGRES_CONTAINER /bin/bash
$ psql -Uairflow
$ YOUR_QUERY
```

# To launch Flower
```
$ docker compose --profile flower up -d
```

# Check interactions with Elasticsearch
Once running `docker compose -f .\docker-compose-es.yaml up -d`
```
$ docker exec -it NAME_OF_AIRFLOW_SCHEDULER_CONTAINER /bin/bash
$ curl -X GET 'http://elastic:9200'
```