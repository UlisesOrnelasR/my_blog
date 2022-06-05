+++
title = "Git: Comandos (git reset, git reflog, git revert)"
date = "2022-06-04"
+++

*Git reset* es un comando que nos ayuda a deshacer uno o varios commits con el fin de revertir sus efectos, *git revert* tambien puede ayudarnos con esta tarea, pero lo hace de una manera diferente. En este post revisaremos que comando deberiamos usar y otros comandos de ayuda...🐤

<!--more-->
## Git reset

Este comando es útil cuando **no se ha subido el commit a GitHub**, esto es porque reescribe el historial de commits y trabajando con otros desarrolladores se complicaria mantener un historial consistente. En caso de que ya se haya subido el commit a GitHub, se recomienda usar *git revert* directamente...

Este comando nos permite devolver nuestro proyecto a un estado anterior, en el que quizas este no fallaba, o no tenia errores.

i1

**--mixed**

Usando git reset con  esta bandera(si no la pones es la función por defecto) lo que pasara es que git eliminara los commits que hubo despues del commit al que quieras regresar.

Eliminara los commits, **pero los cambios seguiran** en el *working directory*.

```
git reset --mixed <id del commit>
```
o

```
git reset  <id del commit>
```

Podemos observar en el siguiente video como funciona este comando:

g1

**--soft**

Usando git reset con  esta bandera lo que pasara es que git eliminara los commits que hubo despues del commit al que quieras regresar, de igual manera que usando la bandera mixed tambien **los cambios en el proyecto seguiran**, solo que con la bandera soft los cambios estaran en el *stage area*.

```
git reset --soft <id del commit>
```

Podemos observar en el siguiente video como funciona este comando:

g2 

**--hard**

Usando esta bandera con git reset, lo que pasara es que se **eliminara todo** lo que contengan los commits posteriores al seleccionado.

```
git reset --hard <id del commit>
```

Podemos observar en el siguiente video como funciona este comando:

g3

Puedes observar un resumen en esta imagen:

i2

## Git reflog

Este comando **captura todos los movimientos** que se hacen inlcuso si borras los commit.

```
git reflog
```

Entonces como ejercicio lo que haremos es:

1.-Mostrar todos los movimientos con *git reflog*, ya que no aparecen los commits que eliminamos. 

2.-Usaremos git reset --hard para regresar a ese punto donde si teniamos los commits.

g4

## Git revert

Git revert tambien **deshace commits anteriores**, pero lo que el hace en vez de sobreescribir el historial de commits como con git reset, este **crea un commit completamente nuevo** *sin los cambios que habia en ese commit que no deseamos*.

```
git revert
```

 Es decir, invierte los cambios implementados en ese commit que que no deseabamos y agrega un nuevo commit con el efecto contrario.

 Quizas puedas entenderlo mejor con esta imagen:

i3

Ahora vamos a deshacer un commit con git revert:

g5

Podemos observar como git revert, hace lo contrario al commit que  queremos eliminar.

En este caso el commit que yo queria eliminar, contenia la creación de un nuevo archivo, por lo que al ejecutar *git revert* lo elimina, dejandolo listo para hacer un nuevo commit con los cambios.

#### Excelente ahora nos metimos con comandos de git un poco mas avanzados, seguiremos usando estos comandos e iremos conociendo más. 🚀

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
