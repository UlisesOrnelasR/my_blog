+++
title = "Crear un proyecto de React con VITE, y configurar ESLINT y PRETTIER"
date = "2022-06-19"
+++

En este post usaremos [VITE](https://vitejs.dev/) para crear un proyecto de React, además de que configuraremos Eslint y Prettier correctamente para que no haya problemas al ejecutar sus comandos...

<!--more-->

## Crear un proyecto de React con VITE⚡

Si ya tienes el proyecto de React y solo quieres configurar Eslint y Pettier puedes saltar esta sección. 😅

i1

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

g1

Listo ya se creó nuestro proyecto, podemos ejecutarlo en el servidor local usando:

```
npm run dev
````

i2

## Configurar ESLINT y PRETTIER

i3

Una de las cosas más complicadas para los desarrolladores es configurar Eslint y Prettier, ya que suele haber conflictos entre estos dos si no se hace correctamente.

**[ESLint](https://eslint.org/docs/user-guide/getting-started)** se preocupara de que es lo que estamos escribiendo y qué significado tiene, además de que nos permitirá adoptar un estilo de código.

**[Prettier](https://prettier.io/docs/en/options.html)** se encargará de darle el formato adecuado a nuestro código, le dará una buena presentación y organización para que tenga una mejor legibilidad.

i4

## Instalando Eslint🔵

Para instalarlo usaremos el comando: 

```
npm i -D eslint
````

Seguido lo configuramos usando el comando: 

```
npx eslint --init
````

g2

Dentro de las opciones puedes presionar la tecla '*espacio*' para seleccionar otra opción. *Listo ya tenemos Eslint instalado y se nos ha creado un archivo de configuración **.eslintrc.js***.

Instalamos la *extensión* **ESLint** para que en pantalla se mostrasen los errores.

i5

#### Solución 'React' must be in scope when using JSX

Este error significa que para que por defecto siempre sea configurado "import React from 'react'", como estamos usando **VITE** **no es necesario esta configuración**.

Para solucionar este problema dentro del archivo de configuración de eslint, *nos aseguramos de agregar este plugin*.

i6

## Instalando Prettier🔵

Para instalar prettier usamos el comando:

```
npm i -D prettier
```

g3

## Configurando ESLint y Prettier🔵

Ahora es cuando surgen los problemas, Prettier pone punto y coma, Eslint los quita, etc.

Para configurar correctamente crearemos un archivo en el directorio raíz del proyecto llamdo **.prettierrc**, nos dirigimos a la documentación de [Prettier](https://prettier.io/docs/en/options.html) para ver que reglas podemos añadir.

g4

Configuramos de acuerdo a nuestras necesidades:

g5

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

g6

Ahora es cuando vienen los problemas, *Prettier pone puntos y comas* y *Eslint dice que no*.

Para solucionarlo tenemos que **instalar un paquete**, lo haremos con el siguiente comando y después **agregamos** lo siguiente al archivo de configuración de eslint:

```
npm i -D eslint-config-prettier
````

g7

Ahora las reglas de Prettier estarán sobre las de Eslint, esto quiere decir que cuando haya una confusión, hará lo que se haya establecido en Prettier.

## Configurando comandos para poder ejecutar ESLint y Prettier desde la terminal🔵

Antes **crearemos** un archivo en el directorio raíz llamado **.prettierignore** donde incluiremos la carpeta *dist* y el *archivo package-lock.json*, esto para que Prettier no toque estos archivos. El *node_modules* lo ignora por defecto.

Haremos lo mismo para Eslint, en el directorio raíz, creamos un archivo **.eslintignore** y **añadimos solamente** *dist*, ya que solamente lee archivos JS y JSX, por tanto no tocara el package-lock.json.

g8

Finalmente para terminar de configurar nos dirigimos al archivo *package.json* y creamos los comandos de lint y de format.

i7

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

i8

Esto se soluciona añadiendo esto al archivo de configuración *.eslintrc.js*:

```
settings: {
        react: {
            version: 'detect'
        }
    },
````

g9

Listo, ahora ya tenemos todo y podemos comenzar a trabajar. :)
#### En este blog aprendimos a crear un proyecto de React desde 0 con VITE y configurar correctamente Eslint y Prettier. 🚀

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
