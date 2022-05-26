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
    ![n1](https://user-images.githubusercontent.com/99143567/170433046-ae3cdd00-51df-4e55-b6ca-5c9470cf3122.JPG)

    *2.-* Para confirmar puedes ir a tu directorio `C:\Program Files` y `C:\Program Files (x86)` y verificar que no exista ningún directorio `nodejs` dentro de estas carpetas, en caso de que si exista, **eliminalo**.

#### Instalación 🟢

*1.-* Dirigete al siguiente link **[NVM para Windows](https://github.com/coreybutler/nvm-windows)**, baja a la parte del readme y da **click** en *Download Now!*.

*2.-* Nos llevará al apartado de *Releases* de GitHub, en la sección de *Assets* **descargamos** el archivo `nvm-setup.zip`.
![g1](https://user-images.githubusercontent.com/99143567/170433143-d979003b-90a5-49e6-9557-0523bfb5c1d7.gif)


*3.-* Descomprimimos el archivo
![g2](https://user-images.githubusercontent.com/99143567/170433192-3cd561d4-7fa0-4382-a7a2-847a736cf3b5.gif)

*4.-* Ejecutamos como administrador, aceptamos la licencia.

*5.-* Verificamos que se esté instalando en la siguiente ruta `C:\Program Files\nodejs`

*6.-* Damos **click** en *Finish*
![g3](https://user-images.githubusercontent.com/99143567/170433215-ec256519-226e-46ba-b3bc-945654a666f2.gif)

Listo ya tendremos instalado Node Version Manager‼

#### Actualizar la version de NVM 🔵
Para actualizar la versión de NVM **descarga** el archivo `nvm-update.zip` y sigue el mismo proceso que en la instalación.
![n3](https://user-images.githubusercontent.com/99143567/170433234-b31eaed4-b3ba-41f8-afe0-e9ac7921dd33.JPG)


#### Usando NVM📚

 Ahora que ya tenemos instalado NVM, es momento de utilizarlo. 
 En estos instantes no tenemos ninguna versión de *Node* instalada.

 - Abrimos la terminal o la PowerShell de Windows y escribimos `nvm`, esto nos mostrada los distintos **comandos** que podemos usar.
  ![n4](https://user-images.githubusercontent.com/99143567/170433258-2fe6f2bf-c61b-4a71-84f6-d5ab108513a0.JPG)


**Instalando una versión de Node**📁

 - Para ver la lista de las *versiones* de Node disponibles escribimos `nvm list available`
  ![g5](https://user-images.githubusercontent.com/99143567/170433326-f04b9580-fd8f-4e70-9893-d1c7c260dd48.gif)


 -Para instalar alguna versión usaremos el comando `nvm install <version>` por ejemplo instalaré la versión más reciente `nvm install 18.2.0`.
 ![g6](https://user-images.githubusercontent.com/99143567/170433359-d02ce808-b3ea-479d-b045-636b4b31ce99.gif)


 - Si ahora ejecutamos el comando `nvm use 18.2.0`, nos debería aparecer esto.
  ![n4](https://user-images.githubusercontent.com/99143567/170433454-817b6ea8-aaf5-40c6-8eef-78cbf9cf51e5.JPG)


**Cambiando a otra versión**💱
- Primeramente observo la lista de versiones con `nvm list available`.
- Descargare la nueva versión que quiero usar con el comando `nvm install 16.15.0`
![n5](https://user-images.githubusercontent.com/99143567/170433485-ee966d2d-5308-430b-b9d4-09f42c998f08.JPG)

- Y finalmente *cambio* a la nueva versión de Node que descargue `nvm use 16.15.0`.
![g7](https://user-images.githubusercontent.com/99143567/170433524-c33a10ce-f621-4c82-95da-a31394bb1b50.gif)


**Desinstalando una versión**🗑
- Para desinstalar una versión usaremos el comando `nvm uninstall 18.2.0` aquí tu pondrás la versión de Node que desees *eliminar*.
![g8](https://user-images.githubusercontent.com/99143567/170433547-1d97a18c-5e7c-4ec9-802e-398a2fa1936e.gif)

#### *Listo ahora ya habras instalado el manejador de versiones de Node, ademas de usarlo ✅ :D*
*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sigueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[Linkedin](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
