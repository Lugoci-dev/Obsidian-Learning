El Stash es un área especial donde puedes guardar temporalmente cambios que no estás listo para comprometer en tu repositorio. Puedes utilizar el comando 
```CMD
git stash
git stahs save "mensaje"
```
 para guardar tus cambios en el Stash y luego recuperarlos más tarde con 
 ```CMD
 git stash pop
```
  _Esto es útil cuando necesitas cambiar de rama o hacer otras operaciones sin comprometer tus cambios actuales._

Para visualizar los Stash que tengas utiliza el comando
```CMD
git stash list
```


Una vez retomado el proyecto donde lo habíamos dejado, es buena practica eliminar el Stash( si no se hizo automáticamente). Para esto utilizamos el siguiente comando:
```CMD
git stash drop
```
_Hay comandos que te darán mas información sobre el Stash_
```CMD
git stash list --stat

git show stash
git show stash@{1}
```

Mas sobre el Stash:

Otro comando que podemos utilizar para restaurar los datos guardados en el Stash es el siguiente:
```CMD 
git stash apply
```
_este toma el ultimo Stash que se encuentre en la lista y lo restaura._
_También podemos hacer referencia a los demás elementos en esta lista:_
```CMD
git stash apply stash@{0}
git stash apply stash@{1}
```
_al igual que con cada elemento a borrar de esta lista:_
```CMD
git stash drop stash@{1}
```

Hay otros comandos que podrían ser útiles:

Keep índex
```CMD
git stash save --keep-index
```
_guarda todos los archivos menos los que están en el stage o escenario_

Include-untracked
```CMD
git stash save --include-untracked
```
_Incluye todos los archivos, junto a los que git no le esta dando seguimiento._

(Por ultimo:)
```CMD
git stash clear
```
_Este comando borra todas las entradas que hay en el Stash_




[Por ver y entender. Rebases]
[_Sección 5 video 7-8-9-_]

Rebase Squash
```CMD
git rebase -i HEAD~4

//En el menu interactivo cambiar "pick" por "squash" en el commit superior de ambos que desees unir
```
_Rebase interactivo con los 4 últimos commits realizados_

Rebase Reword
```CMD
git rebase -i HEAD~1

//En el menu interactivo cambiar "pick" por "reword" en el commit que queremos renombrar.
```

Edit.:
_Justo antes del add si no querías modificar algún archivo de los presentes entre los pendientes_
```CMD
git checkout -- nombreANoModificar
```

```CMD
git rebase -i HEAD~2

//En el menu interactivo cambiar "pick" por "edit"
```

[Por ver sección 5]