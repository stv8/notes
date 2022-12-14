

## Stop All Docker Containers


```shell
docker kill $(docker ps -q)
```

  
The `docker ps` command will list all _running_ containers. The `-q` flag will only list the IDs for those containers. Once we have the list of all container IDs, we can simply run the `docker kill` command, passing all those IDs, and they’ll all be stopped!

  

## Remove All Docker Containers
  

```shell
docker rm $(docker ps -a -q)
```

We already know that `docker ps -q` will list all running container IDs. What is the `-a` flag? Well that will return _all_ containers, not just the running ones. Therefore, this comman will remove all containers (including both running and stopped containers).

  
## Remove All Docker Images

```shell
docker rmi $(docker images -q)
```

  
`docker images -q` will list all image IDs. We pass these IDs to `docker rmi` (which stands for remove images) and we therefore remove all the images.