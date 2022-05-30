+++
title = "CSS: Elementos de bloque y de línea"
date = "2022-05-29"
+++

En este post hablaremos sobre como se clasifican las etiquetas o elementos HTML y como podemos cambiar cambiar esta propiedad para darle el uso que necesitemos.😉
<!--more-->

## Elementos de bloque

Una **etiqueta de bloque**, *abarca todo el ancho disponible* y *comienza en una nueva línea*, no permite que otro elemento se coloque a su lado.
Algunas de las etiquetas de bloque mas usadas son:

- ``<h1>``
- ``<h2>``
- ``<h3>``
- `` <ul>`` 
- ``<li>``
- ``<div>``
- ``<header>``
- ``<nav>``
- ``<footer>``
- ``<section>``
- ``<form>``
- ``<article>``

## Elementos de línea

Un **elemento de línea** abarca el *ancho minimo posible*, *permitiendo que otro elemento se coloque a su lado*.

 - ``<a>``
 -  ``<span>`` 
 -  ``<strong>``
 -  ``<img>`` 
 -  ``<input>`` 
 -  ``<code>``

## Cambiando entre estas propiedades💱

Podemos cambiar la propiedad de un elemento en el CSS con display.

#### Cambiando una etiqueta de bloque a línea

Recordemos que la etiqueta ``<p>`` es de bloque.
b1

Por lo tanto para cambiarla y poder tener las ventajas que ofrece que sea de línea, como que ocupe el ancho minimo podemos hacer lo siguiente.

1.- Creamos una clase con la propiedad **display** y le asignamos el valor **inline**.
b2

2.- Le asignamos esta clase a nuestra etiqueta de bloque, para que se *convierta a una etiqueta de linea*.
b3

#### Cambiando una etiqueta de línea a bloque

La etiqueta ``<a>`` en HTML es un elemento de línea. Podemos observar que ocupa el minimo ancho posible, y se pudo colocar a lado de otro elemento.
b4

Queremos cambiarlo a tipo bloque, para ello haremos lo siguiente:

1.- Creamos una clase con la propiedad **display** y le asignamos el valor **block**.
b5

2.- Le asignamos esta clase a nuestra etiqueta de bloque, para que se *convierta a una etiqueta de bloque*.
Podemos observar que ahora nuestra etiqueta abarca el *ancho total* y se mueve a una *linea nueva*.
b6

#### Display inline-block

Las diferencias entre inline y block contra inline-block, es que **inline-block** **permite dimensionar un elemento con un ancho y alto**, ademas de que tambien **permite que otro elemento se coloque a su lado**.

Crearemos dos clases para *cambiar* el ancho y alto.
b7

Las agreamos a una etiqueta de línea.
b8

Podemos observar que *no cambiaron* las dimensiones de nuestra etiqueta.

Pero si le agregamos la propiedad display: **inline-block;**
Existen **ventajas** porque *podria ponerse al lado de otro elemento*, ademas de que *pudieramos establecer un alto y un ancho*.
b9

#### Listo, ya tenemos nuestro webSite desplegado en una página de **GitHub Pages!** 🚀



*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sigueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[Linkedin](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)