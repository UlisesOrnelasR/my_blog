+++

title = "Deploy de un proyecto Vite en Github pages"

date = "2023-05-17"

+++

¡Hola a todos! En este artículo vamos a aprender cómo hacer deploy de un proyecto Vite en Github Pages 🚀💻. Sabemos que el proceso de deploy puede parecer intimidante, pero ¡no te preocupes! Vamos a guiarte paso a paso para que puedas publicar tu proyecto Vite y tenerlo en línea para que otros puedan verlo 👀. ¿Estás listo para compartir tu proyecto con el mundo? ¡Comencemos! 🎉

<!--more-->

## Pasos a seguir

1.- Primeramente ya debemos de tener nuestro repositorio en GitHub

image1

2.- Nos vamos a **Settings** del repositorio, luego en el apartado de **Pages** en la parte de source seleccionamos **GitHub Actions**.

image2

Esto nos permitira modificar el archivo Jekyll el cual GitHub utiliza para saber que hacer con las **actions**.

image3

3.- De este link `https://vitejs.dev/guide/static-deploy.html` fue extraido el contenido que vamos a sustituir en el archivo `jekyll-gh-pages.yml`:

```
# Simple workflow for deploying static content to GitHub Pages
name: Deploy static content to Pages

on:
  # Runs on pushes targeting the default branch
  push:
    branches: ['master']

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

# Sets the GITHUB_TOKEN permissions to allow deployment to GitHub Pages
permissions:
  contents: read
  pages: write
  id-token: write

# Allow one concurrent deployment
concurrency:
  group: 'pages'
  cancel-in-progress: true

jobs:
  # Single deploy job since we're just deploying
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3
      - name: Set up Node
        uses: actions/setup-node@v3
        with:
          node-version: 18
          cache: 'npm'
      - name: Install dependencies
        run: npm install
      - name: Build
        run: npm run build
      - name: Setup Pages
        uses: actions/configure-pages@v3
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v1
        with:
          # Upload dist repository
          path: './dist'
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v1

```

4.- Hacemos un commit del cambio con la siguiente descripción o con la que gustes `A workflow that installs dependencies and builds using npm is provided.`.

image4

5.- En nuestro proyecto abrimos una terminal y ejecutamos el siguiente comando para descargar los ultimos cambios que hicimos en el repositorio remoto:

```
git pull origin master
```

Despues de hacerlo ya deberia existir la carpeta `.github` en el repositorio local.

6.- Tenemos que agregar el **base** en el archivo `vite.config.js` y subimos el cambio al repositorio remoto haciendo un commit.

image5

7.- Nos dirijimos a la pestaña de **Actions** y verificamos que no haya ningun problema.

image6

Si hacemos click en `Visit site` nuestro sitio ya estara publicado.

image7

**Nota:** Si tienes alguna variable de entorno en el proyecto agrega un archivo `.env.production` con tu variable de entorno y subelo los cambios a GitHub con un commit.

image8

#### Listo ya tenemos nuestro proyecto listo para mostrarselo al mundo... 🌎🚀

_Deseando que te encuentres bien, te saluda Ulises🤵..._

_Sígueme en mis redes_

[GitHub](https://github.com/UlisesOrnelasR)

[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)

[Twitter](https://twitter.com/UlisesOrnelass)
