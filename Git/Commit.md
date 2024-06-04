
_*Un commit es como una fotografía de nuestro código*_

```CMD
git commit -m "commitName"

```
_Crea una copia de los archivos en seguimiento_

```CMD
git commit -am "commitName"
```
_Hace un commit directo de los archivos modificados(sin necesidad del git add)_

```CMD
git commit --amend -m "commitNameRepared"
```
_Permite reescribir el mensaje de nuestro ultimo commit_



Información detallada sobre los autores y la fecha de los commits
```CMD
git log
```
_Muestra el autor y la fecha de cada commit de mas reciente a mas antiguo_

```CMD
git log --oneline
git log --oneline --decorate --all --graph
```
_Muestra un versión reducida del log_
