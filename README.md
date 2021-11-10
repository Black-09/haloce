![stability-wip](https://img.shields.io/badge/stability-unstable-lightgrey.svg)
<img src="https://i.imgur.com/zRXWDEK.png" width="190" height="164" align="right"/>

# Servidor dedicado de Halo CE dockerizado

## Acerca de

Este es un archivo Docker para ejecutar el servidor dedicado de Halo CE en Linux. El contenedor utiliza Wine para ejecutar la aplicación de Windows y xvfb para crear un escritorio virtual.

El contenedor se ejecuta 100% sin interfaz, es decir, no se requiere una interfaz gráfica de usuario para la instalación, la ejecución o la configuración.

## Pasos para instalar Docker

Actualiza la lista de paquetes disponibles de linux y sus versiones, pero no instala o actualiza ningún paquete

    apt update
    
Instala Docker en el vps linux

    apt-get install docker.io


## Instalar Servidor SAPP Halo CE

    git clone https://github.com/Black-09/haloce

## Ejecutar tu servidor Sapp

En la consola de tu vps debes dirigirte al directorio haloce con el siguiente comando :

    cd haloce
    
Ya dentro del directorio debemos crear nuestro contenedor con los archivos de nuestros SAPP Halo CE con el siguiente comando :

    docker build . 
    
Al terminar de crear nuestro contenedor nos saldra algo como esto :   

"Successfully built f01ecb978acc" <---- Con estos nuemero vamos a ejecutar nuestro servidor SAPP en nuestra VPS con el siguiente comando :

    docker run -it -p 2302:2302/udp f01ecb978acc 

Luego dan enter y automaticamente se ejecuta nuestro Servidor SAPP de Halo CE en nuestra vps


## Este proyecto simplifica la creacion del servidor SAPP de Halo CE de antimomentum ##

agradecimientos a :

antimomentum https://github.com/antimomentum


