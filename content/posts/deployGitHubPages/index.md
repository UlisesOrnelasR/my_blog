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

En mi caso **modificaré** las líneas que dicen 'main' por 'master' porque es mi branch **default** en GitHub

![p1master](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/deployGithubPages/p1master.JPG?raw=true)

**Guarda** los cambios y súbelos a tu repositorio de GitHub.

Puedes observar en el repositorio del proyecto como ahora tenemos dos branches.

![p1action](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/deployGithubPages/p1action.JPG?raw=true)

Un branch llamado *gh-pages*, cada vez que hagamos un commit en el branch master, se **construirá automáticamente**
el proyecto de nuevo, actualizando esta rama que será la que utilizaremos para crear nuestra página.

![p1deploy](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/deployGithubPages/p1deploy.JPG?raw=true)

Si nos vamos a la pestaña **Actions** podemos observar el estado de la nuestra.

![p2workflow](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/deployGithubPages/p1workflow.JPG?raw=true)

## 2.- Activando GitHub Pages

Nos dirigimos a la pestaña de **Settings**.

Seleccionamos **Pages** y guardamos ese link, ese será nuestra ruta personal de este proyecto en particular.

![p2linkk](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/deployGithubPages/p2link.JPG?raw=true)

Lo **pegamos** en nuestro archivo **config.toml** en la línea que vemos a continuación.

![p2config](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/deployGithubPages/p2config.JPG?raw=true)

Guardamos los cambios. Volvemos a la pestaña de **Settings** en GitHub, luego vamos **Pages** de nuevo y
cambiamos estas dos opciones para que queden como a continuación y presionamos en **save**.

![p2root](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/deployGithubPages/p2root.JPG?raw=true)

## 3.- Deploy

Volvemos a nuestro proyecto y abrimos la terminal.

Subimos los cambios a GitHub al branch **master** y automáticamente se construirá nuestro proyecto.

![p3push](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/deployGithubPages/p3push.JPG?raw=true)

Podemos ver el estado de nuestro deploy en la pestaña **Actions** tardarán unos segundos en estar listas.

![p3action](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/deployGithubPages/p3action.JPG?raw=true)
![p3finish](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/deployGithubPages/p3finish.JPG?raw=true)

Cuando **estén en verde** vamos al link que guardamos anteriormente, que habíamos dicho que era nuestro link personal.
En mi caso es este [http://ulisesornelasr.github.io/my_webSite/](https://ulisesornelasr.github.io/my_webSite/), ya lo puedo pegar en una pestaña de mi navegador.

#### Listo, ya tenemos nuestro webSite desplegado en una página de **GitHub Pages!** 🚀

![p3listo](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/deployGithubPages/p3listo.JPG?raw=true)

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sigueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[Linkedin](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)