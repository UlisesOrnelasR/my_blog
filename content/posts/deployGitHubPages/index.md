+++
title = "Deploy de mi webSite con GitHub Pages"
date = "2022-04-26"
+++

En nuestro post anterior vimos como podíamos crear un webSite con Hugo, ahora veremos como hacer deploy de este sitio con GitHub Pages.
<!--more-->
Te mostraré paso por paso como debes hacerlo.

## 1.- Compilación de Hugo con un action de GitHub Pages

Usaremos esto para que cada vez que insertemos modificaciones o nuevo código a nuestro repositorio del proyecto, GitHub
Actions construirá el sitio automáticamente.

Creamos una carpeta llamada **.github** en el directorio raíz de nuestro proyecto, dentro de esta carpeta creamos otra que se llame **workflows**, por último dentro de esta carpeta creamos un archivo llamado **gh-pages.yml**, pega el siguiente código en este archivo:

```texto
name: github pages

on:
  push:
    branches:
      - main  # Set a branch to deploy
  pull_request:

jobs:
  deploy:
    runs-on: ubuntu-20.04
    steps:
      - uses: actions/checkout@v2
        with:
          submodules: true  # Fetch Hugo themes (true OR recursive)
          fetch-depth: 0    # Fetch all history for .GitInfo and .Lastmod

      - name: Setup Hugo
        uses: peaceiris/actions-hugo@v2
        with:
          hugo-version: 'latest'
          # extended: true

      - name: Build
        run: hugo --minify

      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        if: github.ref == 'refs/heads/main'
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./public
```

En mi caso modificaré las líneas que dicen 'main' por 'master' porque es mi branch default en GitHub

![p1master](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/deployGithubPages/p1master.JPG?raw=true)

**Guarda** los cambios y súbelos a tu repositorio de GitHub.

Puedes observar en el repositorio del poyecto como ahora tenemos dos branches

![p1action](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/deployGithubPages/p1action.JPG?raw=true)

![p1deploy](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/deployGithubPages/p1deploy.JPG?raw=true)

![p2workflow](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/deployGithubPages/p1workflow.JPG?raw=true)