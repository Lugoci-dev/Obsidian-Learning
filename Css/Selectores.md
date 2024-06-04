
#Tipos 

[Selectores Elementales:]
#### **_Selector Universal:_**
```css
*{
background-color: lightcoral;
}
```
_Aplica este estilo a todos los elementos_

#### **_Selector de etiqueta:_**
```css
/* Pueden utilizarce varias etiquetas separadas por comas*/
nombreDeLaEtiqueta , nombreDelaOtraEtiqueta?{
background-color: lightcoral;
}
```
_Aplica el estilo de la regla a todas las etiquetas del mismo nombre_

[Selectores de Atributo:]
#### **_Selectores de id:_**
```css
#nombreDelId, #nombreDelId2?{
background-color: lightcoral;
}
```
_Se aplica a las etiquetas con el id especificado(el id es único)_

#### **_Selectores de clase:_**
```css
.nombreDeLaClase, .nombreDeLaOtraClase?{
background-color: lightcoral;
}
```
_Se agrega el estilo a todos los elementos con esta Clase_

#### **_Selector de atributos:_**
```html
<etiketa atributo="valor-del-atributo"></etiketa>
```
Este selector se aplicara a la etiqueta con el atributo especificado, si son varias se aplicara a todas ellas.
```css
[atributo]{
background-color: lightcoral;
}

/* Este se aplicara solo a aquellos que tengan el mismo valor de atributo */
[atributo="valor-del-atributo"]{
background-color: lightcoral;
}

/* Este comprueba si hay algun atributo que empiece con ese "valor" dado y le aplica los estilos a todos los que empiecen con esa cadena */
[atributo^="valor"]{
background-color: lightcoral;
}

/* EN este aplicara el estilo de la regla a todos los atributos iguales que en cualquier parte de su valor contengan la cadena dada */
[atributo*="valor"]{
background-color: lightcoral;
}

/*En este caso si termina por esta palabra se aplicaran los estilos*/
[atributo$="valor"]{
background-color: lightcoral;
}

/* Se utiliza en ocasiones que el valor del atributo puede venir acompannado de un guion */
[atributo|="valor-"]{
background-color: lightcoral;
}
```

#### **_Selectores Descendentes_**
_Se utilizan cuando se desea dar un estilo solo a alguna etiqueta especifica que se encuentra dentro de otra:_
```html
<body>
    <div>
        <h1 class="valor" >Esta es una prueba con un estilo diferente</h1>
        <h1>Esta es una prueba con estilo</h1>
    </div>
    <h1 class="valor" >Esta es una prueba con estilo</h1>
</body>
```

_Aquí le damos estilo solo al H1 de clase valor que esta dentro del div_
```css
div .valor{
background-color: lightcoral;
}
```
_Lo que realmente hacemos es seleccionar hijos_

#### **_Selectores Combinadores_**
_Se utiliza para seleccionar elementos a partir de sus hermanos_

```html
<body>
    <div>
        <h1 class="valor" >Esta es una prueba</h1>
    	<p class="parrafo" >esto debe parecer un texto</p>
        <h1 class="valor" >Esta es una prueba con un estilo diferente</h1>
        <h1>Esta es una prueba con estilo</h1>
        <h1 class="valor" >Esta es una prueba con un estilo diferente 
           <span>Pruevalo</span>
        </h1>
    </div>
    <h1 class="valor" >Esta es una prueba con estilo</h1>
</body>
```

_Al utilizar el + solo aplicara los cambios al hermano a continuación del primer selector que tengan la clase valor_
```css
.parrafo + .valor {
background-color: lightcoral;
}
```
_podrían utilizarse tanto etiquetas y clases para seleccionar los elementos_

Al utilizar la ~ se seleccionaran todos los hermanos solo a continuación que coincidan con el 2do selector de la regla.
```css
.parrafo ~ .valor {
background-color: lightcoral;
}

/* Al igual que en todos los selectores anteriores, estos pueden combinarse para obtener el objetivo deseado */
.parrafo ~ .valor span {
background-color: lightcoral;
}
```

Un ultimo selector, utilizado para referirse a los hijos directos de una etiqueta:

```css
selectorPadre > .selectorHijo{
background-color: lightcoral;
}
/* Este seleccionara a todos los elementos que coincidan con el selector hijo que sean hijos directos del selector padre */
```
