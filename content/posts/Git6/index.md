+++
title = "Git: Comandos (git checkout, git branch)"
date = "2023-04-23"
+++

Para trabajar en equipo no es suficiente con los comandos que hemos visto, en este post revisaremos los usos de _git checkout_ y _git branch_ para darnos cuenta de su importancia...🐤

<!--more-->

## Git branch

Cuando un equipo trabaja en un proyecto, no es conveniente trabajar en la misma línea de desarrollo, ya que puede generar conflictos. Git resuelve este problema incorporando ramas o branches, que nos ayudan a separar el flujo de trabajo.

Por ejemplo, si vamos a trabajar en una nueva funcionalidad, podemos crear una nueva rama para esa funcionalidad y trabajar en ella sin interferir con el trabajo de los demás.

Una vez que hayamos completado nuestra funcionalidad, podemos unir los cambios con la rama principal, pero veremos eso en detalle en otro post...🧐

![i1](https://user-images.githubusercontent.com/99143567/172110072-e35f2c68-8ff3-4c2f-a368-26e094bdf51b.png)

**Estos son algunos comandos importantes que deberías conocer:**

Ver las ramas en el repositorio local:

```
git branch
```

Ver las ramas en el repositorio local como en el remoto:

```
git branch -a
```

Ver las ramas en el repositorio local y remoto, mostrando información de los commits:

```
git branch -a -v
```

Crear una nueva rama con el comando:

```
git branch <branch name>
```

![g1](https://user-images.githubusercontent.com/99143567/172110095-672e4c9a-0ac8-4d8b-8550-a5661d3d8713.gif)

También puedes cambiar el nombre de una rama existente::

```
git branch -m <branch name> <new branch name>
```

**Eliminar una rama.** Ten en cuenta que debes estar en una rama diferente para poder eliminarla::

```
git branch -d <branch name>
```

Si has realizado cambios en la rama y no los has fusionado, te mostrará un error, pero puedes forzar el borrado de la rama con el siguiente comando:

```
git branch -D <branch name>
```

## Git checkout

Git checkout es un comando muy interesante que puede hacer varias cosas.

**Visitar el pasado, entre los commits de nuestro proyecto.**

Sin embargo, no es recomendable realizar modificaciones cuando estamos visitando un commit, ya que solo deberíamos utilizarlo para revisar cómo estaba el proyecto en ese punto específico.

Durante el desarrollo de un proyecto, vemos que _HEAD_ apunta a la rama principal o a otra rama local. Pero cuando usamos git checkout en un commit específico, lo que sucede es que _HEAD_ ya no apunta a una rama, sino directamente al commit. A este estado se le llama detached _HEAD_.

![i2](https://user-images.githubusercontent.com/99143567/172110143-0c5a76d3-428d-4eb2-a139-cc46b33f4e7d.png)

El comando que usaremos es:

```
git checkout <ID del commit>
```

En este video podemos observar cómo volvemos al pasado en nuestro working directory. Los archivos y carpetas se muestran exactamente como estaban en ese commit, junto con el historial de commits.

![g2](https://user-images.githubusercontent.com/99143567/172110168-ee08cc9e-8c73-4f72-a0fd-4a256d268f11.gif)

Ten cuidado de no realizar cambios, recuerda que lo usamos con fines de observación solamente.

Con el comando anterior, nos quedamos observando un commit del pasado, pero ¿cómo podemos volver a la versión actual de nuestro proyecto?

Es fácil, volvemos a usar _git checkout_, pero esta vez hacemos que apunte a la rama master, que por defecto nos posicionará en el último commit que hayamos hecho en la rama master:

```
git checkout master
```

![g3](https://user-images.githubusercontent.com/99143567/172110194-ad18c003-18f9-48c1-aab4-1f57d931ad48.gif)

**Cambiar a otra rama**

Para cambiar a otra rama, utilizamos el siguiente comando:

```
git checkout <branch name>
```

Esto hará que el _HEAD_ apunte al último commit de la rama seleccionada.

![g4](https://user-images.githubusercontent.com/99143567/172110225-9850b9f4-538a-431d-92c3-0ccbe19e915d.gif)

![i3](https://user-images.githubusercontent.com/99143567/172220402-941249c5-165f-4c34-8d94-0d0993337484.png)

**Crear otra rama e ir a ella al instante**

Para crear una nueva rama y dirigirnos a ella con un solo comando podemos usar lo siguiente:

```
git checkout -b <branch name>
```

![g5](https://user-images.githubusercontent.com/99143567/172110250-24dfe675-cd90-44de-8284-6f584507eb1e.gif)

**Crear otra rama en base a otra e ir a ella al instante**

Por defecto, _git checkout -b_ se basará en la rama en la que esté el _HEAD_. Si queremos basarnos en otra rama, necesitamos agregar un parámetro adicional, que será el nombre de la rama en la que queremos basarnos.

```
git checkout -b ＜new branch＞ ＜existing-branch＞
```

![g6](https://user-images.githubusercontent.com/99143567/172110262-d58414e2-27f9-4c77-a5c4-2aad0af775c6.gif)

**Subir una rama al repositorio remoto(GitHub)**

Podemos subir nuestra nueva rama al repositorio remoto usando el comando push y especificando la rama que queremos subir:

```
git push -u origin ＜branch name＞
```

#### Hice este post con estos comandos juntos porque se utilizan con frecuencia en combinación. En futuras publicaciones, seguiremos incorporando más comandos y explorando cómo se pueden usar de manera efectiva en conjunto. 🚀

_Deseando que te encuentres bien, te saluda Ulises🤵..._
_Sígueme en mis redes_
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
