+++
title = "Cómo crear un sitio web con Go Hugo"
date = "2022-04-25"
+++

Go Hugo es el framework más rápido del mundo para crear sitios web, aquí te enseñaré como tú puedes hacerlo.
<!--more-->
A continuación te contaré de mi experiencia realizando un sitio web con GoHugo mientras te explico como puedes hacerlo paso a paso.

## 1.- Instalación de GoHugo

Primero necesitamos instalar Hugo, esto dependerá del sistema operativo que estés manejando, para ello te dejaré el link a la documentación para instalarlo. → [Install Hugo](https://gohugo.io/getting-started/installing/)

En mi caso tengo **Windows** y uso [Chocolatey](https://chocolatey.org/) para la administración de paquetes así que usaré este comando en la PowerShell para la instalación de Hugo:

```texto
choco install hugo -confirm
```

![install](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/installHugo.jpg?raw=true)

Para confirmar que se instaló correctamente escribimos el siguiente comando y presionamos **enter** para ejecutarlo:

```texto
hugo version
```

Nos deberá aparecer lo siguiente, esto significa que se instaló correctamente.

![hugoVersion](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/hugoVersion.JPG?raw=true)

## 2.- Creación del static website

Ahora que verificamos que instalamos correctamente Hugo, crearemos el sitio, para ello nos ubicaremos en la carpeta que vamos a querer que se cree nuestro proyecto y desde **esta dirección que escogimos ejecutaremos nuestra terminal.**
En mi caso yo escogí esta ubicación:

![p2directorio](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/paso2directorio.JPG?raw=true)

![p2terminal](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/paso2terminal.JPG?raw=true)

Escribimos el siguiente comando y presionamos **enter** para ejecutarlo:

```texto
hugo new site my_webSite
```

![p2new](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/pas2new.JPG?raw=true)

Nos deberá aparecer la siguiente carpeta creada en la dirección que abrimos la terminal. Yo escogí como nombre del proyecto **my_webSite**, pero tú puedes escoger el que desees.

![P2newww](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p2new.JPG?raw=true)

La carpeta creada contendrá los siguientes archivos necesarios para el proyecto.

![P2newSitee](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p2mysite.JPG?raw=true)

## Crea un repositorio de GitHub para el proyecto

Para hacer esto, primero tenemos que inicializar git.

Abre la terminal **en la carpeta de tu proyecto** y **ejecuta** el siguiente comando, nos deberá aparecer lo siguiente:

![p2git](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p2git.JPG?raw=true)

```texto
git init
```

**Crea un repo** en GitHub con el nombre que tú quieras, en mi caso escogí "my_webSite"

![p2crrepo](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p2crerepo.JPG?raw=true)

Obtenemos la liga de nuestro repositorio, la pegamos en la terminal y ejecutamos el comando.
 **OJO** la terminal debe estar apuntando a la carpeta del proyecto.

![p2remote](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p2remote.JPG?raw=true)

Ahora ya tenemos **enlazado** nuestro repo local de git con el repo remoto de GitHub.

Ejecutamos los siguientes comando en la terminal **Uno por uno**.

Para ver los cambios:

```texto
git status -s
```

Para mandar los cambios a stage área usamos el comando:

```texto
git add .
```

Confirmamos los cambios:

```texto
git commit -m "first commit"
```

Hacemos un push para enlazar los cambios a nuestro repositorio remoto de GitHub:

```texto
git push origin master
```

Si **no te funcionó** este último comando posiblemente sea porque **tienes como rama principal 'main'**, en vez de 'master', en GitHub **modifica** tu rama predeterminada.

Al final de ejecutar estos comandos tu terminal se debería ver así:

![p2first](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p2first.JPG?raw=true)

Y nuestro repositorio de GitHub debería verse algo así:

![p2firstgithu](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p2firstgithub.JPG?raw=true)

**Nota**: Las demás carpetas no se subieron porque están vacías por el momento.

## 3.- Dale estilo a tu website

Ahora le daremos estilo a nuestro proyecto, esto será una plantilla de diseño predeterminada la cual podemos escoger
dando click aquí ⇾ [Hugo Themes](https://themes.gohugo.io/)

Nos llevará a la siguiente página:

 ![p3themes](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p3themes.JPG?raw=true)

 Escogemos el que más nos guste, en mi caso escogí este, **importante** ver que se nos proporciona con licencia MIT, esto para poder modificarlo libremente

 ![p3escoger](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p3escoger.JPG?raw=true)

 Damos click en **Descargar** y nos llevará a su repo de GitHub.

 Realizamos un **Fork** para poder modificar el diseño.

 ![p3descar](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p3descarga.JPG?raw=true)

 ![p3fork](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p3fork.JPG?raw=true)

 Ahora ya tenemos una **copia** del proyecto para poder modificarlo libremente.

 ![p3copia](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p3copia.JPG?raw=true)

Obtenemos este link del repo que acabas de crear. Para ello damos click en code y guardamos esa ruta.

![p3link](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p3link.JPG?raw=true)

Ahora nos posicionamos en **la carpeta de nuestro proyecto**

![P2newSitee](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p2mysite.JPG?raw=true)

Abrimos la terminal **desde esta dirección** y
ejecutamos este comando. **Quita las comillas y pon la ruta que guardaste**.

```texto
git submodule add 'tu ruta que guardaste aqui va' themes/minimal
```

Después de ejecutar el comando obtendremos el **contenido del repo que hicimos fork**, lo tendremos como **theme** de nuestro proyecto

![p3module](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p3submodule.JPG?raw=true)

Abrimos VScode y copiamos esto en el archivo **config.toml**

```texto
baseURL = "http://example.com/"
languageCode = "en-us"
title = "Minimal"
theme = "minimal"
disqusShortname = "username" # delete this to disable disqus comments
googleAnalytics = ""

[params]
    author = "Calin Tataru"
    description = "Personal blog theme powered by Hugo"
    githubUsername = "#"
    accent = "red"
    showBorder = true
    backgroundColor = "white"
    font = "Raleway" # should match the name on Google Fonts!
    highlight = true
    highlightStyle = "default"
    highlightLanguages = ["go", "haskell", "kotlin", "scala", "swift"]

[[menu.main]]
    url = "/"
    name = "Home"
    weight = 1

[[menu.main]]
    url = "/about/"
    name = "About"
    weight = 2

[[menu.main]]
    url = "/post/"
    name = "Posts"
    weight = 3

[[menu.main]]
    url = "/project/"
    name = "Projects"
    weight = 4

# Social icons to be shown on the right-hand side of the navigation bar.
# The "name" field should match the name of the icon in Font Awesome.
# The list of available icons can be found at http://fontawesome.io/icons.

[[menu.icon]]
    url = "mailto:me@example.com"
    name = "fas fa-envelope"
    weight = 1

[[menu.icon]]
    url = "https://github.com/username/"
    name = "fab fa-github"
    weight = 2

[[menu.icon]]
    url = "https://twitter.com/username/"
    name = "fab fa-twitter"
    weight = 3

[[menu.icon]]
    url = "https://www.linkedin.com/in/username/"
    name = "fab fa-linkedin"
    weight = 4

[[menu.icon]]
    url = "https://www.stackoverflow.com/username/"
    name = "fab fa-stack-overflow"
    weight = 5

```

Eliminamos la carpeta **content** del directorio raíz y pegamos la carpeta **content** que se encuentra en themes/minimal/exampleSite

![p3copy](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p3copy.JPG?raw=true)

Abrimos la terminal y ejecutamos el siguiente comando:

```texto
hugo server
```

Esperamos a que esté listo... Y abrimos en el navegador la dirección que nos da, en mi caso [localhost](http://localhost:1313/)

![p3server](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p3server.JPG?raw=true)

¡¡Listo!! ya poder observar nuestro webSite

![p3navegador](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p3navegador.JPG?raw=true)

Puedes modificar lo que tú quieras.

Para detener el servidor ⇾ **Ctrl + C**

Para volverlo a iniciar ejecuta en la terminal

```texto
hugo server
```

Por ejemplo para modificar el color nos dirigimos al archivo **config.toml** y cambiamos "red" por el que queramos, yo quiero azul
entonces escribo "blue".

![p3color](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p3color.JPG?raw=true)

![p3blue](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p3blue.JPG?raw=true)

## 4.- Crea contenido

Puedes hacer los cambios que quieras dentro de tu sitio web, por ejemplo te enseñaré a crear un post en tu sitio.

Primero debes crear un archivo.md con el nombre que quieras dentro de la carpeta content/post/, yo le pondre el nombre de **gatitos.md**
y pon el siguiente contenido

```texto
---
title: "Gatitos"
date: 2022-04-26
tags: ["Beaty", "Animals"] 
draft: false
---

## Los gatitos

No cabe duda que los gatos son una excelente compañía. Son perfectos cómplices para las personas que buscan un compañero con quien descansar, que le guste pasar momentos tranquilos y sobretodo aquel que busca un amigo fiel. Muchos artistas afirman que son la mejor compañía y, a veces, una gran inspiración.
```

**Recurda** iniciar tu servido o si ya lo tienes iniciados solo guarda los cambios en VsCode
Listo! Ya tienes tu primer post.

![p4post](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p4post.JPG?raw=true)

## 4.- Construye tu webSite

Muy bien, ahora tenemos nuestro sitio web al que le añadimos un tema, un post y lo configuramos...

Pero esto lo hicimos **localmente**, y esto es lo que hace Hugo, nos ayuda a construir un webSite de manera sencilla.
Para construir nuestro proyecto ejecutaremos el siguiente comando en nuestra terminal.

```texto
hugo -D
```

Este comando nos generará una carpeta **public** que solo contendrá archivos de tipo, html, css y js.

![p4constru](https://github.com/UlisesOrnelasR/assetsMy_blog/blob/master/HowToCreateSite/p4constru.JPG?raw=true)

Todo lo que hicimos anteriormente se resume en esta carpeta, la cual podemos subir a algún servidor o usar GitHub Pages.

**Pero esto lo veremos próximamente...**
