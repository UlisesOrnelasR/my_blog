+++
title = "3.- Solucionando conflictos entre el Testing y Eslint"
date = "2022-06-25"
+++

En este post resolveremos los conflictos que tenemos, ya que al añadir EsLint surgen inconvenientes...

<!--more-->
## Solucinando los conflictos
![i1](https://user-images.githubusercontent.com/99143567/175790322-074bd984-b91c-4a98-9260-367ac96eb332.png)

En este post iremos directo al grano...

#### Solucionando conflictos de EsLint y Jest

Primero solucionamos los conflictos que hay entre Jest y Eslint, para ello haremos lo siguiente:

🛸Instalamos el siguiente paquete:

```
npm install --dev eslint eslint-plugin-jest
```

🛸En el archivo **.eslintrc** añadimos el plugin de jest:

```
plugins: ['jest'],
```

🛸En la sección de reglas agregamos las siguientes:

```
rules: {
      'jest/no-disabled-tests': 'warn',
      'jest/no-focused-tests': 'error',
      'jest/no-identical-title': 'error',
      'jest/prefer-to-have-length': 'warn',
      'jest/valid-expect': 'error',
  }
```

🛸Marcamos como **true** las variables de entorno de Jest

```
env: {
    'jest/globals': true,
  }
```

#### Solucionando conflictos de EsLint y Testing Library

🛸Instalamos el siguiente paquete:

```
npm install --save-dev eslint-plugin-testing-library
```

🛸En el archivo **.eslintrc** añadimos el plugin de testing-library:

```
plugins: ['testing-library'],
```

🛸En la sección de reglas agregamos las siguientes:

```
rules: {
    'testing-library/await-async-query': 'error',
    'testing-library/no-await-sync-query': 'error',
    'testing-library/no-debugging-utils': 'warn',
    'testing-library/no-dom-import': 'off',
  }
```

#### Ejecutando plugin eslint-plugin-testing-library en archivos de prueba

Posiblemente al ejecutar **npm run lint** tengamos errores, para corregir estos errores haremos que *eslint-plugin-testing-library* solo se ejecute en los archivos de prueba.

🛸En el archivo **.eslintrc** en la sección de extends añadimos lo siguiente():

```
extends: [
    'standard',
    'plugin:prettier/recommended'
  ],
```

🛸En la sección de plugins agregamos *react-hooks*:

```
plugins: ['react-hooks'],
```

🛸Activamos que *eslint-plugin-testing-library* solo funcione en archivos de testing agregando lo siguiente en el archivo **.eslintrc** debajo de los plugins:

```
overrides: [
    {
      // 3) Now we enable eslint-plugin-testing-library rules or preset only for matching testing files!
      files: ['**/__tests__/**/*.[jt]s?(x)', '**/?(*.)+(spec|test).[jt]s?(x)'],
      extends: ['plugin:testing-library/react'],
    },
  ],
```

🛸Finalmente ejecutamos los siguientes comandos en la consola:

```
npm install eslint-plugin-prettier@latest --save-dev
```

```
npm install eslint-plugin-react-hooks@latest --save-dev
```

Listo finalmente podemos ejecutar nuestros comandos sin conflictos:

```
npm run format
```

```
npm run test
```

```
npm run lint
```

#### En este blog resolvimos los conflictos que había en el Testing y Eslint. 🚀

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
