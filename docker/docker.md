
# Docker commands and discripation


This is a brief description of what your Docker.

## to buld the image

```
docker build -t <imagename> .
```

## to see all running images

```
docker images 
```

## to runn the images
```
docker run -d -p <sys pot>:<conterpot> <conter name>
```

## to runn the images
```
docker run -it  <conter name>  /bin/bash
```

### example
```
docker run -d -p 5000:5000 helloapp
```

## to check running container 
```
docker ps
```
## to check all container 
```
docker ps -a
```

## to stop immage
```
docker stop  <immagr id>
```
# to logine 
```
docker login
```

# to push docker hub
```
docker tag <image name> <user name>/<repo name>
```

# to pull the immage
```
docker push <user name>/<repo name>
```