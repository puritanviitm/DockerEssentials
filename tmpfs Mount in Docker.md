### Create a container with tmpfs mount

```
docker run -d -it --name tmpmount --mount type=tmpfs,destination=/app nginx:latest
```
```
docker container inspect tmpmount
```
