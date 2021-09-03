# Apache Superset

## How to run

```shell
docker-compose up -d
```

If its the first execution:
```shell
docker exec -it superset superset fab create-admin \
               --username admin \
               --firstname Superset \
               --lastname Admin \
               --email admin@superset.com \
               --password admin
```
then
```shell
docker exec -it superset superset db upgrade
docker exec -it superset superset init
```

### Load Examples

```shell
docker exec -it superset superset load_examples
```
