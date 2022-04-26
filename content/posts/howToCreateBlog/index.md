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

![install](https://github.com/UlisesOrnelasR/assetsToBlogHowToSite/blob/master/installHugo.jpg?raw=true)

Para confirmar que se instaló correctamente escribimos el siguiente comando y presionamos **enter** para ejecutarlo:

```texto
hugo version
```

Nos deberá aparecer lo siguiente, esto significa que se instaló correctamente.

![hugoVersion](https://github.com/UlisesOrnelasR/assetsToBlogHowToSite/blob/master/hugoVersion.JPG?raw=true)

## 2.- Creación del static website

Ahora que verificamos que instalamos correctamente Hugo, crearemos el sitio, para ello nos ubicaremos en la carpeta que vamos a querer que se cree nuestro proyecto y desde **esta dirección que escogimos ejecutaremos nuestra terminal.**
En mi caso yo escogí esta ubicación:

![p2directorio](https://github.com/UlisesOrnelasR/assetsToBlogHowToSite/blob/master/paso2directorio.JPG?raw=true)

![p2terminal](https://github.com/UlisesOrnelasR/assetsToBlogHowToSite/blob/master/paso2terminal.JPG?raw=true)

Escribimos el siguiente comando y presionamos **enter** para ejecutarlo:

```texto
hugo new site my_webSite
```

![p2new](https://github.com/UlisesOrnelasR/assetsToBlogHowToSite/blob/master/pas2new.JPG?raw=true)

Nos deberá aparecer la siguiente carpeta creada en la dirección que abrimos la terminal. Yo escogí como nombre del proyecto **my_webSite**, pero tú puedes escoger el que desees.

![p2newww](https://github.com/UlisesOrnelasR/assetsToBlogHowToSite/blob/master/p2new.JPG?raw=true)

La carpeta creada contendrá los siguientes archivos necesarios para el proyecto.

![p2newSitee](https://github.com/UlisesOrnelasR/assetsToBlogHowToSite/blob/master/p2mysite.JPG?raw=true)
