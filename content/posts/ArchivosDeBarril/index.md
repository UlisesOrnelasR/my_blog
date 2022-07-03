+++
title = "Archivos de Barril en React js"
date = "2022-07-03"
+++

En este post veremos como implementar los Archivos de barril en React y al final importar los componentes que necesitemos en una sola línea...

<!--more-->
## Archivos de Barril📁📚

Esta funcionalidad es propia de React y también puede ser aplicada en TypeScript, la finalidad es que todos los componentes estén **centralizados**.

Veremos como podemos hacer esto en un proyecto de React, que tengo preparado.

Podemos observar que tengo múltiples componentes importados a un mismo archivo:

i1

🛸 Dentro de la carpeta **components** o en cualquier carpeta que tengamos múltiples importaciones, creamos un archivo **index.js**

🛸 Escribimos todos lo componentes que queremos exportar, en mi caso:

```
export * from './TaskCreator'
export * from './TaskTable'
export * from './Container'
```

g1

🛸 Regresamos a nuestra componente principal donde anteriormente teníamos múltiples exportaciones.

**Haremos una única importación** con todos nuestros componentes de la siguiente manera, apuntando el *path* hacia el **index.js**

g2

i2

#### En este post dejamos nuestra aplicación más limpia usando los Archivos de Barril para hacer más fáciles las importaciones en React😉🚀

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
