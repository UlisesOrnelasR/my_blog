+++
title = "Integrar Testing a tu proyecto de React JS con Jest y React Testing Library"
date = "2022-06-22"
+++

En esta publicación veremos como integrar pruebas de unidad a nuestro proyecto de React JS, utilizando [JEST](https://jestjs.io/)🃏 y [React Testing Library](https://testing-library.com/)🐙...

<!--more-->
## Unit Testing

Las pruebas de unidad son **muy importantes** en un proyecto, tanto asi, que decía mi mentor [CarloGilmar](https://twitter.com/carlogilmar) durante mi travesía en Launch X "Las pruebas no son negociables, ¿Como compruebas que tu proyecto realmente funciona?-Con pruebas".

Tristemente tenemos una cultura donde se cree que las pruebas son una pérdida de tiempo, que tardaríamos incluso más del doble en realizar una funcionalidad, pero **esto no es asi**, este tiempo en que realizaríamos las pruebas nos lo tomaría en corregir los posibles bugs que tengamos sin hacer pruebas.

No obstante, realizar pruebas no quiere decir que estemos exentos de tener errores en nuestra aplicación, **somos humanos y comentemos errores**.

Gracias a las pruebas podemos corregir bugs o errores, antes de desplegar la aplicación en producción, además de que agregan **calidad** a nuestro software.

## Pruebas Unitarias

Las pruebas unitarias están orientadas a pequeñas funcionalidades de un componente en específico.

![i2](https://user-images.githubusercontent.com/99143567/175169220-acba6646-6cb1-4523-86b7-3730ca53ddcc.png)

## Pruebas de Integración

Las pruebas de integración están orientadas a probar como interactúan los componentes entre sí, a probar su comportamiento.

![i3](https://user-images.githubusercontent.com/99143567/175169265-86143481-df6f-4f20-8ea4-b94fcd9ebff3.png)

## Integrar Testing a tu proyecto de React js

![i1](https://user-images.githubusercontent.com/99143567/175169273-bfead16f-9cf3-4ecc-b911-dc716c0feec2.png)

#### Instalando jest🔵

Como nosotros usamos VITE para crear el proyecto **tenemos que configurar jest** manualmente para hacer las pruebas.

Lo primero que tenemos que hacer es **instalarlo**, para ello usamos el siguiente comando en nuestra terminal, esto agregara jest como dependencia de desarrollo en nuestro *package.json*:

```
npm install --save-dev jest
```

![g1](https://user-images.githubusercontent.com/99143567/175169289-d6e2139b-592d-44c2-a488-804e10bcad93.gif)

#### Añadiendo script de jest 🔵

Seguido de haber instalado el paquete, en nestro *package.json*, agregaremos:

**a)** Si queremos ejecutar un archivo de prueba solamente.

```
{
  "scripts": {
    "test": "jest"
  }
}
```

**b)** Si queremos estar ejecutando continuamente todas las pruebas cada que hagamos un cambio, o solamente estar al pendiente de una prueba cada qeu se hagan cambios:

```
{
  "scripts": {
    "test": "jest --watchAll"
  }
}
```

En mi caso usare la segunda opción.

![g2](https://user-images.githubusercontent.com/99143567/175169473-aa144ae5-663b-4ae1-861d-dfd6f3ad5cc1.gif)

Ya podemos ejecutar jest en la terminal usando el comando:

```
npm run test
```

Pero sorpresa, aun no tenemos pruebas que ejecutar.

#### Estructura de carpetas🔵

Puedes acomodar tus archivos de test como quieras, yo lo hare de la siguiente forma:

1.- En la raíz de tu proyecto crea una carpeta que se llame **tests**, esta carpeta será un espejo de tu carpeta *src*, y contendrá la misma estructura.

A diferencia que los archivos tendrán una extensión **.test.js** o **.test.jsx**

![i4](https://user-images.githubusercontent.com/99143567/175169592-b50c4524-6806-4e3c-99f7-f01328c024e0.JPG)

#### Agregando dependencia para ayudarnos con los comandos de Jest🔵

Instalaremos este paquete que nos ayudara a no tener que memorizar todos los comandos.

```
npm install --save-dev @types/jest
```

![g3](https://user-images.githubusercontent.com/99143567/175169605-f3d64b0b-91fb-4037-981b-878e60d2e2ba.gif)

#### Confiuraciones adicionales y añadiendo React Testing Library para testear el DOM🐙🔵

🛸Añadimos la dependencia de React Testing Library a nuestro proyecto:

```
npm install --save-dev @testing-library/react
```

🛸Añadimos la siguiente dependencia:
```
npm install jest-environment-jsdom
```

🛸Crear un archivo en la raiz del proyecto llamado **jest.config.js** y dentro el siguiente codigo:

```
module.exports = {
    testEnvironment: 'jest-environment-jsdom',
    setupFiles: ['./jest.setup.js']
}
```

🛸Añadimos la siguiente dependencia:

```
npm install whatwg-fetch --save
```

🛸Creamos un archivo en la raíz del proyecto llamado **jest.setup.js** y dentro el siguiente código:

```
import 'whatwg-fetch';
```

🛸 Instalamos estos paquetes necesarios para que no haya conflictos con React y Babel:

```
npm install --save-dev @babel/preset-react
```

```
npm install --save-dev babel-jest @babel/core @babel/preset-env
```

🛸 Crear un archivo en la raíz del proyecto llamado **babel.config.js** y dentro el siguiente código:

```
module.exports = {
  presets: [
    ['@babel/preset-env', { targets: { esmodules: true } }],
    ['@babel/preset-react', {runtime: 'automatic'}]
  ],
};
```

Al final de todas las configuraciones, así deberían quedar los archivos.

i0

#### Estructura de una prueba 🔵

Después de realizar todos los pasos anteriores, ya podemos escribir nuestras pruebas.

![i6](https://user-images.githubusercontent.com/99143567/175169644-857df844-1f84-44d6-af46-9f0078d9d346.JPG)

**🚨Recuerda no confiar en una prueba que no has visto fallar🚨**

Ejecutamos para ver como nuestra prueba falla:

```
npm run test
```

Reescribimos el código para que pase la prueba y guardamos los cambios, automáticamente se ejecutara la prueba gracias a la configuración que hicimos con *jest --watchAll*.

![i7](https://user-images.githubusercontent.com/99143567/175169672-132a8848-4ccd-42f4-af53-32526e61b219.JPG)

![i8](https://user-images.githubusercontent.com/99143567/175169679-5ad5cc47-8ba4-4233-80c7-07f885197684.JPG)

Listo ya puedes escribir tus pruebas en React :).

#### En este blog aprendimos a como integrar pruebas a nuestro proyecto de React y como configurar jest para que funcione correctamente. 🚀

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
