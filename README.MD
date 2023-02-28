# Repositorio para reto final del curso de GitFlow
RETO GIT FLOW


Ruta del repo: https://github.com/degonzalezuy/PruebaGitFlow
Link para clonar: https://github.com/degonzalezuy/PruebaGitFlow.git

Comandos desde host local.
Iniciando repo
git init
echo "# Repositorio para reto final del curso de GitFlow" >> README.MD
git add .
git commit -m "Primer commit, creación página principal"
git branch -M main
git remote add origin https://github.com/degonzalezuy/PruebaGitFlow.git
git push -u origin main

Se envía el primer commit realizado en la rama “master” con el README.MD y el index.html principal.


Creación de rama ‘develop’
git checkout -b develop

Creación de ramas de función
git checkout -b feat/0001-hu01-dg develop
Se crea archivo sitiohu.html para poder commitear una acción.

git checkout -b feat/0002-hu02-dg develop
Se crea archivo sitiohu2.html para poder commitear una acción.

Agregando modificaciones de las ramas funcionales feat/0001-hu01-dg y feat/0002-hu02-dg
git merge feat/0001-hu01-dg
git merge feat/0002-hu02-dg

Me cambio a main y realizo un merge en main para luego hacer un push.
git checkout main
git push

Creo las ramas de BugsFix
Creación de rama ‘release’
git checkout -b release

Descargo la última actualización desde la main de el repositorio remoto 
git branch --set-upstream-to=origin/main release
git pull


Creo las ramas de BugsFix
git checkout -b BugFix/2222-hu01-dg
git checkout -b BugFix/1111-hu02-dg

Descargo proyecto
git fetch
Modifico los archivos aplicando mismo mecanismo para ambos bugs.
Verifico con git status las modificaciones realizadas, luego confirmo y comiteo.

git add .
git commit -m
En rama BugFix/2222-hu01-dg
git commit -m "Se realizan cambios en sitiou.html"
En rama BugFix/1111-hu02-dg
git commit -m "Se actualiza archivo sitiohu2.html"

Combinando cambios de las ramas de BugFix a Release
git merge BugFix/2222-hu01-dg
git merge BugFix/1111-hu02-dg


Lo mismo lo actualizamos en la rama Develop.
git merge BugFix/2222-hu01-dg
git merge BugFix/1111-hu02-dg

En la rama principal se realizar merge desde la rama release
git checkout main
git merge release

git push para actualizar el repositorio remoto.
 
Creando ramas HotFix
git checkout -b HotFix/2222-hu01-dg
git checkout HotFix/1111-hu02-dg main

Descargo repositorio a la rama
git branch --set-upstream-to=origin/main HotFix/2222-hu01-dg
git pull

Moficiación confirmada en la primer rama
git commit -m "Se agrega archivo css que se había olvidado"

Se realizan modificaciones y se suben a la rama main y develop respectivamente.
git checkout develop
git merge HotFix/2222-hu01-dg
git merge HotFix/1111-hu02-dg
git checkout main
git merge HotFix/1111-hu02-dg
git merge HotFix/2222-hu01-dg
 
Se suben las ramas de HotFix creadas localmente al repositorio
git checkout  HotFix/222-hu01-dg
git push origin HotFix/2222-hu01-dg

 git checkout  HotFix/1111-hu02-dg
 git push origin HotFix/1111-hu02-dg

Se realizan correcciones en la rama main y se sube el repo.

https://github.com/degonzalezuy/PruebaGitFlow
