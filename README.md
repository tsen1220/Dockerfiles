# Dockerfiles

Contains docker command.

[Create](#Create)

[List](#List)

[AwakeSleep](#AwakeSleep)

[Remove](#Remove)

## Create

### Create Images

Docker container requires images to run.

Therefore, We need to build docker image from Dockerfile.

```
docker build -t <image_name>:tag .
```

For example: 

```
docker build -t  example:1.0 .
```

To decrease size, we create dockerignore file to ignore unnecessary files.

Hint: -t means --tag.

### Run Docker Container With Docker Image In Background

After creating docker image, we can create docker container to start server.

```
docker run -p <device_port>:<container_port> -d <image_name>:tag
```

## List

### Image List

We can get images.

```
docker images
```

### Container List 

We can get running containers list.

```
docker ps 
```

All containers list.

```
docker ps -a 
```

## AwakeSleep

We can do these with container id.

Start container.

```
docker start <container_id>
```

Stop container.

```
docker stop <container_id>
```

Restart container.

```
docker restart <container_id>
```

Force to stop container.

```
docker kill <container_id>
```

Stop all container.

```
docker stop $(docker ps -a -q) 
```

## Remove

### Remove Container
We can remove stopping container.

```
docker rm <container_id>
```

Remove all stopping container.

```
docker rm $(docker ps -a -q)
```

### Remove Images

Remove useless image.

```
docker rmi <image_id>
```

Remove all useless images.

```
docker rmi $(docker images -a -q)
```
