+++
title = "Git: Comandos (git restore)"
date = "2022-06-04"
+++

Si lo quieres ahora es deshacer algún cambio, lo veremos en este post con algunos comandos que te pueden ayudar, cabe destacar que cada comando se usa para una cosa distinta...🐤

<!--more-->
## Git restore

Si realizaste modificaciones a un archivo, antes de subirlo a *stage area* y resulta que ya no quieres esas modificaciones y quieres regresar el archivo como estaba, puedes usar el comando:

```
git restore <file>
```

![i2](https://user-images.githubusercontent.com/99143567/172026771-4ecce1b8-12a1-420d-9d24-cc249c956440.png)

![g2](https://user-images.githubusercontent.com/99143567/172026776-048306a0-5bf7-48b4-a451-613e0bcb47a5.gif)

**--staged**

Si accidentalmente subiste cambio a la etapa de stage, puedes descartarlo si así lo deseas, es decir, lo elimina del `stage area` pero deja intactas las modificaciones que le hiciste.

```
git restore --staged <file>
```

![i1](https://user-images.githubusercontent.com/99143567/172026785-33e1e1a8-b357-448a-81ae-32a75f6cbb45.png)

![g1](https://user-images.githubusercontent.com/99143567/172026790-f9df0151-b9a9-4aeb-99ad-00ea35b10980.gif)

**--source**

Si lo que queremos es restaurar un archivo a como estaba en un commit del pasado, lo que debemos hacer es usar el siguiente comando:

```
git restore --source <id commit> <file>
```

Nota que debemos especificar el commit, y el archivo que queremos restaurar a esa versión.

![i3](https://user-images.githubusercontent.com/99143567/172026793-420be507-604a-432f-a217-b9b9b450e8fc.png)

![g3](https://user-images.githubusercontent.com/99143567/172026794-9d693e7c-d35b-4f0f-a033-ce4829a3fecf.gif)

#### Enhorabuena ahora ya sabes más comandos de git, conforme avancemos, seguiremos usando estos comandos e iremos conociendo más. 🚀

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
