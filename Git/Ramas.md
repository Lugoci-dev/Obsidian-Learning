_Las ramas son como una linea alternativa del tiempo_

Para crear una nueva rama en nuestro repositorio:
```CMD
git branch ramaName

git checkout -b newRamaName

//Aqui se crea una nueva rama y nos movemos a ella automaticamente.
```
Si escribimos solamente:
```CMD 
git branch
```
nos mostrará las ramas que tenemos en nuestro repositorio, y  en cual nos encontramos.

Para movernos de una rama a otra utilizamos el sigte comando:
```CMD
git checkout ramaObjetivoName
```

Y para mostrar las diferencias entre ambas ramas:
```CMD
git diff rama1Name rama2Name
```

*Unir ramas*
Cuando nos preparamos para unir una rama con otra, debemos asegurarnos de estar en la rama a la cual fusionaremos la otra.
```CMD
git merge ramaAUnir
```
Al unir ambas ramas, es buena practica eliminar la rama sobrante:
```CMD
git branch -d ramaBorrarName
```

Note:
(Al estar en una rama alternativa solo podrás ver el código de esta, si has hecho cambios en alguna otra rama estos no se verán a menos que estés en ella.)


Merch Automático:
_Cuando en nuestra rama2 modificamos alguno de los archivos, y en un instante de tiempo superior a este cambio en nuestra rama1 hacemos alguna otra modificación (sin crear conflictos entre las modificaciones(no sean en el mismo archivo)) . El Merge automático se encargara de priorizar los cambios en función del tiempo._


Conflictos:
_Cuando en una rama alternativa modificamos un archivo y después desde otra rama modificamos nuevamente el mismo archivo, una vez que intentemos unir estas ramas habrá conflicto entre ellas_