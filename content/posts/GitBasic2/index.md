+++
title = "Git: Comandos básicos (git diff, git log, git show)"
date = "2022-06-02"
+++

En este post hablaremos acerca de comandos que nos servirán a la hora que no sabemos bien que cambios se hicieron, estaremos enfocados en comandos de Git que devuelven información...🐣

<!--more-->
Para estos ejercicios yo usare la consola de PowerShell, tú puedes usar la que tu quieras, ya sea esta, el cmd, o git bash.

Para empezar a usar los comandos en la PowerShell, nos ubicaremos dentro de la carpeta de nuestro proyecto donde ya teníamos inicializado un repositorio.

En la barra de dirección escribimos 'powershell' y presionamos enter.

![g1](https://user-images.githubusercontent.com/99143567/171784941-003c8c15-2af1-43c9-9868-3ebd56e8ece9.gif)

## Git diff

Primeramente estaremos hablando de este comando:

```texto
git diff <file>
```

Este comando nos muestra los cambios que se realizaron en un cierto archivo, lee los cambios y los compara con una versión suya que fue guardada.

Para mostrar los archivos que se modificaron, podemos apoyarnos con un *git status -s*.

Modificare un archivo para que puedas entender cómo funciona.

![i1](https://user-images.githubusercontent.com/99143567/171784971-dccd5846-3e91-4d76-8291-8cdd6bd346e8.png)

Ahora bien, en la terminal para que git nos muestre los cambios que hubo en este archivo usamos:

```texto
git diff <file>
```
![g2](https://user-images.githubusercontent.com/99143567/171784994-585668cf-99c4-46c0-b626-ff6bba725e31.gif)

Podemos observar que con *git status* observamos los archivos modificados y con *git diff* los cambios específicamente en ese archivo.

## Git log

```texto
git log --oneline
``` 

Con *git log* podemos revisar el historial commits que se han hecho en la historia del proyecto, también podemos saber quién y cuando lo hizo.

![g3](https://user-images.githubusercontent.com/99143567/171785015-7c1d7d01-a243-4cd7-aa72-c196e620584f.gif)

Podemos salir de la pantalla de git log presionando la tecla **q**. Así mismo con el comando:

```texto
git log --oneline
```
Podemos verlo de manera resumida, en otras consolas podríamos ver el código de manera más legible porque incorporan colores.

![g4](https://user-images.githubusercontent.com/99143567/171785030-728a6486-6ce6-4261-b09d-289dbbb8a207.png)

Cada línea representara un commit que se haya hecho, hasta arriba mostrara el commit más reciente, y abajo los más antiguos respectivamente.

## Git status

Este comando ya lo hemos visto, recordemos que este comando nos mostrara los archivos que fueron modificados.

```texto
git status 
```

![g5](https://user-images.githubusercontent.com/99143567/171785051-88ebbff3-255f-4b70-b697-dd7e6242db5b.gif)

## Git show

Es un comando que nos muestra información de objetos ya subidos al repo local. En esta ocasión lo usaremos para mostrar cuales fueron los cambios en un commit en específico.

Por ejemplo, usaremos el comando *git log* para mostrar los commits que se hicieron en el proyecto.

![i2](https://user-images.githubusercontent.com/99143567/171785070-17ac01f9-1ba2-4483-af5e-12a0a81ebb19.JPG)

Seguido usaremos el comando de git show junto con el identificador del commit.

```texto
git show <identificador del commit>
```

![g6](https://user-images.githubusercontent.com/99143567/171785093-0b4a4f7a-6728-41b4-acf1-dd909e9fa69a.gif)

Podemos observar que nos muestra cual fue el cambio que se realizó en este commit, en este caso se agregó una línea que dice 'volumen bajo'.

En resumen:

**git status:** Muestra las modificaciones que se hicieron en los archivos.

**git diff:** Muestra las modificaciones de un archivo en especifico.

**git log:** Muestra el historial de commits del proyecto.

**git show:** Muestra el objeto en específico, en este caso lo usamos para revisar un commit.

#### Enhorabuena ahora ya sabes más comandos de git, conforme avancemos, seguiremos usando estos comandos e iremos conociendo más. 🚀

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
