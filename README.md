# prefixed-superset

Change the root context path to your own.

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
$ docker exec -it prefixed-superset superset load_examples
```

## Accesss

### 1. Direct access (for testing)

http://localhost:8080

### 2. With context path

http://localhost/awesome or http://localhost/${SUPERSET_CONTEXT_PATH}


## Stop the superset and nginx

```
$ docker-compose down
```

