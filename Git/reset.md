(_Se utiliza para modificar el contenido de los commit_)



```CMD
git reset .
git reset fileName.tipe
git reset *.png
git reset file/
```
Estos comandos devuelven nuestros archivos dentro del staged
fuera del mismo.


(_Se usan banderas como --soft, --hard..._)

```CMD
git reset --soft HEAD^
git reset --soft HEAD~1
git reset --soft ideCommit
```
Este comando nos permite modificar el contenido del ultimo commit (por el HEAD^)

```CMD
git reset --hard HEAD^
git reset --hard HEAD~1
git reset --hard ideCommit
```
Este comando elimina el ultimo commit
_El git reset regresa hasta el punto dado después del --hard (sin modificarlo a el)_

Muestra todas las acciones hechas en los repositorios.
```CMD
git reflog
```
