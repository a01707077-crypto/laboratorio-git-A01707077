Mi Cheatsheet 

Guia: 

**TEMA 1= La Terminal (Para no andar perdida)**
Antes de mover cualquier cosa en Git, siempre hay que saber responder las tres preguntas básicas:
`pwd` (¿Dónde estoy?): Me da la ruta completa de la carpeta en la que estoy parado. Si me sale un error raro, casi seguro es porque no estoy en la carpeta correcta.
 `ls` (¿Qué hay aquí?): Lista todos los archivos y carpetas de donde estoy parado.
`cd <nombre-carpeta>` (¿A dónde voy?): Me entra a una carpeta.
  `cd ..` -> Sube un nivel (se regresa una carpeta atrás).
  `cd ../..` -> Se regresa dos niveles de golpe.
  `cd ~` -> Te regresa a la carpeta raíz de tu usuario por si te perdiste feo.
 `clear`: Limpia la pantalla para no ver tanto texto amontonado.

**TEMA 2= El Ciclo de Git (Toma de fotos y control)**
`git status`: Me dice en qué estado están mis archivos (si hay cambios sin guardar, si están listos para la foto o si no los está rastreando). Hay que usarlo a cada rato.
`git add <archivo>`: Mete un archivo a la "zona de preparación". Es como juntar a las personas y acomodarlas antes de tomar la foto.
  `git add .` -> Acomoda todos los archivos modificados de un jalón.
`git commit -m "Mensaje directo en presente"`: Toma la foto (guarda la versión en el historial).
  Versión limpia:* `git log --oneline` te lo muestra en una sola línea por commit, mucho más fácil de leer.


**TEMA 3= Trabajo en Equipo (Sincronizar con GitHub)**

`git pull`: **Lo primero que se hace al abrir VSCODE!! si voy a trabajar en equipo, ya que baja los cambios que mis compañeros subieron al repositorio en GitHub.
`git push`: Sube mis commits locales al repositorio remoto en GitHub para que mi equipo los vea.

**TEMA 4=  Comparar Cambios**
`git diff`: Muestra exactamente qué líneas cambié en mis archivos antes de hacer `git add` (compara mi trabajo actual con la zona de preparación).
`git diff --staged`: Muestra lo que ya preparé con `git add` comparado con el último commit. Sirve para revisar qué se va a ir en la foto antes de hacer el commit.

**TEMA 5= Deshacer y corregir errores**

 `git restore <archivo>`:Descarta todos los cambios que le hice al archivo desde el último commit y los borra por completo. Sirve también para recuperar un archivo si lo borré por accidente.
`git restore --staged <archivo>`: Si metí un archivo al `git add` por error pero no quiero perder el código que escribí, este comando lo saca de la zona de preparación y me deja conservar mi trabajo intacto.
`git commit --amend -m "Nuevo mensaje"`: Sirve si la regué escribiendo el mensaje del último commit (por ejemplo, si puse `"cambios"`)
  *  Solo usar si NO he hecho `git push`. Si ya lo subí a GitHub, no se toca.
