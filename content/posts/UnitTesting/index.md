+++
title = "Integrar Testing con a tu proyecto de React JS"
date = "2022-06-22"
+++

En esta publicación veremos como integrar pruebas de unidad a nuestro proyecto de React JS, utilizando [JEST](https://jestjs.io/)🃏...

<!--more-->
## Unit Testing

Las pruebas de unidad son **muy importates** en un proyecto, tanto asi, que decia mi mentor [CarloGilmar](https://twitter.com/carlogilmar) durante mi travesia en Launch X "Las pruebas no son negociables, ¿Como compruebas que tu proyecto realmente funciona?-Con pruebas".

Tristemente tenemos una cultura donde se cree que las pruebas son una perdida de tiempo, que tardariamos incluso mas del doble en realizar una funcionalidad, pero **esto no es asi**, este tiempo en que realizariamos las pruebas nos lo tomaria en corregir los posibles bugs que tengamos sin hacer pruebas.

No obstante, realizar pruebas no quiere decir que estemos excetos de tener errores en nuestra aplicación, **somos humanos y comentemos errores**.

Gracias a las pruebas podemos corregir bugs o errores, antes de desplegar la aplicación en producción, ademas de que agregan **calidad** a nuestro software.

## Pruebas Unitarias

Las pruebas unitarias estan orientadas a pequeñas funcionalidades de un componente en especifico.

i2

## Pruebas de Integración

Las pruebas de integración estan orientadas a probar como interactuan los componentes entre si, a probar su comportamiento.

i3

## Integrar Testing a tu proyecto de React js

i1

#### Instalando jest🔵

Como nosotros usamos VITE para crear el proyecto **tenemos que configurar jest** manualmente para hacer las pruebas.

Lo primero que tenemos que hacer es **instalarlo**, para ello usamos el siguiente comando en nuestra terminal, esto agregara jest como dependencia de desarrollo en nuestro *package.json*:

```
npm install --save-dev jest
````

g1

#### Añadiendo script de jest 🔵

Seguido de haber instalado el paquete, en nestro *package.json*, agregaremos:

**a)** Si queremos ejecutar un archivo de prueba solamente.

```
{
  "scripts": {
    "test": "jest"
  }
}
````

**b)** Si queremos estar ejecutando continuamente todas las pruebas cada que hagamos un cambio, o solamente estar al pendiente de una prueba cada qeu se hagan cambios:

```
{
  "scripts": {
    "test": "jest --watchAll"
  }
}
````

En mi caso usare la segunda opción.

g2

Ya podemos ejecutar jest en la terminal usando el comando:

```
npm run test
```

Pero sorpresa, aun no tenemos pruebas que ejecutar.

#### Estructura de carpetas🔵

Puedes acomodar tus archivos de test como quieras, yo lo hare de la siguiente forma:

1.- En la raiz de tu proyecto crea una carpeta que se llame **tests**, esta carpeta sera un espejo de tu carpeta *src*, y contendra la misma estructura.

A diferencia que los archivos tendran una extension **.test.js** o **.test.jsx**

i4

#### Agregando dependencia para ayudarnos con los comandos de Jest🔵

Instalaremos este paquete que nos ayudara a no tener que memorizar todos los comandos.

```
npm install --save-dev @types/jest
```

g3

#### Solucionando error 🔵

i5

Este error sucede porque React usa babel, para resolverlo tenemos que hacer lo siguiente:

1.- Instalar un nuevo paquete:

```
npm install --save-dev babel-jest @babel/core @babel/preset-env
```

2.-Crear un archivo en la raiz del proyecto llamado *babel.config.js* y dentro el siguiente codigo:

```
module.exports = {
  presets: [['@babel/preset-env', {targets: {node: 'current'}}]],
};
```

g4

#### Estructura de una prueba 🔵

Despues de realizar todos los pasos anteriores, ya podemos escribir nuestras pruebas.

i6

**🚨Recuerda no confiar en una prueba que no has visto fallar🚨**

Ejecutamos para ver como nuestra prueba falla:

```
npm run test
```

Reescribimos el codigo para que pase la prueba y guardamos los cambios, automaticamente se ejecutara la prueba gracias a la configuracion que hicimos con *jest --watchAll*.

i7

i8

Listo ya puedes escribir tus pruebas en React :).

#### En este blog aprendimos a como integrar pruebas a nuestro proyecto de React y como configurar jest para que funcione correctamente. 🚀

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
