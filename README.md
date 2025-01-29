# docker-shortcuts
This is a repository for Docker shortcuts , so no magic

---
<br />

### Remove all Docker containers
```bash
docker rm -f $(docker ps -aq)
```

### Remove all Docker images
```bash
docker rmi -f $(docker images -q)
```

### Remove all Docker volumes
```bash
docker volume rm $(docker volume ls -q)
```

### Remove all unused Docker networks
```bash
docker network prune -f
```

### Clean up unused Docker system data
```bash
docker system prune -a --volumes -f
```

### Full Clean Up to remove everything
> [!CAUTION]
>  Before using, make sure u really want to remove everything
```bash
docker rm -f $(docker ps -a -q) && docker rmi -f $(docker images -q) && docker volume rm $(docker volume ls -q) && docker network prune -f
```
