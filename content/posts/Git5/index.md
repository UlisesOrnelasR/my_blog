+++
title = "Git y GitHub: Comandos (git clone, fork)"
date = "2022-04-18"
+++

Cuando se trata de colaborar en un proyecto, existen diferentes opciones para empezar a trabajar. En este post, vamos a ver cuándo es recomendable usar "git clone" y cuándo hacer un "fork" del proyecto...🐤

<!--more-->

## Git clone

Al trabajar en un proyecto con un equipo, lo más común es usar el comando _git clone_, el cual clona el proyecto de la nube de GitHub hacia tu entorno local para que puedas trabajarlo.

Este comando es diferente a simplemente descargar el proyecto, ya que clona el historial de commit completo del repositorio remoto:

![i1](https://user-images.githubusercontent.com/99143567/172074611-cd93f0a2-ccda-4b34-9ffb-117e327749e4.png)

Pudieras creer que es similar que descargar el proyecto, pero no, aquí las diferencias:
![i2](https://user-images.githubusercontent.com/99143567/172074620-6c426ea5-1f74-4bab-9aff-70cf8665cb82.png)

Puedes usar el comando de la siguiente manera:

```
git clone <remote-repo-url>
```

1.- Dirígete al repositorio del cual deseas descargar el proyecto.

2.- Selecciona la pestaña **Code** y copia la URL.

3.- Abre la consola en la carpeta en la que deseas descargar el proyecto.

4.- Escribe `git clone` seguido de la URL y presiona Enter.

Con estos pasos, tendrás el proyecto completo descargado y listo para realizar cambios y subirlos al repositorio remoto.

![g1](https://user-images.githubusercontent.com/99143567/172074631-5110e458-abc7-4850-92d1-10e1267d0c60.gif)

Si solo deseas clonar una rama específica, utiliza el siguiente comando:

```
git clone --branch <nombre del branch> <remote-repo-url>
```

## Fork

Si deseas hacer una copia independiente de un repositorio para modificarlo a tu gusto, entonces debes hacer un _fork_.

Al hacer un _fork_, se crea una copia del repositorio original en tu cuenta de GitHub. Este repositorio que se crea es independiente del original, es una copia que podemos modificar, borrar, corromper, reescribir los commits, etc. Somos los dueños de esa copia.
![i3](https://user-images.githubusercontent.com/99143567/172074638-4c22a0f9-8675-4951-bb02-c5bec8cdc5ac.png)
![i6](https://user-images.githubusercontent.com/99143567/172075807-3153da15-4b05-4c2e-acc3-1028a3e57367.png)
En un próximo post veremos lo que es un **pull request**... 😉

Para hacer un fork de algún proyecto, simplemente nos metemos al repositorio de ese proyecto y damos click en **fork**.

![g2](https://user-images.githubusercontent.com/99143567/172074643-0b95d02b-d8c2-41bd-a2a5-98d40164a94f.gif)

Podemos observar que se creó un repositorio exactamente igual que el original, somos libres de hacer lo que queramos con el.

#### Usaremos estos comandos e iremos conociendo más, conforme avancemos en este proceso de aprendizaje. 🚀

_Deseando que te encuentres bien, te saluda Ulises🤵..._
_Sígueme en mis redes_
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
