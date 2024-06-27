Si instaló Python desde la fuente, con un instalador de [python.org](https://www.python.org/) o mediante [Homebrew](https://brew.sh/) , ya debería tener pip.

**Puede comprobarlo ejecutando el siguiente comando**
```CMD
py -m pip --version
```

Si `pip`aún no está instalado, primero intente iniciarlo desde la biblioteca estándar:
```CMD
py -m ensurepip --default-pip
```


Si eso todavía no te permite ejecutar :`python -m pip`
- Descargue de forma segura [get-pip.py](https://bootstrap.pypa.io/get-pip.py) [[ 1 ]](https://packaging.python.org/en/latest/tutorials/installing-packages/#id7)

- Correr . [[](https://packaging.python.org/en/latest/tutorials/installing-packages/#id8) [2](https://packaging.python.org/en/latest/tutorials/installing-packages/#id8) []](https://packaging.python.org/en/latest/tutorials/installing-packages/#id8) Esto instalará o actualizará pip. Además, instalará [las herramientas de configuración](https://packaging.python.org/en/latest/key_projects/#setuptools) y [la rueda](https://packaging.python.org/en/latest/key_projects/#wheel) si aún no están instaladas.
```CMD
python get-pip.py
````
