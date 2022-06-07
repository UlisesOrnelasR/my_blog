+++
title = "Git: Comandos (git rebase, git merge)"
date = "2022-06-07"
+++

En este post veremos el uso de git rebase, un comando que nos ayuda a mover una rama, a otro punto del árbol, OJO este comando reescribe la historial de los commits ten cuidado al usarlo, también veremos la diferencia entre usar este comando y git merge...🐤

<!--more-->

## Git Rebase

Ya hemos trabajado con ramas y vimos como fusionarla con otra usando git merge, pero en esta ocasión lo que haremos es usar git rebase.

g1

Este comando **puede mover una rama en su totalidad**, hacia otro punto del árbol.

Tanto como git merge como git rebase son comandos utiles, sin embargo, tienen sus diferencias para que a la hora de trabajar las tengas en cuenta.

**Usar git rebase es arriesgado**, ya que *reescribe el historial de commits*, si este comando se hace en el repositorio remoto, puede generar conflictos a la hora que otros desarrolladores intenten sacar los últimos cambios del repositorio remoto.

```
git rebase master
```

Un ejemplo de rebase es:

1.- Creamos una nueva rama *(rama2)* y realizamos un nueva funcionalidad, añadiendo commits.

2.- Realizamos unos cambios en la rama *master*, añadimos commits.

3.- Volvemos a rama2 y hacemos un git rebase para traernos los cambios de master.

```
git rebase master
```

g2

Gráficamente esto fue lo que sucedió, y lo que sucedería si usáramos *git merge*:

i1

Podemos notar que el orden como se acomodaron los commits **fue diferente**, y si usamos git merge se nos creara un commit extra.

Si usamos el comando:

```
git log --oneline --graph
```

Podemos ver también los cambios en las ramas.

Al usar este comando puede que se modifique el orden de los commits visualmente para el entendimiento de lo que paso con las ramas.

Pero el orden correcto de los commits se muestra usando solamente:

```
git log --oneline
```

**Recuerda usar git rebase solo en el repositorio local.** 😃

#### Por el momento podemos dar por finalizado este blog de git rebase comparándolo con git merge. 🚀

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
