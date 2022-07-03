+++
title = "Archivos de Barril en React js"
date = "2022-07-03"
+++

En este post veremos como implementar los Archivos de barril en React y al final importar los componentes que necesitemos en una sola línea...

<!--more-->
## Archivos de Barril📁📚

![i3](https://user-images.githubusercontent.com/99143567/177057820-99df5092-059d-4f0d-bc19-2408bef5c1e5.png)

Esta funcionalidad es propia de Javascript y también puede ser aplicada en TypeScript, la finalidad es que todos los componentes estén **centralizados**.

Veremos como podemos hacer esto en un proyecto de React, que tengo preparado.

Podemos observar que tengo múltiples componentes importados a un mismo archivo:

![i1](https://user-images.githubusercontent.com/99143567/177057824-baa4c671-c256-446a-8de1-5c4ec83ad79c.JPG)

🛸 Dentro de la carpeta **components** o en cualquier carpeta que tengamos múltiples importaciones, creamos un archivo **index.js**

🛸 Escribimos todos lo componentes que queremos exportar, en mi caso:

```
export * from './TaskCreator'
export * from './TaskTable'
export * from './Container'
```

![g1](https://user-images.githubusercontent.com/99143567/177057829-b29cef6c-c980-4267-9505-f09ade230bd5.gif)

🛸 Regresamos a nuestra componente principal donde anteriormente teníamos múltiples exportaciones.

**Haremos una única importación** con todos nuestros componentes de la siguiente manera, apuntando el *path* hacia el **index.js**

![g2](https://user-images.githubusercontent.com/99143567/177057830-d0b624c5-dc73-446a-a355-58f21d6b81b3.gif)

![i2](https://user-images.githubusercontent.com/99143567/177057836-d42dd362-d7d6-401a-8f70-c64d4cd4d3c7.png)

Postdata: Nótese que me falto un componente😅
#### En este post dejamos nuestra aplicación más limpia usando los Archivos de Barril para hacer más fáciles las importaciones en React😉🚀

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
