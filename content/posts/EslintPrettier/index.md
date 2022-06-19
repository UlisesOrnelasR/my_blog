+++
title = "Crear un proyecto de React con VITE, y configurar ESLINT y PRETTIER"
date = "2022-06-19"
+++

En este post usaremos VITE para crear un proyecto de React, ademas de que configuraremos Eslint y Prettier correctamente para que no haya problemas al ejecutar sus comandos...

<!--more-->

## Crear un proyecto de React con VITE⚡

Si ya tienes el proyecto de React y solo quieres configurar Eslint y Pettier puedes saltar esta sección.😅

i1

Para nuestro proyectos **NO** estaremos usando el comando tipico de 'create react app' para crear un proyecto de React. Nosotros usaremos **VITE**, esta herramienta nos permite crear un proyectos de Vue, Angular, **React**, etc.  

VITE nos permitira crear un proyecto, un servidor de desarrollo y tambien hacer **build** de nuestro codigo, a diferencia que **VITE es mas veloz que otras alternativas**, tanto como para ejecutar el codigo de desarrollo como para hacer el build de tus aplicaciones web.

Para crear el proyecto usando VITE, escribimos el comando y configuramos deacuerdo a nuestras necesidades:

```
npm init vite@latest
````

Posteriormente entramos a la carpeta creada para instalar la carpeta *node_modules*, usaremos el comando:

```
npm i
````

g1

Listo ya se creo nuestro proyecto, podemos ejecutarlo en el servidor local usando:

```
npm run dev
````

i2

## Configurar ESLINT y PRETTIER

i3

Una de las cosas mas complicadas para los desarrolladores es configurar Eslint y Prettier, ya que suele haber conflictos entre estos dos si no se hace correctamente.

**Eslint** se preocupara de que es lo que estamos escribiendo y que significado tiene, ademas de que nos permitira adoptar un estilo de código.

**Prettier** se encargará de darle el formato adecuado a nuestro codigo, le dara una buena presentación y organización para que tenga una mejor legibilidad.

i4

#### Instalando Eslint

Para instalarlo usaremos el comando: 

```
npm i -D eslint
````

Seguido lo configuramos usando el comando: 

```
npx eslint --init
````

#### En este blog aprendimos a crear un proyecto de React desde 0 con VITE y configurar correctamente Eslint y Pettier. 🚀

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
