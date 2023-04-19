+++
title = "Git: Comandos (git fetch, git merge, git pull)"
date = "2023-04-18"
+++

En este post veremos comandos que nos ayudarán a descargar ramas que se crearon en el repositorio remoto. También veremos cómo fusionar ramas y cómo descargar los cambios que están en el repo remoto pero que aún no los tenemos en el repositorio local...🐤

<!--more-->

## Git Merge

En un post anterior vimos cómo crear ramas y cómo movernos hacia ellas.

Pero ahora, ¿cómo podemos fusionar esta rama que creamos con otra para que se apliquen los cambios que hicimos?

![g1](https://user-images.githubusercontent.com/99143567/172264432-276e3754-6494-407e-b789-998b85c56b86.gif)

1.- Posiciónate en la rama en la que deseas que se apliquen los cambios de la otra.

2.- Usa el comando git merge seguido del nombre de la rama con la que deseas fusionarla.

```
git merge <rama que se fusionará>
```

![g2](https://user-images.githubusercontent.com/99143567/172264452-3e0538d6-47f5-41de-800f-dc916021a06b.gif)

**La fusión de las ramas puede producirse por técnicas diferentes**. Git seleccionará de forma automática la técnica de fusión más adecuada a menos que se especifique.

En caso de que Git no pueda hacer la fusión, tendrás que resolver los conflictos manualmente, indicar qué es lo que se desea hacer y, luego, guardar los cambios con un commit.

## Git Fetch y Git Pull

![i1](https://user-images.githubusercontent.com/99143567/172264464-534cbf06-5e39-415a-815e-78e64c43ffd8.png)

**Git fetch** es un comando que nos permite saber si hubo cambios en el repositorio remoto. Solamente revisará si hubo cambios, actualizará nuestro repositorio local con la última información, pero no la tendremos en nuestro espacio de trabajo; los cambios se mantendrán como ocultos.

El comando de git fetch es:

```
git fetch
```

Con este comando podremos observar que estamos a 1 commit por debajo del repositorio remoto.

```
git branch -a -v
```

![g3](https://user-images.githubusercontent.com/99143567/172264503-247de3bc-aff5-477e-a7cf-bc0a183e14fe.gif)

**Git pull** también comprueba si hay cambios en el repositorio remoto, en caso de que si, **trae esos cambios a nuestro espacio de trabajo**.

**Git pull** hace un _git fetch_ seguido de un _git merge_.

```
git pull origin master
```

![g4](https://user-images.githubusercontent.com/99143567/172264519-41880aae-4ff1-494a-be77-86f116b5bfc7.gif)

#### Vamos muy bien aprendiendo todos los comandos de Git. Si te fijas, estos ya son comandos más avanzados y nos serán de gran ayuda cuando trabajemos en equipo. 🚀

_Deseando que te encuentres bien, te saluda Ulises🤵..._
_Sígueme en mis redes_
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
