+++
title = "Git: Comandos (git reset, git reflog, git revert)"
date = "2023-04-18"
+++

_Git reset_ es un comando que nos ayuda a deshacer uno o varios commits con el fin de revertir sus efectos, _git revert_ también puede ayudarnos con esta tarea, pero lo hace de una manera diferente. En este post revisaremos que comando deberíamos usar y otros comandos de ayuda...🐤

<!--more-->

## Git reset

Git reset nos permite revertir uno o varios commits, devolviendo nuestro proyecto a un estado anterior. Este comando es útil _si aún no hemos subido el commit a GitHub_, ya que reescribe el historial de commits y puede complicar la colaboración con otros desarrolladores.

En caso de que ya hayamos subido el commit a GitHub, se recomienda usar **git revert**en su lugar.

![i1](https://user-images.githubusercontent.com/99143567/172036441-32dbfe16-0013-4a03-905a-d6fd2b2cb199.png)

**Git reset** ofrece tres opciones de bandera que determinan cómo se eliminan los commits:

**--mixed**

Usando git reset con esta bandera (si no la pones es la función por defecto --mixed) lo que pasara es que git eliminara los commits que hubo después del commit al que quieras regresar.

Eliminará los commits, **pero los cambios seguiran** en el _working directory_.

```
git reset --mixed <ID del commit>
```

o

```
git reset <ID del commit>
```

Podemos observar en el siguiente video cómo funciona este comando:

![g1](https://user-images.githubusercontent.com/99143567/172036473-30a15844-4057-49c1-b6ad-971dad98dee0.gif)

**--soft**

Usando git reset con esta bandera lo que pasara es que git eliminara los commits que hubo después del commit al que quieras regresar, de igual manera que usando la bandera mixed tambien **los cambios en el proyecto seguirán**, solo que con la bandera soft los cambios estarán en el _stage area_.

```
git reset --soft <ID del commit>
```

Podemos observar en el siguiente video cómo funciona este comando:

![g2](https://user-images.githubusercontent.com/99143567/172036499-54437f43-526b-406e-8897-cbbe0797de04.gif)

**--hard**

Usando esta bandera con git reset, lo que pasara es que se **eliminara todo** lo que contengan los commits posteriores al seleccionado.

```
git reset --hard <ID del commit>
```

Podemos observar en el siguiente video cómo funciona este comando:

![g3](https://user-images.githubusercontent.com/99143567/172036519-546a9546-d30e-4c53-97a4-b1d406085097.gif)

Puedes observar un resumen en esta imagen:

![i2](https://user-images.githubusercontent.com/99143567/172036562-5f666c40-92e5-4c43-8b29-65632fc05dfc.png)

## Git reflog

`Git reflog` registra todos los movimientos que se han hecho, incluso si se eliminan los commits. Este comando es útil si necesitamos deshacer cambios que se hicieron hace varios commits.

Entonces lo que haremos es:

Podemos usar _git reflog_ para mostrar todos los movimientos realizados y encontrar el ID del commit al que queremos regresar. Luego, usamos git reset --hard con el ID del commit para regresar a ese punto específico.

```
git reflog
git reset --hard <ID del commit>
```

![g4](https://user-images.githubusercontent.com/99143567/172036566-6674e9db-6035-4c84-b669-e8da8ee316b7.gif)

## Git revert

Git revert tambien **deshace commits anteriores**, pero lo que este comando hace en vez de sobrescribir el historial de commits como con git reset, este **crea un commit completamente nuevo** _sin los cambios que había en ese commit que no deseamos_.

```
git revert
```

Es decir, invierte los cambios implementados en ese commit que no deseábamos y agrega un nuevo commit con el efecto contrario.

Quizas puedas entenderlo mejor con esta imagen:

![i3](https://user-images.githubusercontent.com/99143567/172036689-475a0c62-244b-4437-904b-19f3dfe1bb96.png)

Ahora vamos a deshacer un commit con git revert:

![g5](https://user-images.githubusercontent.com/99143567/172036575-d6a23aaf-3e0a-43dc-bb5b-f247775eaef6.gif)

Podemos observar cómo git revert, hace lo contrario al commit que queremos eliminar.

En este caso el commit que yo queria eliminar, contenia la creación de un nuevo archivo, por lo que al ejecutar _git revert_ lo elimina, dejándolo listo para hacer un nuevo commit con los cambios.

#### En este post, hemos explorado tres comandos de Git esenciales: git reset, git reflog y git revert. Cada comando tiene un propósito específico y puede ser útil en diferentes situaciones. Esperamos que esta información sea útil para tu próximo proyecto de programación. ¡Feliz codificación! 🚀

_Deseando que te encuentres bien, te saluda Ulises🤵..._
_Sígueme en mis redes_
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
