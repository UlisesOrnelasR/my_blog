+++
title = "Git: Comandos (git reset, git reflog, git revert)"
date = "2022-06-04"
+++

*Git reset* es un comando que nos ayuda a deshacer uno o varios commits con el fin de revertir sus efectos, *git revert* también puede ayudarnos con esta tarea, pero lo hace de una manera diferente. En este post revisaremos que comando deberíamos usar y otros comandos de ayuda...🐤

<!--more-->
## Git reset

Este comando es útil cuando **no se ha subido el commit a GitHub**, esto es porque reescribe el historial de commits y trabajando con otros desarrolladores se complicaría mantener un historial consistente. En caso de que ya se haya subido el commit a GitHub, se recomienda usar *git revert* directamente...

Este comando nos permite devolver nuestro proyecto a un estado anterior, en el que quizás este no fallaba, o no tenía errores.

![i1](https://user-images.githubusercontent.com/99143567/172036441-32dbfe16-0013-4a03-905a-d6fd2b2cb199.png)

**--mixed**

Usando git reset con esta bandera (si no la pones es la función por defecto --mixed) lo que pasara es que git eliminara los commits que hubo después del commit al que quieras regresar.

Eliminará los commits, **pero los cambios seguiran** en el *working directory*.

```
git reset --mixed <id del commit>
```
o

```
git reset <id del commit>
```

Podemos observar en el siguiente video cómo funciona este comando:

![g1](https://user-images.githubusercontent.com/99143567/172036473-30a15844-4057-49c1-b6ad-971dad98dee0.gif)

**--soft**

Usando git reset con esta bandera lo que pasara es que git eliminara los commits que hubo después del commit al que quieras regresar, de igual manera que usando la bandera mixed tambien **los cambios en el proyecto seguirán**, solo que con la bandera soft los cambios estarán en el *stage area*.

```
git reset --soft <id del commit>
```

Podemos observar en el siguiente video cómo funciona este comando:

![g2](https://user-images.githubusercontent.com/99143567/172036499-54437f43-526b-406e-8897-cbbe0797de04.gif)

**--hard**

Usando esta bandera con git reset, lo que pasara es que se **eliminara todo** lo que contengan los commits posteriores al seleccionado.

```
git reset --hard <id del commit>
```

Podemos observar en el siguiente video cómo funciona este comando:

![g3](https://user-images.githubusercontent.com/99143567/172036519-546a9546-d30e-4c53-97a4-b1d406085097.gif)

Puedes observar un resumen en esta imagen:

![i2](https://user-images.githubusercontent.com/99143567/172036562-5f666c40-92e5-4c43-8b29-65632fc05dfc.png)

## Git reflog

Este comando **captura todos los movimientos** que se hacen incluso si borras los commit.

```
git reflog
```

Entonces como ejercicio lo que haremos es:

1.-Mostrar todos los movimientos con *git reflog*, ya que no aparecen los commits que eliminamos. 

2.-Usaremos git reset --hard para regresar a ese punto donde si teníamos los commits.

![g4](https://user-images.githubusercontent.com/99143567/172036566-6674e9db-6035-4c84-b669-e8da8ee316b7.gif)

## Git revert

Git revert tambien **deshace commits anteriores**, pero lo que este comando hace en vez de sobrescribir el historial de commits como con git reset, este **crea un commit completamente nuevo** *sin los cambios que había en ese commit que no deseamos*.

```
git revert
```

 Es decir, invierte los cambios implementados en ese commit que no deseábamos y agrega un nuevo commit con el efecto contrario.

 Quizas puedas entenderlo mejor con esta imagen:

i3

Ahora vamos a deshacer un commit con git revert:

![g5](https://user-images.githubusercontent.com/99143567/172036575-d6a23aaf-3e0a-43dc-bb5b-f247775eaef6.gif)

Podemos observar cómo git revert, hace lo contrario al commit que queremos eliminar.

En este caso el commit que yo queria eliminar, contenia la creación de un nuevo archivo, por lo que al ejecutar *git revert* lo elimina, dejándolo listo para hacer un nuevo commit con los cambios.

#### Excelente ahora nos metimos con comandos de git un poco mas avanzados, seguiremos usando estos comandos e iremos conociendo más. 🚀

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
