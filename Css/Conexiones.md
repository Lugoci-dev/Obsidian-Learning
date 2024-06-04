_Existen 4 formas de añadir estilos Css a un documento HTML_

1- Conectar a un archivo:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    (...)
    //etiketa link
    <link rel="stylesheet" href="./css/style.css">
</head>
<body>
    <h1>Esta es una prueba con estilo</h1>
</body>
</html>
```
_Dentro de la etiqueta 'head' de nuestro HTML añadimos la etiqueta 'link rel="stylesheet" href="./css/style.css"' para conectar el archivo de css que se encuentra en el directorio del "href"_ 

2- A través de la etiqueta styles dentro del head:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  (...)
    <!-- <link rel="stylesheet" href="./css/style.css"> -->
    <style>
        h1{
            color: rgb(3, 62, 79);
        }
    </style>
</head>

<body>(...)</body>
```
_Dentro del 'style' se trabaja del mismo modo que en un archivo.css_

3- Estilos en linea, o dentro de las etiquetas: (no recomendada)
```html
<body>
    <h1 style="color: aqua; text-align: center;" >Esta es una prueba con estilo</h1>
</body>
```
_En este caso se trabaja con la propiedad style de cada etiqueta y se añaden los estilos propios a cada una._ 

4- Con un @import desde el 'style' dentro del 'head': (no recomendada)
```html
<head>
(...)
    <title>Css Bases desde 0</title>
    <!-- <link rel="stylesheet" href="./css/style.css"> -->
    <style>
        /* h1{
            color: rgb(3, 62, 79);
        } */
        @import url(./css/style.css);
    </style>
</head>
```
_Este @import equivale a añadir nuestro archivo css pero en css se hace con un @import mientras que en HTML con la etiqueta 'link'_
