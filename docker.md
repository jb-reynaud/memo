# Docker

## Configuration

- Get Docker Community Edition ([link](https://www.docker.com/get-docker)).
- Set folder of our project in `Docker > Preferences > File Sharing`.

## Add docker to a symfony project

If it's not already installed, follow https://phpdocker.io/ 

#### Usefull links
http://blog.joeymasip.com/docker-for-symfony-4/

## Cheats sheet

```bash
# Start docker
docker-compose up -d

# To clear containers/images/volumes
docker rm -f $(docker ps -a -q)
docker rmi -f $(docker images -a -q)
docker volume rm $(docker volume ls -q)
```

## How to

#### Access mysql in workbench?
params|values
---|---
url|127.0.0.1
port|8002
user|root
password|MYSQL_ROOT_PASSWORD in `docker-compose.yml`

## Notes

- [03/04/18] Mysql 8 did not seems to work properly (could not connect, plugin needed), I went back to 5.7.
