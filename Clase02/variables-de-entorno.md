# Variables de entorno

### Para crear variables de entorno

```
docker run -d --name servernginx03 -p 9200:80 -e name=sergio -e lastname=hidalgo nginx
docker run -d --name servermysql -p 5000:3306 -e MYSQL_ROOT_PASSWORD=12345 mysql:8

//No funciono con el volumen tipo host
docker run -d --name servermysql -p 5000:3306 -e MYSQL_ROOT_PASSWORD=12345 -v $(pwd)/Clase02/mysql:/var/lib/msyql mysql:8
```

```
docker volume create vol_mysql_docker
docker run -d --name servermysql -p 5000:3306 -e MYSQL_ROOT_PASSWORD=12345 -v vol_mysql_docker:/var/lib/msyql mysql:8
```