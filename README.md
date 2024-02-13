Crear una carpeta
cd
mkdir practica_evaluble
Cambiar de master a main
git branch -M main
git init

Crear dos archivos
echo “Creo Documento1”>documento1.txt
cat documento1.txt
git add.
git commit -m “Añado documento1”
git log –oneline

Escribo otra línea en el documento1.txt
echo “Escribo otra línea”>>documento1.txt
git add .
git commit -m “Realizo commit”
git log –oneline

Volver a la situación anterior, se pone el anterior
git reset –hard fb1b979

Revertir un commit
git revert HEAD

Conectar un repositorio remoto público en GitHub
git remote add origin “url del github creado”
git remote -v
git push -u origin master

Crear una rama 
git checkout -b mirama
echo “Creo rama1”>rama1,txt
git add .
git commit -m "Añado archivos en la rama mirama"
git push origin mirama → sube la rama mirama al repositorio remoto

Fusionar la rama mirama con la rama main, despues de hacer merge se borra la rama
git checkout master
git merge mirama
git branch → comprobar las ramas que hay
Borrar la rama mirama
git branch -d mirama
git branch → comprobar que se ha borrado
// git branch -v -a
-a incluye también las ramas remotas
-v incluye el mensaje commit del HEAD de la rama
Sincroniza los cambios con el repositorio remoto
git pull origin master
git push origin master

Crear un tag
git tag -a V1 -m “Creo una etiqueta V1”
git push origin V1 → Envía la etiqueta al repositorio remoto
git show V1 → ver información de la etiqueta

Hacer un clonado del repositorio remoto practica_evaluable a uno nuevo llamado practica_evaluable2
git clone “url del repositorio practica_evaluable” practica_evaluable2

Para añadir cambios a un documento por ejemplo el documento2.txt, validar y subir al repositorio remoto
git add documento2.txt
git commit -m “Realizo cambios en el documento2.txt”
git push origin master

Resolver un conflicto
git checkout master
git branch
git merge mirama master
cat documento2.txt
nano documento2.txt
git add .4
git commit -m “Resolver conflicto”
git log –oneline

README
git push origin master →  envía tus cambios locales al repositorio remoto
git pull origin master → trae los cambios remotos al repositorio local

