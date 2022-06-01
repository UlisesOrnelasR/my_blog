+++
title = "Git y Github: Fundamentos"
date = "2022-05-31"
+++

En este post entenderas que es Git y que es Github, aprenderas cuales son sus diferencias y porque es tan importante utilizar estas dos herramientas si eres un desarrollador de software...💻

<!--more-->
Primeramente vamos a aclarar que Git y Github son dos cosas muy diferentes, Git es la tecnologia que nos permitira versionar nuestro codigo localmente y Github nos brinda la opcion de guardar este repositorio en la nube, esto lo veremos mas adelante.

## ¿Que es Git?

**Git** es un sistema de *control de versiones* distribuido, es decir, git nos permitira tener un historial de como nuestro proyecto va creciendo, ademas mencionabamos que es distribuido, esto permitira cuando asi lo deseemos compartir todas esas versiones de cambios que hicimos a lo largo de la construcción del código.
![g3](https://user-images.githubusercontent.com/99143567/171487829-8f345219-be97-4f5b-a23b-c09082c0a1e6.png)


## ¿Que es Github?
Github aloja proyectos en la nube utilizando el sistema de control de versiones de git, podemos decir que localmente podemos guardar proyectos, pero github hara que estos cambios puedan estar en la nube, mas sin embargo github no tiene las funciones de git, github cumple con la funcion de almacenar todo el historial del código, pero git es el encargado de versionar el código.
![g4](https://user-images.githubusercontent.com/99143567/171487862-adefecad-4924-46d7-a90c-fbe6d4c3b232.png)


## Git es una herramienta muy potente que cumple con las siguientes ventajas y funcionalidades:🔨

**Tener un historial completo de las versiones de nuestro proyecto**:
  Con git podemos tener a la mano todos los cambios a lo largo de la contrucción de un proyecto, por ejemplo, en caso de insertar un error en el codigo accidentalmente, entre muchas otras cosas, git nos puede permitir regresar a una versión que no contenga este error y asi, podemos darnos una pista de como solucionarlo.

**Moverte en el tiempo**
Git permite moverte en el tiempo por todas las revisiones de código y desplazarte de forma sencilla.

**Almacena tu código**
Git permite almacenar el historial de tu proyecto de forma local.

**Facilita el trabajo en equipo**
Git permite que cada miembro del equipo obtenga una copia del proyecto para que asi pueda trabajar y no haya interferencias con lo que esta haciendo su compañero.

**Git es un sistema de control de versiones distribuido**
No depende de un repositorio central y permite trabajar incluso sin conexión.

**Permite trabajar con ramas**
    A la hora de trabajar en equipo, git brinda solución a la hora de estar todos aportando funcionalidades a un proyecto, y esto lo hace mediante las **branch**, haciendo que cada miembro del equipo pueda introducior sus cambios en una rama y fusionarla con la rama principal.

**Es un software libre**
Puedes contribuir a Git para mejorarlo.

**Permite respaldar tus proyectos en la nube, por ejemplo con GitHub**
Esto lo veremos mas adelante...

Por el momento para entender que es Git es suficiente.😉

## Flujo de trabajo en Git básico con Git y Github💱
**Working directory**
Aqui nos encontramos en nuestro computador en cualquier carpeta que queramos versionar.
Pero aun eliminando y modificando archivos estos cambios no se guardaran en nuestro control de versiones hasta que hallamos inicializado git, para ello usaremos el comando ``git init``, si es que no hay ningun repositorio local existente en esa ubicación.
Para versionar los cambios que hicimos, usaremos **git add** esto llevara nuestro cambios al Stage area.

**Stage area**
Aqui nuestros cambios ya se encuentran contemplados para que se guarden en el repositorio local, ahora lo que necesitamos es agregarle una descripción al cambio para que se guarde, para ello usaremos **git commit**

**Local repository**
Ahora nuestros cambios ya se encuentran guardador en el repositorio local, pero para guardarlos en un repositorio en la nube de Github usaremos **git push**.


**Remote repository**
Para almacenar y administrar nuestro código en la nube necesitaremos a **Github**, esta plataforma nos permite trabajar en equipo facilmente, la plataforma nos dejara descargar una version del proyecto para nosotros, en la cual podemos hacer nuestros cambios sin ningun problema.

Podemos ver todo esto de manera ilustrativa en la siguiente imagen:
![g1](https://user-images.githubusercontent.com/99143567/171487897-ce8ad44e-53d1-46f0-b525-410dedc7828c.png)

![g2](https://user-images.githubusercontent.com/99143567/171487923-3b816b53-6735-4266-af05-c1142e8bccb3.png)

#### Perfecto, ahora ya sabras diferenciar entre Git y Github, más adelante profundizaremos en este tema 🚀


*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
