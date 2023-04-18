+++
title = "Git: Comandos (git rebase, git merge)"
date = "2023-04-18"
+++

En este post veremos el uso de git rebase, un comando que nos ayuda a mover una rama a otro punto del árbol. Sin embargo, es importante tener en cuenta que este comando reescribe el historial de commits, por lo que debemos tener cuidado al usarlo, especialmente en el repositorio remoto. También veremos las diferencias entre git rebase y git merge...🐤

<!--more-->

## Git Rebase

Ya hemos trabajado con ramas y vimos cómo fusionarlas con otra usando git merge, pero en esta ocasión utilizaremos git rebase.

![g1](https://user-images.githubusercontent.com/99143567/172306966-a529b9c5-fa9b-4514-82a9-0b6aaf916f6b.gif)

Este comando nos permite **mover una rama completa** a otro punto del árbol.

Tanto git merge como git rebase son comandos útiles, pero tienen diferencias importantes que debemos tener en cuenta al trabajar con ellos.

Es importante destacar que usar git rebase es **arriesgado**, ya que reescribe el historial de commits. Si se realiza este comando en el repositorio remoto, puede generar conflictos cuando otros desarrolladores intenten obtener los últimos cambios del repositorio remoto.

Un ejemplo de cómo usar git rebase es:

1.- Creamos una nueva rama _(rama2)_ y realizamos un nueva funcionalidad, añadiendo commits.

2.- Realizamos unos cambios en la rama _master_, añadimos commits.

3.- Volvemos a rama2 y hacemos un git rebase para traernos los cambios de master.

```
git rebase master
```

![g2](https://user-images.githubusercontent.com/99143567/172306986-28e60a05-bfff-4a18-bed5-d244727145a2.gif)

Gráficamente esto fue lo que sucedió, y lo que sucedería si usáramos _git merge_:

![git7](https://user-images.githubusercontent.com/99143567/172307553-85784d11-0aa4-4e08-aad7-26c19c7fd2c6.png)

Podemos notar que el orden como se acomodaron los commits **fue diferente**, y si usamos git merge se creará un commit extra.

Si usamos el comando:

```
git log --oneline --graph
```

Es importante tener en cuenta que al usar este comando se puede modificar el orden de los commits visualmente para entender lo que sucedió con las ramas.

Sin embargo, el orden correcto de los commits se muestra utilizando solamente:

```
git log --oneline
```

**Recuerda usar git rebase solo en el repositorio local.** 😃

#### Por el momento podemos dar por finalizado este blog de git rebase comparándolo con git merge. 🚀

_Deseando que te encuentres bien, te saluda Ulises🤵..._
_Sígueme en mis redes_
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
