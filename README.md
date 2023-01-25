# prefixed-superset

Adds context path (url prefix, sub path) of Apache Superset by NGINX reverse proxy and sub_filter.

# How to use

## Start a superset and nginx

with awesome(default) context path
```
$ docker-compose up -d 
```

or

with the context path `mysuperset`
```
$ SUPERSET_CONTEXT_PATH=mysuperset docker-compose up -d
```

## Load examples

```
$ docker exec -it prefixed_superset superset load_examples
```

## Accesss

### 1. Direct access (for testing)

http://localhost:8080

### 2. With context path

http://localhost/awesome/superset/welcome/ or http://localhost/${SUPERSET_CONTEXT_PATH}/superset/welcome/


## Stop the superset and nginx

```
$ docker-compose down
```

