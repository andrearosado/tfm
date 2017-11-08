# tfm
Trabajo Final (TFM) para obtener título Máster SIG y Teledetección de la Universidad de Zaragoza

# Trabajo con esta plantilla

No es necesario tener LaTeX instalado para trabajar con esta plantilla. Únicamente es imprescindible tener instalado el *Docker engine* y una buena conexión a internet.

Es muy sencillo lanzar un contenedor *Docker* con Texlive y Texmaker ya instalados, y trabajar en el escritorio del siguiente modo:

```sh
docker run -it --rm=true -e USER=$USER -e USERID=$UID -v /tmp/.X11-unix:/tmp/.X11-unix -e DISPLAY=unix$DISPLAY --device /dev/dri -v $HOME:/home/texmaker --name texmaker benizar/texmaker
```

Los cambios que realicemos desde la aplicación (dentro del *docker*) se reflejarán en nuestra máquina y viceversa, de un modo muy natural. De este modo es posible trabajar desde otros PC sin necesidad de hacer nada especial.
