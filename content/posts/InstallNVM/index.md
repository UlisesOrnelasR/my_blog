+++
title = "Cómo instalar NVM(Node Version Manager) en windows"
date = "2022-05-25"
+++

A continuación te enseñaré como puedes tener y utilizar una u otra versión de **Node** en un mismo ambiente según sea tu necesidad.😉
<!--more-->
Para ello usaremos NVM, sin más preámbulo empecemos...

#### Antes de la instalación 🔴
- **Asegurarse no tener instalado node**
    *1.-* Abrir la terminal, o la PowerShell de Windows y escribir `node --version`
    Así debería aparecer:
    n1
    *2.-* Para confirmar puedes ir a tu directorio `C:\Program Files` y `C:\Program Files (x86)` y verificar que no exista ningún directorio `nodejs` dentro de estas carpetas, en caso de que si exista, **eliminalo**.

#### Instalación 🟢

*1.-* Dirigete al siguiente link **[NVM para Windows](https://github.com/coreybutler/nvm-windows)**, baja a la parte del readme y da **click** en *Download Now!*.

*2.-* Nos llevará al apartado de *Releases* de GitHub, en la sección de *Assets* **descargamos** el archivo `nvm-setup.zip`.
g1

*3.-* Descomprimimos el archivo
g2
*4.-* Ejecutamos como administrador, aceptamos la licencia.

*5.-* Verificamos que se esté instalando en la siguiente ruta `C:\Program Files\nodejs`

*6.-* Damos **click** en *Finish*
g3

Listo ya tendremos instalado Node Version Manager‼

#### Actualizar la version de NVM 🔵
Para actualizar la versión de NVM **descarga** el archivo `nvm-update.zip` y sigue el mismo proceso que en la instalación.
n3

#### Usando NVM📚

 Ahora que ya tenemos instalado NVM, es momento de utilizarlo. 
 En estos instantes no tenemos ninguna versión de *Node* instalada.

 - Abrimos la terminal o la PowerShell de Windows y escribimos `nvm`, esto nos mostrada los distintos **comandos** que podemos usar.
  g4

**Instalando una versión de Node**📁

 - Para ver la lista de las *versiones* de Node disponibles escribimos `nvm list available`
  g5
 -Para instalar alguna versión usaremos el comando `nvm install <version>` por ejemplo instalaré la versión más reciente `nvm install 18.2.0`.
 g6

 - Si ahora ejecutamos el comando `nvm use 18.2.0`, nos debería aparecer esto.
  n4

**Cambiando a otra versión**💱
- Primeramente observo la lista de versiones con `nvm list available`.
- Descargare la nueva versión que quiero usar con el comando `nvm install 16.15.0`
n5
- Y finalmente *cambio* a la nueva versión de Node que descargue `nvm use 16.15.0`.
g7

**Desinstalando una versión**🗑
- Para desinstalar una versión usaremos el comando `nvm uninstall 18.2.0` aquí tu pondrás la versión de Node que desees *eliminar*.
- g8
  
#### *Listo ahora ya habras instalado el manejador de versiones de Node, ademas de usarlo ✅ :D*
*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sigueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[Linkedin](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
