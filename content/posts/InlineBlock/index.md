+++
title = "CSS: Elementos de bloque y de línea"
date = "2022-05-29"
+++

En este post hablaremos sobre cómo se clasifican las etiquetas o elementos HTML y cómo podemos cambiar esta propiedad para darle el uso que necesitemos. 😉
<!--more-->

## Elementos de bloque

Una **etiqueta de bloque**, *abarca todo el ancho disponible* y *comienza en una nueva línea*, no permite que otro elemento se coloque a su lado.
Algunas de las etiquetas de bloque más usadas son:

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

Un **elemento de línea** abarca el *ancho mínimo posible*, *permitiendo que otro elemento se coloque a su lado*.

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
![b1](https://user-images.githubusercontent.com/99143567/170921077-6ed4ca80-7c7e-4141-87ce-b62ba69331d3.JPG)

Por lo tanto, para cambiarla y poder tener las ventajas que ofrece que sea de línea, como que ocupe el ancho mínimo podemos hacer lo siguiente.

1.- Creamos una clase con la propiedad **display** y le asignamos el valor **inline**.
![b2](https://user-images.githubusercontent.com/99143567/170921097-0513862b-c883-4637-b652-08115596b383.JPG)

2.- Le asignamos esta clase a nuestra etiqueta de bloque, para que se *convierta a una etiqueta de línea*.
![b3](https://user-images.githubusercontent.com/99143567/170921846-bde39206-3cba-46af-8ba8-2e6aad039771.JPG)

#### Cambiando una etiqueta de línea a bloque

La etiqueta ``<a>`` en HTML es un elemento de línea. Podemos observar que ocupa el mínimo ancho posible, y se pudo colocar a lado de otro elemento.
![b4](https://user-images.githubusercontent.com/99143567/170921132-7c252197-f111-43c1-af97-5e0894278138.JPG)

Queremos cambiarlo a tipo bloque, para ello haremos lo siguiente:

1.- Creamos una clase con la propiedad **display** y le asignamos el valor **block**.
![b5](https://user-images.githubusercontent.com/99143567/170921160-5054e450-b776-4aa8-bde5-6f42493d95cf.JPG)

2.- Le asignamos esta clase a nuestra etiqueta de bloque, para que se *convierta a una etiqueta de bloque*.
Podemos observar que ahora nuestra etiqueta abarca el *ancho total* y se mueve a una *línea nueva*.
![b6](https://user-images.githubusercontent.com/99143567/170921178-42440659-d68e-44be-9034-417bbf230d40.JPG)

#### Display inline-block

Las diferencias entre inline y block contra inline-block, es que **inline-block** **permite dimensionar un elemento con un ancho y alto**, además de que también **permite que otro elemento se coloque a su lado**.

Crearemos dos clases para *cambiar* el ancho y alto.
![b7](https://user-images.githubusercontent.com/99143567/170921218-f691e404-f738-4505-80ca-153a06b73b4d.JPG)

Las agregamos a una etiqueta de línea.
![b8](https://user-images.githubusercontent.com/99143567/170921251-599fcb95-22f0-42c4-b697-2caebce5c97e.JPG)

Podemos observar que *no cambiaron* las dimensiones de nuestra etiqueta.

Pero si le agregamos la propiedad display: **inline-block;**
![b10](https://user-images.githubusercontent.com/99143567/170922453-ad035138-5b47-497b-979f-e2a1b34909af.JPG)

Existen **ventajas** porque *podría ponerse al lado de otro elemento*, además de que *pudiéramos establecer un alto y un ancho*.
![b9](https://user-images.githubusercontent.com/99143567/170921264-7ca4fabc-752f-430d-b55f-b37ccb9caf87.JPG)

#### Ahora ya sabemos las diferencias entre los elementos inline y block y como cambiar estas propiedades para nuestro beneficio 🚀


*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
