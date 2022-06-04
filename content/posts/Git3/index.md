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

i2

g2

**--staged**

Si accidentalmente subiste cambio a la etapa de stage, puedes descartarlo si así lo deseas, es decir, lo elimina del `stage area` pero deja intactas las modificaciones que le hiciste.

```
git restore --staged <file>
```

i1

g1

**--source**

Si lo que queremos es restaurar un archivo a como estaba en un commit del pasado, lo que debemos hacer es usar el siguiente comando:

```
git restore --source <id commit> <file>
```

Nota que debemos especificar el commit, y el archivo que queremos restaurar a esa versión.

i3

g3

#### Enhorabuena ahora ya sabes más comandos de git, conforme avancemos, seguiremos usando estos comandos e iremos conociendo más. 🚀

*Deseando que te encuentres bien, te saluda Ulises🤵...*
*Sígueme en mis redes*
[GitHub](https://github.com/UlisesOrnelasR)
[LinkedIn](https://www.linkedin.com/in/ulises-ornelas/)
[Twitter](https://twitter.com/UlisesOrnelass)
