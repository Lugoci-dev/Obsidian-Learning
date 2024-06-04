Para hacer un push a un repositorio en git Hub debes crearlo:

```CMD
git remote add origin https://github.com/Lugoci-dev/udemy-heroes.git
```
_debes añadir el origen a tu repositorio en git_

Para mostrar información de esto podemos ejecutar el siguiente comando:
```CMD
git remote
git remote -v
```
y para hacer el push:
```CMD
git push -u origin main
```

Para subir los tags, debe hacerse de forma manual.
```CMD
git push --tags
```
y para descargar los cambios
```CMD
git pull
git pull origin master
```

Para clonar un repositorio completo debes copiar el link necesario para esto desde el GitHub y ejecutar el siguiente comando:
```CMD
git clone https://github.com/Lugoci-dev/udemy-heroes.git
```
_Esto creara una carpeta del repositorio completo en tu directorio_

Si quieres que se añada dentro de alguna carpeta:
```CMD
git clone https://github.com/Lugoci-dev/udemy-heroes.git nombreNewFolder
```

Una forma segura de ver los cambios realizados al repositorio remoto es utilizando el comando:
```CMD
git fetch
```
funciona igual que el git pull, pero no realiza ningún Merge automático, sino que solo muestra los cambios como cuando hay conflictos