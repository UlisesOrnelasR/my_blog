+++
title = "Crear un proyecto de React con VITE, y configurar ESLINT y PRETTIER"
date = "2022-06-19"
+++

En este post usaremos [VITE](https://vitejs.dev/) para crear un proyecto de React, además de que configuraremos Eslint y Prettier correctamente para que no haya problemas al ejecutar sus comandos...

<!--more-->

## Crear un proyecto de React con VITE⚡

Si ya tienes el proyecto de React y solo quieres configurar Eslint y Pettier puedes saltar esta sección. 😅

![i1](https://user-images.githubusercontent.com/99143567/174501048-c997321f-7665-4e10-93bb-e1c3877225d9.png)

Para nuestros proyectos **NO** estaremos usando el comando típico de 'create react app' para crear un proyecto de React. Nosotros usaremos **VITE**, esta herramienta nos permite crear un proyecto de Vue, Angular, **React**, etc.  

[VITE](https://vitejs.dev/) nos permitirá crear un proyecto, un servidor de desarrollo y también hacer **build** de nuestro código, a diferencia que **es más veloz que otras alternativas**, tanto como para ejecutar el código de desarrollo como para hacer el build de tus aplicaciones web.

Para crear el proyecto usando VITE, escribimos el comando y configuramos de acuerdo a nuestras necesidades:

```
npm init vite@latest
````

Posteriormente entramos a la carpeta creada para instalar la carpeta *node_modules*, usaremos el comando:

```
npm i
````

![g1](https://user-images.githubusercontent.com/99143567/174501056-43104906-1980-4042-9e4d-b10e2a8aee00.gif)

Listo ya se creó nuestro proyecto, podemos ejecutarlo en el servidor local usando:

```
npm run dev
````

![i2](https://user-images.githubusercontent.com/99143567/174501072-1b652621-50c0-4b17-9e60-0b5b68282bbd.JPG)

## Configurar ESLINT y PRETTIER

![i3](https://user-images.githubusercontent.com/99143567/174501076-7f373c7a-1313-415b-abc0-a2582aa4528d.png)

Una de las cosas más complicadas para los desarrolladores es configurar Eslint y Prettier, ya que suele haber conflictos entre estos dos si no se hace correctamente.

**[ESLint](https://eslint.org/docs/user-guide/getting-started)** se preocupara de que es lo que estamos escribiendo y qué significado tiene, además de que nos permitirá adoptar un estilo de código.

**[Prettier](https://prettier.io/docs/en/options.html)** se encargará de darle el formato adecuado a nuestro código, le dará una buena presentación y organización para que tenga una mejor legibilidad.

![i4](https://user-images.githubusercontent.com/99143567/174501090-db10d6b1-c6f5-4727-9f2c-38aa33d24f13.png)

## Instalando Eslint🔵

Para instalarlo usaremos el comando: 

```
npm i -D eslint
````

Seguido lo configuramos usando el comando: 

```
npx eslint --init
````

![g2](https://user-images.githubusercontent.com/99143567/174501101-1f02783b-5206-4c22-97df-774e9026b2bf.gif)

Dentro de las opciones puedes presionar la tecla '*espacio*' para seleccionar otra opción. *Listo ya tenemos Eslint instalado y se nos ha creado un archivo de configuración **.eslintrc.js***.

Instalamos la *extensión* **ESLint** para que en pantalla se mostrasen los errores.

![i5](https://user-images.githubusercontent.com/99143567/174501107-345ef1c5-2d8a-4d64-b8a3-1df48e9843df.JPG)

#### Solución 'React' must be in scope when using JSX

Este error significa que para que por defecto siempre sea configurado "import React from 'react'", como estamos usando **VITE** **no es necesario esta configuración**.

Para solucionar este problema dentro del archivo de configuración de eslint, *nos aseguramos de agregar este plugin*.

![i6](https://user-images.githubusercontent.com/99143567/174501115-967f3ba7-9f6c-4667-8c7d-5005be4f66a9.JPG)

## Instalando Prettier🔵

Para instalar prettier usamos el comando:

```
npm i -D prettier
```

![g3](https://user-images.githubusercontent.com/99143567/174501124-da6846c0-425f-446d-a6f8-10d616c7f751.gif)

## Configurando ESLint y Prettier🔵

Ahora es cuando surgen los problemas, Prettier pone punto y coma, Eslint los quita, etc.

Para configurar correctamente crearemos un archivo en el directorio raíz del proyecto llamdo **.prettierrc**, nos dirigimos a la documentación de [Prettier](https://prettier.io/docs/en/options.html) para ver que reglas podemos añadir.

![g4](https://user-images.githubusercontent.com/99143567/174501131-0544b484-eec9-4c22-904f-cdc5adcbdd4f.gif)

Configuramos de acuerdo a nuestras necesidades:

![g5](https://user-images.githubusercontent.com/99143567/174501133-3a2f5887-6746-4dac-8663-7c20bce20686.gif)

De esa manera puedes configurar el archivo, al final esta fue mi configuración en el archivo *.prettierrc*:

```
{
    "useTabs":true,
    "singleQuote":true,
    "jsxSingleQuote":true,
    "arrowParens":"avoid"
}
````

**Instalamos** la extensión de Prettier, y la **seleccionamos como formateador por defecto**, y por último,**activamos** la casilla para que cada vez que guardemos los cambios se dé formato automáticamente.

![g6](https://user-images.githubusercontent.com/99143567/174501139-74622a7d-7139-4c7a-b4e0-d40c6660a060.gif)

Ahora es cuando vienen los problemas, *Prettier pone puntos y comas* y *Eslint dice que no*.

Para solucionarlo tenemos que **instalar un paquete**, lo haremos con el siguiente comando y después **agregamos** lo siguiente al archivo de configuración de eslint:

```
npm i -D eslint-config-prettier
````

![g7](https://user-images.githubusercontent.com/99143567/174510247-e12e0908-2072-4260-a5f6-5f42202706e6.gif)

Ahora las reglas de Prettier estarán sobre las de Eslint, esto quiere decir que cuando haya una confusión, hará lo que se haya establecido en Prettier.

## Configurando comandos para poder ejecutar ESLint y Prettier desde la terminal🔵

Antes **crearemos** un archivo en el directorio raíz llamado **.prettierignore** donde incluiremos la carpeta *dist* y el *archivo package-lock.json*, esto para que Prettier no toque estos archivos. El *node_modules* lo ignora por defecto.

Haremos lo mismo para Eslint, en el directorio raíz, creamos un archivo **.eslintignore** y **añadimos solamente** *dist*, ya que solamente lee archivos JS y JSX, por tanto no tocara el package-lock.json.

![g8](https://user-images.githubusercontent.com/99143567/174501150-8bb818b7-f4ea-409a-be3a-fb49525d2789.gif)

Finalmente para terminar de configurar nos dirigimos al archivo *package.json* y creamos los comandos de lint y de format.

![i7](https://user-images.githubusercontent.com/99143567/174501152-30d36c10-d826-43d0-bda8-01709de66369.JPG)

Ahora ya podemos usar los comandos...😉

Para darle formato a todo✅:

```
npm run format
````

Para hacerle linting a todo✅:

```
npm run lint
````

Al ejecutar *npm run lint* nos saltara un warning:

![i8](https://user-images.githubusercontent.com/99143567/174501162-03abdc80-68de-4cbc-b1a8-a29d0e4f783d.JPG)

Esto se soluciona añadiendo esto al archivo de configuración *.eslintrc.js*:

```
settings: {
        react: {
            version: 'detect'
        }
    },
````

![g9](https://user-images.githubusercontent.com/99143567/174501171-89de1af3-b545-4720-9e7d-c4a60e792239.gif)

Listo, ahora ya tenemos todo y podemos comenzar a trabajar. :)
#### En este blog aprendimos a crear un proyecto de React desde 0 con VITE y configurar correctamente Eslint y Prettier. 🚀

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
