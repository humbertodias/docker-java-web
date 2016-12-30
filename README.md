# ¿Qué es?

Servicio de JavaEE con Docker usando AlpineLinux.


# Prerrequisitos

1. [Docker](https://www.docker.com) 1.12+
2. [VirtualBox](www.virtualbox.org) 5.0+

# Cómo empezar

Construir

```
docker build -t docker-javaee .
```

Correndo

```
docker run -p 8080:8080 -d docker-javaee
```

Por último, en su navegador 

```
localhost:8080/hello
```

Respuesta

```
Hello Docker Tomcat World
```

# Acceso remoto

```
docker run -t -i docker-javaee /bin/sh
```

```
/usr/src/app #
```

# Cómo detener

Tome el ID del CONTENEDOR

```
docker ps
```

```
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS                    NAMES
76f8306bf53d        docker-javaee       "catalina.sh run"   2 minutes ago       Up 40 seconds       0.0.0.0:8080->8080/tcp   nostalgic_easley
```

Parada

```
docker stop 76f8306bf53d
```

o

Destruyendo

```
docker rm 76f8306bf53d
```

# ¿Cuanto cuesta?

Sólo ~135MB!

Dónde:

Paquete | MB
--- | ---
AlpineLinux | 4
Java | 113
Tomcat | 18

Mostrar docker imágenes

```
docker images
```

```
REPOSITORY            TAG                 IMAGE ID            CREATED             SIZE
docker-javaee         latest              6dc31cb08980        2 minutes ago       134.7 MB
```

# Referencias

1. [www.docker.com](https://www.docker.com)

2. [hub.docker.com](https://hub.docker.com)

3. [alpinelinux.org](https://alpinelinux.org)

4. [tomcat.apache.org](https://tomcat.apache.org/download-90.cgi)