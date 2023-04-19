+++
title = "Git: Comandos (git restore)"
date = "2022-04-17"
+++

Si necesitas deshacer algún cambio en Git, en este post encontrarás algunos comandos útiles que pueden ayudarte. Es importante tener en cuenta que cada comando se usa para una tarea específica...🐤

<!--more-->

## Git restore

Si realizaste modificaciones a un archivo y deseas deshacerlas antes de subirlo al _stage area_, puedes usar el comando:

```
git restore <file>
```

![i2](https://user-images.githubusercontent.com/99143567/172026771-4ecce1b8-12a1-420d-9d24-cc249c956440.png)

![g2](https://user-images.githubusercontent.com/99143567/172026776-048306a0-5bf7-48b4-a451-613e0bcb47a5.gif)

**--staged**

Si accidentalmente agregaste cambios al _stage area_, puedes descartarlos con el siguiente comando. Esto eliminará los cambios del stage area, pero dejará intactas las modificaciones que le hiciste al archivo.

```
git restore --staged <file>
```

![i1](https://user-images.githubusercontent.com/99143567/172026785-33e1e1a8-b357-448a-81ae-32a75f6cbb45.png)

![g1](https://user-images.githubusercontent.com/99143567/172026790-f9df0151-b9a9-4aeb-99ad-00ea35b10980.gif)

**--source**

Si deseas restaurar un archivo a como estaba en un commit pasado, usa el siguiente comando:

```
git restore --source <commit_id> <file>
```

Asegúrate de especificar el commit y el archivo que deseas restaurar a esa versión.

![i3](https://user-images.githubusercontent.com/99143567/172026793-420be507-604a-432f-a217-b9b9b450e8fc.png)

![g3](https://user-images.githubusercontent.com/99143567/172026794-9d693e7c-d35b-4f0f-a033-ce4829a3fecf.gif)

#### ¡Felicidades, ahora sabes más comandos de Git! Conforme avancemos, seguiremos usando estos comandos y aprendiendo más. 🚀

_Deseando que te encuentres bien, te saluda Ulises🤵..._
_Sígueme en mis redes_
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
