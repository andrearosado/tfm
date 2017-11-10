# tfm
Trabajo Final (TFM) para obtener título Máster SIG y Teledetección de la Universidad de Zaragoza

## Cómo colaborar

*En este ejemplo se sincroniza siempre la rama 'master' desde la misma rama del repositorio original, pero podría hacerse para cualquier otra rama.*

I use 'master' in the example for pulling from the original repo, but you could pull from any branch.

Es posible hacer un 'fork' y después proponer cambios del siguiente modo:

1. Clonar el fork

    git clone git@github.com:YOUR-USERNAME/YOUR-FORKED-REPO.git

2. Añadir una rama remota desde el repositorio original al fork 

    cd into/cloned/fork-repo
    git remote add upstream git://github.com/ORIGINAL-DEV-USERNAME/REPO-YOU-FORKED-FROM.git
    git fetch upstream

3. Actualizar el fork desde el repositorio original para recoger sus cambios

    git pull upstream master

4. Subir a GitHub el repositorio para que los dos repositorios online estén sincronizados

    git push origin master


## Editar el trabajo

No es necesario tener LaTeX instalado para trabajar con esta plantilla. Únicamente es imprescindible tener instalado el *Docker engine* y una buena conexión a internet.

Es muy sencillo lanzar un contenedor *Docker* con Texlive y Texmaker ya instalados, y trabajar en el escritorio del siguiente modo:

```sh
docker run -it --rm=true -e USER=$USER -e USERID=$UID -v /tmp/.X11-unix:/tmp/.X11-unix -e DISPLAY=unix$DISPLAY --device /dev/dri -v $HOME:/home/texmaker --name texmaker benizar/texmaker
```

Los cambios que realicemos desde la aplicación (dentro del *docker*) se reflejarán en nuestra máquina y viceversa, de un modo muy natural. De este modo es posible trabajar desde otros PC sin necesidad de hacer nada especial.
