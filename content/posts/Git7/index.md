+++
title = "Git: Comandos (git fetch, git merge, git pull)"
date = "2022-06-06"
+++

En este post veremos comandos que nos ayudaran a descargar ramas que se crearon en el repositorio remoto, también veremos como fusionar ramas, como descargar los cambios que están en el repo remoto pero que aún no los tenemos en el repositorio local, etc...🐤

<!--more-->

## Git Merge

En un post anterior vimos cómo crear ramas y como nos movemos hacia ellas.

Pero ahora, ¿cómo podemos fusionar esta rama que creamos con otra para que se apliquen los cambios que hicimos?

![g1](https://user-images.githubusercontent.com/99143567/172264432-276e3754-6494-407e-b789-998b85c56b86.gif)

1.- Posicionarte en la rama que quieres que se apliquen los cambios de la otra.

2.- usar el comando git merge seguido pondrás el nombre de la rama que quieres que se fusione con la que estas actualmente.

```
git merge <rama que se fusionara>
```

![g2](https://user-images.githubusercontent.com/99143567/172264452-3e0538d6-47f5-41de-800f-dc916021a06b.gif)

**La fusión de las ramas puede producirse por técnicas diferentes**, *git seleccionara de forma automática la técnica* de la fusión más adecuada a menos que esta se especifique.

En caso de que git no pueda hacer la fusión tendrá que resolver los conflictos manualmente, indicar que es lo que se desea hacer y luego con un commit guardar los cambios.

## Git Fetch y Git Pull 

![i1](https://user-images.githubusercontent.com/99143567/172264464-534cbf06-5e39-415a-815e-78e64c43ffd8.png)

**Git fetch** es un comando que nos permite saber si hubo cambios en el repositorio remoto, solamente revisara si hubo cambios, hará que nuestro repositorio local se actualice con la última información, pero no hace que los podamos tener en nuestro espacio de trabajo, los mantendrá como ocultos.

El comando de git fetch es:
```
git fetch
```

Con este comando podremos observar que estamos 1 commit abajo del repositorio remoto.

```
git branch -a -v
```

![g3](https://user-images.githubusercontent.com/99143567/172264503-247de3bc-aff5-477e-a7cf-bc0a183e14fe.gif)

**Git pull** también comprueba si hay cambios en el repositorio remoto, en caso de que si, **trae esos cambios a nuestro espacio de trabajo**.

**Git pull** hace un **git fetch** seguido de un **git merge**.

```
git pull origin master
```
![g4](https://user-images.githubusercontent.com/99143567/172264519-41880aae-4ff1-494a-be77-86f116b5bfc7.gif)

#### Vamos muy bien aprendiendo todos los comandos de git, si puedes notarlo estos ya son comandos más avanzados y nos serán de gran ayuda al momento de estar trabajando en equipo. 🚀

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
