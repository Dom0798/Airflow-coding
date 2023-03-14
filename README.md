# Airflow code
This repo contains tips and code for Airflow

## For installing

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