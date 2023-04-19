+++
title = "Git: Comandos básicos (git diff, git log, git show)"
date = "2023-04-16"
+++

En este post, hablaremos acerca de algunos comandos básicos de Git que nos pueden ayudar a conocer mejor los cambios que se han realizado en nuestro proyecto...🐣

<!--more-->

Para estos ejercicios, usaremos la consola de PowerShell, pero puedes utilizar la que prefieras, ya sea la consola de Windows (cmd) o Git Bash.

Antes de empezar, asegúrate de estar ubicado dentro de la carpeta de tu proyecto donde ya has inicializado un repositorio.

En la barra de dirección escribimos 'powershell' y presionamos enter.

![g1](https://user-images.githubusercontent.com/99143567/171784941-003c8c15-2af1-43c9-9868-3ebd56e8ece9.gif)

## Git diff

Primeramente estaremos hablando de este comando:

```texto
git diff <file>
```

El comando git diff nos permite ver los cambios que se han realizado en un archivo específico en comparación con la versión previa que se guardó.

Si quieres ver los archivos que se han modificado, puedes utilizar el comando _git status -s_.

Modificare un archivo para que puedas entender cómo funciona.

![i1](https://user-images.githubusercontent.com/99143567/171784971-dccd5846-3e91-4d76-8291-8cdd6bd346e8.png)

Ahora bien, en la terminal para que git nos muestre los cambios que hubo en este archivo usamos:

```texto
git diff <file>
```

![g2](https://user-images.githubusercontent.com/99143567/171784994-585668cf-99c4-46c0-b626-ff6bba725e31.gif)

Podemos observar que con _git status_ observamos los archivos modificados y con _git diff_ los cambios específicamente en ese archivo.

## Git log

```texto
git log --oneline
```

El comando _git log_ nos permite ver el historial de commits que se han hecho en el proyecto, junto con la información del autor y la fecha en que se realizó cada commit.

Para ver el historial de commits, puedes utilizar el siguiente comando:

```
git log
```

![g3](https://user-images.githubusercontent.com/99143567/171785015-7c1d7d01-a243-4cd7-aa72-c196e620584f.gif)

Podemos salir de la pantalla de git log presionando la tecla **q**. Así mismo con el comando:

```texto
git log --oneline
```

Podemos verlo de manera resumida, en otras consolas podríamos ver el código de manera más legible porque incorporan colores.

![g4](https://user-images.githubusercontent.com/99143567/171785030-728a6486-6ce6-4261-b09d-289dbbb8a207.png)

Cada línea representara un commit que se haya hecho, hasta arriba mostrara el commit más reciente, y abajo los más antiguos respectivamente.

## Git status

El comando git status nos permite ver los archivos que han sido modificados en nuestro proyecto.

Para ver los archivos que han sido modificados, puedes utilizar el siguiente comando:

```texto
git status
```

![g5](https://user-images.githubusercontent.com/99143567/171785051-88ebbff3-255f-4b70-b697-dd7e6242db5b.gif)

## Git show

El comando git show nos permite ver información detallada sobre un objeto que ya ha sido subido al repositorio local. En este caso, lo utilizaremos para ver los cambios realizados en un commit específico.

Por ejemplo, usaremos el comando _git log_ para mostrar los commits que se hicieron en el proyecto.

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

**git show:** Muestra información detallada sobre un objeto en particular (por ejemplo, un commit).

#### ¡Enhorabuena! Ahora conoces algunos comandos básicos de Git que te serán de gran ayuda en tu trabajo diario. A medida que avances en tu trabajo, irás descubriendo muchos más comandos útiles de Git. ¡Sigue adelante!🚀

_Deseando que te encuentres bien, te saluda Ulises🤵..._
_Sígueme en mis redes_
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
