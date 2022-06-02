+++
title = "Git y Github: Comandos básicos"
date = "2022-06-01"
+++

Muy bien, ahora que ya conocemos un poquito de teoria sobre como funciona Git y GitHub, comenzaremos a usar los comandos básicos...🐣

<!--more-->
Si ya tienes algo de experiencia te dejo el resumen de los comandos utilizados en este post:

Inicializar un repositorio en git

```git init```

Seleccionar todos los cambios que querramos versionar y añadirlos a *stage area*

```git add .```

Para ver los cambios que se han hecho en el proyecto, los cambios que ya se agregaron para subir al repo local, tanto como los que no se han agregado

```git status -s```

Añadir una descripción a los cambios que se subiran al repo local

```git commit -m "aqui tu descripcion"```

Subir los cambios al repositorio remoto 

```git push origin master```

Veremos cada comando mas adelante. 😉

- Omitiremos la instalación de Git, puedes descargarlo desde aquí [descarga Git](https://git-scm.com/downloads).

- Tambien omitiremos la creación de una cuenta en GitHub, puedes hacerlo desde aquí [GitHub](https://github.com/).
## Inicializando un nuevo repositorio 

Perfecto, ahora podemos iniciar con este mini taller, para ello, primeramente inicializaremos un repositorio local en nuestro proyecto.

1.- Nos dirigimos dentro de la carpeta de nuestro proyecto y abrimos git bash dando click derecho.

2.-Escribimos el comando:

```git init```

Nos deberia aparecer lo siguiente y se habra creado una carpeta *.git* por favor **no elimines esta carpeta**, ya que aquí se encuentrara guardado el historial de cambios de tu rpoyecto.
g1

## Creación del repositorio remoto

1.- Nos dirigimos a nuestro perfil en github, seleccionamos **Repositories** y seleccionamos **New** para crear un nuevo repositorio remoto en GitHub.

g2

2.- Te recomiendo que en el nombre del repositorio uses el mismo nombre que estas usando en tu proyecto, para que en un futuro no te confundas.
En mi caso mi proyecto se llama *practicandoGit* entonces este nombre le dare al repositorio remoto.

Por el momento no añadiremos un *readme* pero mas adelante podemos hacerlo, esto nos servira para describir nuestro proyecto.

Seleccionamos si queremos que nuestro repo sea publico o privado, en mi caso quiero que sea publico.

Y finalizamos dando click en **Create repository**.

Esto deberia aparecer en tu pantalla:

g3

## Conectar el repositorio local con el repo remoto de GitHub

Muy bien, hasta ahora tenemos nuestro repositorio local y uno remoto, lo que haremos ahora sera conectar estos dos.

1.- Abrimos git bash dentro de la carpeta de nuestro proyecto donde inicializamos un repo local.

2.- Conectamos el repo local con el repo remoto a traves del usando el siguiente comando que nos muestra.

g4

Listo ya tendremos conectados nuestro repo local, con nuestro repo remoto. 😉
## Git status

Creare unos archivos, y carpetas para que git reconozca que hay cambios en el proyecto.

Con el comando:

```git status``` 

Git nos muestra los cambios que hay en nuestro proyecto.

g5

Git nos dice que hay archivos que no estan siendo seguidos.

Para ver de forma mas resumida los cambios tambien podemos usar:

```git status -s```

## Selecionar los cambios que queremos versionar

Ahora bien, estos cambios que git no esta siguiendo, debemos pasarlos a *stage area*, podemos hacerlo seleccionando cada uno con:

```git add <nombre de tu archivo>```

O agregando todos los cambios:

```git add .```

Por lo pronto yo subire solo un cambio.

g6

Podemos observar que ahora git ya esta contemplando este archivo porque se puso en color verdesito. 🙂

## Subiendo los cambios al repo local

Muy bien ahora que tenemos nuestro cambio en el *stage area* vamos a subirlo a nuestro **repo local**, para ello lo añadiremos con una descripción.

Se recomienda que con tu descripción, se pueda entender que es lo que se hizo.

```git commit 'aqui tu descripcion del cambio'```

g7

Ahora nuestro cambio se encuentra en el historial de modificaciones del proyecto, tan solo en el repositorio local. 😦
## Subiendo los cambios al repo remoto de GitHub

Excelente, ahora solo nos queda subir estos cambios al repo remoto, para ello usaremos el comando:

```git push origin master```

g8

Listo, nuestros cambios ya estan en la nube, nuestros repos conectados y asi podemos seguir trabajando.

Esto es solo una parte de lo que es Git, y al trabajarlo con GitHub podemos hacer grandes cosas, seguiremos hablando más adelante sobre esto. 😉

#### Excelenteee, hoy vimos los comandos básicos de git, como conectar nuestro repositorio local con el remoto, y como subir nuestros cambios 🚀

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
