+++
title = "CSS: Diferencias entre REM y EM (medidas relativas)"
date = "2022-05-29"
+++

Personalmente durante mi aprendizaje en CSS, solamente usaba unidades de medida en px, esta es una unidad de medida absoluta, es decir, que ya está definida y no depende de ninguna otra, como por ejemplo:

- padding: 50px;
- margin-top: 20px; etc, etc...
<!--more-->
Al ir profundizando mi conocimiento en CSS descubrí que no solamente podía usar unidades de medida absolutas, y que también existían las unidades relativas en CSS.

Esto quiere decir que se calculan a partir de otro valor de referencia.

## REM 📏

La unidad de medida **REM** es **relativa** al *HTML* que por defecto en los navegadores la manejan en 16px, **1rem = 16px**(por defecto)**.**
![i1](https://user-images.githubusercontent.com/99143567/170896028-9c8cfaee-d6a0-4591-b1be-83ed8457249e.JPG)


Entonces si nosotros en nuestro HTML escribimos un h1 y en el **CSS** le damos una medida de 1rem.
![gi1](https://user-images.githubusercontent.com/99143567/170896046-490678cc-ba2b-4fdb-a847-e15cc4a76915.gif)


El font-size del *h1* deberia ser 16px (1*16=16px).
![gi2](https://user-images.githubusercontent.com/99143567/170896051-a5318132-ba7f-4330-ba03-0fb0c884c6f5.gif)


Si ahora añadimos un párrafode 2rems, este debería tener un font-size de 32px (2*16=32px).
![gi3](https://user-images.githubusercontent.com/99143567/170896058-2c1e52bc-40d6-4ce8-90f5-d987068308d7.gif)


De esa forma funciona el REM, es *relativo* al **HTML** del navegador, puedes configurarle *otra medida*, pero es recomendable mantener el eestándarde **1rem = 16px.**
## EM 📏

No obstante el **EM**, es *relativo* al font-size del elemento HTML en el que se encuentra **1em = la medida del font-size del elemento.**
![gi4](https://user-images.githubusercontent.com/99143567/170896065-7c80b1df-e1fc-43eb-aba7-05eab4c60353.gif)


Y si *no existe* un font-size en esa etiqueta, tomara la medida del font-size del elemento superior.
![gi5](https://user-images.githubusercontent.com/99143567/170896068-65048a78-3e69-4d8b-9489-fc437b1658e3.gif)


En este caso, en el elemento *h3*, se le asasignóna medida de 2em al font-size, por lo tanto **sube al nivel superior** y encuentra que en la etiqueta *body* se tiene que font-size=14px.

Entonces el resultado para el font-size del elemento *h3* de 2em fue de 28px, (2*14=28px).

Si en este elemento asignamos un padding de 1em, recordemos que es **relativo** a la medida del font-size del elemento actual.
![gi6](https://user-images.githubusercontent.com/99143567/170896075-076d20c2-6d1e-4343-810e-605f3400798e.gif)


El padding es de 28px debido a que en el *font-size del elemento* *h3* es 2em = 28px, ahora esto sera igual a 1em = 28px en nuestras propiedades de este elemento.

Por lo tanto el padding de 1em resulto 28px.

#### *Ahora conoces las diferencias entre las medidas relativas REM y EM ✅ :D*

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sigueme en mis redes*

[GitHub](https://github.com/UlisesOrnelasR)
[Linkedin](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
