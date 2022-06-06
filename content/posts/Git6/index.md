+++
title = "Git: Comandos (git checkout, git branch)"
date = "2022-06-05"
+++

Para trabajar en equipo no es suficiente con los comandos que hemos visto, en este post revisaremos los usos de *git checkout* y *git branch* para darnos cuenta de su importancia...🐤

<!--more-->

## Git branch

A la hora de que un equipo este trabajando en un proyecto, no podemos trabajar en una misma línea, en esencia sí, pero sería complicado, tendríamos conflictos.

Git resuelve este problema, incorporando ramas o branches, estas nos ayudaran a separar el flujo de trabajo, es decir, si yo voy a trabajar en una nueva funcionalidad, creo una nueva rama para esa funcionalidad, la agrego y no estoy interfiriendo con el trabajo de los demás.

Después de tener mi funcionalidad, puedo unir los cambios con la rama principal, pero eso lo veremos más adelante en otro post...🧐

i1

**Estos son algunos comandos importantes que deberías conocer: **

**Mirar que ramas hay en el repositorio local: **

```
git branch
```

Mirar que ramas hay tanto en el repositorio local como en el remoto:

```
git branch -a
```

Mirar que ramas hay tanto en el repositorio local como en el remoto, además mostrara información de los commits:

```
git branch -a -v
```

**Puedes crear una nueva rama con el comando: **

```
git branch <branch name>
```

g1

Podemos modificar el nombre de una rama:

```
git branch -m <branch name> <new branch name>
```

**Para eliminar una rama** podemos usar el siguiente comando, *debemos estar en otra rama para poder eliminarla*:

```
git branch -d <branch name>
```

Si realizamos cambios y no los fusionamos, nos devolverá un error, pero *podemos forzar el borrado de la rama con el comando*:

```
git branch -D <branch name>
```
## Git checkout

Git checkout es un comando muy interesante, puede hacer múltiples cosas.

**Podemos visitar al pasado, entre los commits de nuestro proyecto. **

Aun así, no es recomendable realizar modificaciones cuando estemos visitando un commit, solamente es aconsejable estar de visitante para revisar como estaba el proyecto en ese punto.

Durante el desarrollo de un proyecto vemos a **HEAD** apuntando hacia la rama principal, u otra rama local, pero lo que hacemos cuando usamos git checkout de algún commit, lo que sucede es que *HEAD* ya no apunta a una rama, apunta directamente al commit, a este estado se le llama *detached HEAD*.

i2

El comando que usaremos es:

```
git checkout <id del commit>
```

En este video podemos observar cómo volvemos al pasado, en nuestro working directory los archivos y carpetas están tal cual como estaban en ese commit, junto con el historial de commits.

g2

Ten cuidado de no realizar cambios, recuerda que lo usamos con fines de observación solamente.

Con el comando anterior, nos quedamos observando un commit del pasado, pero ¿cómo podemos volver a como esta nuestro proyecto actualmente?

Fácil, volvemos a usar git checkout pero hacemos que apunte a la rama master, por defecto nos posicionara en el último commit que hayamos hecho:

```
git checkout master
```

g3

**Cambiar a otra rama**

Para cambiar a otra rama, usamos el comando:

```
git checkout <branch name>
```

Esto hará que el *HEAD* apunte al último commit de la rama seleccionada.

g4

**Crear otra rama e ir a ella al instante**

Para crear una nueva rama y dirigirnos a ella con un solo comando podemos usar lo siguiente:

```
git checkout -b <branch name>
```

g5

**Crear otra rama en base a otra e ir a ella al instante**

De manera predeterminada *git checkout -b* se basará en la rama que este *HEAD*. Para basarnos en otra rama necesitamos agregar un parámetro adicional, este será la rama en la que queremos basarnos.

```
git checkout -b ＜branch name＞ ＜existing-branch＞
```

g6

#### Hice este post con estos comandos juntos, porque se usan mucho entre ellos, mas adelante seguiremos incorporando más comando, y viendo como es útil usarlo en conjunto. 🚀

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)

