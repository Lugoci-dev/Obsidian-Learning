([[Commit]], [[reset]], [[config]], [[Ramas]], [[Tag]] )

(_Creación de un usuario: git [[config]]_)
```CMD
git config --global user.name "userName"
git config --global user.email "userName@gmail.com"
```
(_Para acceder a la información de las configuraciones_)
```CMD
git config --global -l
```

(_Creación de un nuevo repositorio en la carpeta de nuestro
proyecto_)
```CMD
git init
```

Comandos Necesarios: 
```CMD
git status
git status -s -b
```
_Muestra las carpetas y archivos de tu repositorio. Los que tienen modificaciones no registradas desde el ultimo commit(rojo) y las que si se encuentran registradas en el repositorio(verde) _

```CMD
git add .
git add -- .
git add fileName.tipe
git add *.png
git add file/
```
_Registra los archivos dentro de esa carpeta para darles seguimiento (envía al staged)_

```CMD
git add -u
//la bandera -u actualiza el repositorio

git add -A
```
Esta serie de comandos se utiliza cuando se renombra un archivo del repositorio sin utilizar los comandos de git. 


```CMD 
git checkout -- .

//Revierte unicamente los cambios realizados a este file.
git checkout -- README.md
```
_Devuelve nuestro proyecto hacia nuestro ultimo commit_

```CMD 
//Muestra los cambios de archivos modificados recientemente 
git diff

//Muestra los cambios de los archivoas enviados al staged
git diff --staged
```
Muestra las diferencias o los cambios realizados a nuestro código

(Creación de un [[Commit]]: git [[reset]])

[Para ignorar algún archivo o carpeta en el repositorio se crea el archivo .gitignore.]

