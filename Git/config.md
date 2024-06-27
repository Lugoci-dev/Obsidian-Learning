Muestra nuestras configuraciones hechas
(_Para modificar la seguridad de git_)
```CMD
git config --global http.sslVerify false/true
```
(_Permite modificarlas_)
```CMD
git config --global -e
```
(No permite modificaciones)
```CMD
git config --global -l
```

(Configuraciones del entorno de git.)

_Forma para configurar alias a comandos "demasiado" largos_
```CMD
[inicial]
git config --global alias.lg "log --oneline --decorate --all --graph"
git config --global alias.s "status -s -b"

[equivalente]
git lg
git s
```
Ejemplos

