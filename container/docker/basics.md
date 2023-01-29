## Docker

- Show running containers
```bash
docker ps
```

- Show all containers
```bash
docker ps -a
```

- Show images
```bash
docker images
```

- Create a container
```bash
docker create image-name
```

- Start a container
```bash
docker start container-id
```

- Start a container with output
```bash
docker start -a container-id
```

- Create and start a container
```bash
docker run image-name command
```

- Get logs of running container
```bash
docker logs container-id
```

- Execute command in running container in interactive mode
```bash
docker exec -it container-id command
```

- Stop a running container
```bash
docker stop container-id
```
- Kill a running container
```bash
docker kill container-id
```

- Remove containers, images, network, build cache
```bash
docker system prune
```
