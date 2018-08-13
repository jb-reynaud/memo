# Docker

## Common
```bash
# List all containers.
docker ps -a

# Start/stop a container.
docker start [container_id]
docker stop [container_id]

# Remove all containers.
docker rmi $(docker images -q) -f
```
## How to...

### Start a mysql container
```bash
# Start mysql 5.7.
docker run -p 3306:3306 --name mysql01 -e MYSQL_ROOT_PASSWORD=root -d mysql:5.7

# See logs.
docker logs mysql01
```
