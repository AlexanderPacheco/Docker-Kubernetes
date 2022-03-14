# Volúmenes

### Para crear un volúmen tipo host

```
docker run -d --name servernginx03 -p 8888:80 -v D:\\Cursos\\Docker_Kubernetes_Group05\\Clase02\\html:/usr/share/nginx/html nginx
docker run -d --name servernginx03 -p 4000:80 -v /home/alexander/Documentos/Docker_Kubernetes_Group05/Clase02/html:/usr/share/nginx/html nginx
docker run -d --name test01 -p 5000:80 -v /home/alexander/Documentos/Docker_Kubernetes_Group05/Clase02/html01:/usr/share/nginx/html nginx
```

### Para crear un volúmen tipo host (en terminales tipo linux)

```
docker run -d --name servernginx03 -p 8888:80 -v $(pwd)\\html\:/usr/share/nginx/html nginx
docker run -d --name test01 -p 5000:80 -v $(pwd)/Clase02/html01:/usr/share/nginx/html nginx
```

### Para crear un volúmen tipo host (powershell)

```
docker run -d --name servernginx03 -p 8888:80 -v ${PWD}\html:/usr/share/nginx/html nginx
```

### Para crear un volúmen tipo host (cmd)

```
docker run -d --name servernginx03 -p 8888:80 -v %cd%\html:/usr/share/nginx/html nginx
```

### Para crear un volúmen tipo anónimo

```
//Se omite la parte del host y se crea en la carpeta de docker
docker run -d --name servernginx03 -p 8888:80 -v /usr/share/nginx/html nginx
```

### Para eliminar un contenedor y su volumen anónimo

```
//Solo funciona para volumenes anonimos
docker rm -fv servernginx03
//Ruta en windows
//\\wsl$\docker-desktop-data\version-pack-data\community\docker\containers
```

### Para crear un volumen nombrado

```
docker volume create vol_nginx
```

### Para listar los volúmenes

```
docker volume ls
```

### Para listar los volúmenes

```
docker volume inspect vol_nginx
```

### Para vincular un volumen nombrado a un contenedor

```
docker run -d --name servernginx03 -p 8888:80 -v vol_nginx:/usr/share/nginx/html nginx
```

### Para listar volúmenes huérfanos

```
docker volume ls -f dangling=true
```

### Para listar volúmenes huérfanos

```
docker volume rm <nombre del volumen>
```
