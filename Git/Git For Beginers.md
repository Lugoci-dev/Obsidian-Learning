(_Creación de un usuario:_)
```CMD
"git config --global user.name "userName""
"git config --global user.email "userName@gmail.com""
```
(_Para acceder a la información del registro de usuario_)
```CMD
"git config --global -e"
```

(_Creación de un nuevo repositorio en la carpeta de nuestro
proyecto_)
```CMD
"git init"
```

Comandos Necesario:
```CMD
"git status"  
```
_Muestra las carpetas y archivos de tu repositorio. Los que se no han registrado o han tenido modificaciones desde el ultimo commit(rojo) y las q si (verde) _

```CMD
"git add ."
"git add fileName.tipe"
```
_Registra los archivos dentro de esa carpeta para darles seguimiento (envía al stage) _
```CMD 
git checkout -- .
```
_Devuelve nuestro proyecto hacia nuestro ultimo commit_

(Creación de un [[Commit]])


