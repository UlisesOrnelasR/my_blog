+++
title = "Git: Comandos básicos (git diff, git log, git show)"
date = "2022-06-02"
+++

En este post hablaremos acerca de comandos importantes a la hora que no sabemos bien que cambios se hicieron, estaremos enfocados en comandos de Git que devuelven información...🐣

<!--more-->
Para estos ejercicios yo usare la consola de PowerShell, tú puedes usar la que tu quieras, ya sea esta, el cmd, o git bash.

Para empezar a usar los comandos en la PowerShell, nos ubicaremos dentro de la carpeta de nuestro proyecto donde ya teníamos inicializado un repositorio.

En la barra de dirección escribimos 'powershell' y presionamos enter.

g1

## Git diff

Primeramente estaremos hablando de este comando:

```texto
git diff <file>
```

Este comando nos muestra los cambios que se realizaron en un cierto archivo, lee los cambios y los compara con una versión suya que fue guardada.

Para mostrar los archivos que se modificaron, podemos apoyarnos con un *git status -s*.

Modificare un archivo para que puedas entender cómo funciona.

i1

Ahora bien, en la terminal para que git nos muestre los cambios que hubo en este archivo usamos:

```texto
git diff <file>
```
g2

Podemos observar que con *git status* observamos los archivos modificados y con *git diff* los cambios específicamente en ese archivo.

## Git log

```texto
git log --oneline
``` 

Con *git log* podemos revisar el historial commits que se han hecho en la historia del proyecto, también podemos saber quién y cuando lo hizo.

g3

Podemos salir de la pantalla de git log presionando la tecla **q**. Así mismo con el comando:

```texto
git log --oneline
```
Podemos verlo de manera resumida, en otras consolas podríamos ver el código de manera más legible porque incorporan colores.

g4

Cada línea representara un commit que se haya hecho, hasta arriba mostrara el commit más reciente, y abajo los más antiguos respectivamente.

## Git status

Este comando ya lo hemos visto, recordemos que este comando nos mostrara los archivos que fueron modificados.

```texto
git status 
```

g5
## Git show

Es un comando que nos muestra información de objetos ya subidos al repo local. En esta ocasión lo usaremos para mostrar cuales fueron los cambios en un commit en específico.

Por ejemplo, usaremos el comando *git log* para mostrar los commits que se hicieron en el proyecto.

i2

Seguido usaremos el comando de git show junto con el identificador del commit.

```texto
git show <identificador del commit>
```

g6

Podemos observar que nos muestra cual fue el cambio que se realizó en este commit, en este caso se agregó una línea que dice 'volumen bajo'.
#### Enhorabuena ahora ya sabes más comando de git, con forme avancemos, seguiremos usando estos comandos e iremos conociendo más. 🚀

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
