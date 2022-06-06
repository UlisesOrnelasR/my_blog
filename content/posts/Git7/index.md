+++
title = "Git: Comandos (git fetch, git merge, git pull)"
date = "2022-06-06"
+++

En este post veremos comandos que nos ayudaran a descargar ramas que se crearon en el repositorio remoto, tambien veremos como fusionar ramas, como descargar los cambios que estan en el repo remoto pero que aun no los tenemos en el repositorio local, etc...🐤

<!--more-->

## Git Merge

En un post anterior vimos como crear ramas y como nos movemos hacia ellas.

Pero ahora, ¿como podemos fusionar esta rama que creamos con otra para que se apliquen los cambios que hicimos?.

g1

1.- Posicionarte en la rama que quieres que se apliquen los cambios de la otra.

2.- usar el comando git merge seguido pondras el nombre de la rama que quieres que se fusione con la que estas actualmente.

```
git merge <rama que se fusionara>
```

g2

**La fusión de las ramas puede producirse por tecnicas diferentes**, *git seleccionara de forma automatica la tecnica* de la fusión mas adecuada a menos que esta se especifique.

En caso de que git no pueda hacer la fusión tendrá que resolver los conflictos manualmente, indicar que es lo que se deseea hacer y luego con un commit guardar los cambios.

## Git Fetch y Git Pull 

i1

**Git fetch**es un comando que nos permite saber si hubo cambios en el repositorio remoto, solamente revisara si hubo cambios, hara que nuestro repositorio local se actualice con la ultima información, pero no hace que los podamos tener en nuestro espacio de trabajo, los mantendra como ocultos.

El comando de git fetch es:
```
git fetch
```

Con este comando podremos observar que estamos 1 commit abajo del repositorio remoto.

```
git branch -a -v
```

g3

**Git pull** tambien comprueba si hay cambios en el repositorio remoto, en caso de que si, **trae esos cambios a nuestro espacio de trabajo**.

**Git pull** hace un **git fetch** seguido de un **git merge**.

```
git pull origin master
```
g4

#### Vamos muy bien aprendiendo todos los comandos de git, si puedes notarlo estos ya son comandos mas avanzados y nos seran de gran ayuda al momento de estar trabajando en equipo. 🚀

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)

