# supinfo-4DOKR OR supinfo-3DOKR

## Launch backend api (simple_api)

```
docker build -t simple_api ./simple_api
docker run --name simple_api -d -p 5000:5000 simple_api
```

If the backend run it should throw an error on http://localhost:5000

Curl the endpoint to get data :

```
curl -u toto:python -X GET http://127.0.0.1:5000/pozos/api/v1.0/get_student_ages
```

### Remove whole created resources except image

```
docker container rm simple_api -f
docker volume prune
```

##

When you update the index.php url, don't miss the point that your localhost will not work. Docker have an intern localhost and you will need to pass the backend container name instead so it can be automatically recognized.

## Launch docker-compose.yml

```
docker compose up
docker compose down
```

## To get local registry

Just tag your image and push it
