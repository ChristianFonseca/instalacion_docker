# Instalacion de Docker
Instalación de Docker para Linux y Mac - Español

## Linux
### 1. Actualizacionde Sistema
Normalmente el sistema debe actualizarce por seguridad y confiabilidad en la instalacion de Docker.
Utilizar los siguientes comandos:

```
sudo apt update
sudo apt upgrade
```

### 2. Instalacion de paquetes previos
Se instalaran las dependencias y/o paquetes necesarios para que docker funcione correctamente.
```
sudo apt-get install curl apt-transport-https ca-certificates software-properties-common
```

### 3. Agregar repositorios de Docker
Ayudara a docker en su instalacion como paquete, usando la instalacion oficial.
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

Agregacion del repositorio
```
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```

Actualizacion de la informacion recibida
```
sudo apt update
```

Para asegurarnos de haber instalado desde el repositorio de Docker colocamos:
```
apt-cache policy docker-ce
```

Y la salida correcta que nos deberia salir debe ser la siguiente con diferentes numeros de version:
```
docker-ce:
   Installed: (none)
   Candidate: 16.04.1~ce~4-0~ubuntu
   Version table:
       16.04.1~ce~4-0~ubuntu 500
            500 https://download.docker.com/linux/ubuntubionic/stableamd64package
```

### 4. Instalaciòn de Docker
Usamos el siguiente comando para instalar Docker:
```
sudo apt-get install docker-ce
```

Y ya estarìa listo para usarse!

## MAC
### Descarga inicial
Se debe revisar si el procesador es de [Intel](https://desktop.docker.com/mac/main/amd64/Docker.dmg?utm_source=docker&utm_medium=webreferral&utm_campaign=docs-driven-download-mac-amd64) o [Apple Silicon](https://desktop.docker.com/mac/main/arm64/Docker.dmg?utm_source=docker&utm_medium=webreferral&utm_campaign=docs-driven-download-mac-arm64), y en funciòn de eso descargar el ```.dmg``` que se necesita haciendo click en el nomnbre correspondiente.

### Instalaciòn Interactiva
1. Doble click al archivo descargado ```Docker.dmg``` y agarrar y soltar al archivo mostrado al Applications Folder.

2. Doble click al archivo ```Docker.app``` en el Applications Folder para iniciar Docker.

3. Docker se iniciara, y si se requiere se puede iniciar con una cuenta de Google. Sin embargo, ya es posible utilizar los comandos docker desde el terminal.


