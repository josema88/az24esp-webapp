# Aplicación web node-js + express

## Ejecutar aplicacion localmente
```sh
$ cd app

# Installar dependencias
$ npm install

# Ejecutar pruebas unitarias
$ npm test

# Levantar la aplicación
$ node app
```
La aplicación estará disponible en el puerto 8080.

## Construir y ejecutar app con Docker localmente
Ubicarse en el folder donde se encuentra el archivo *Dockerfile* e iniciar sesion en [DockerHub](https://hub.docker.com/).
```sh
# Iniciar sesion e ingresar Username y password
$ docker login

# Configurar variable de entorno el id de Docker Hub
$ export DOCKER_ID=dockerid

# Construir imagen (utilizando docker id)
$ docker build -t ${DOCKER_ID}/az24esp .

# Correr Imagen
$ docker run -it -d -p 80:8080 ${DOCKER_ID}/az24esp
```
La aplicacion estará disponible en el puerto 80.

## Subir Imagen a DockerHub
La imagen sera construida por default con el tag *latest*, por lo tanto la imagen sera subid a Docker Hub con el mismo tag.

```sh
$ docker push ${DOCKER_ID}/az24esp
```