
## Margin
#### _El margen solo puede aplicarse a 4 lados en nuestro elemente:_

**margin-top: Margen superior.**

**margin-right: Margen derecho.**

**margin-bottom: Margen inferior.**

**margin-left: Margen izquierdo.**

##### Esta propiedad admite hasta cuatro valores que van en el orden de las agujas del reloj

**4 valores -> margin: 'top' 'right' 'bottom' 'left';**

**3 valores -> margin: 'top' 'right/bottom' 'left';**

**2 valores -> margin: 'top/right' 'bottom/left';**

**1 valores -> margin: 'top/right/bottom/left';**

_Las comillas se han puesto para diferenciar solamente_

#### _Tanto el margin como los valores de height y widht no funcionan como esperaríamos para los elementos en linea_

_Las propiedades  height y widht no le aplican ningún tipo de cambio porque lo que define su tamaño es su contenido._

_Y en las propiedades del margen solo le aplicaran cambios margin-right y margin-left_
(Solo tienen márgenes horizontales)
a diferencia de los elementos en bloque que tiene todos los márgenes.

_Existe una propiedad que podemos utilizar en los elementos de bloque:_

```css
margin: auto;
margin-right: auto;
margin-left: auto;
```
_Pero debe tener altura y anchura ya definidos para que funcione, debido a que al ser de bloque(y no ser especificado lo contrario) esta ocupando todo el espacio disponible horizontalmente_

## Padding

_El padding es el espacio interno entre el borde y su contenido_

Al igual que el margin, es una propiedad abreviada (shortHand) que permite dar un margen interior a los cuatro lados del contenedor

(_**Tiene el mismo funcionamiento que el margin**_)

**padding-top: Padding superior.**

**padding-right: Padding derecho.**

**padding-bottom: Padding inferior.**

**padding-left: Padding izquierdo.**

##### Esta propiedad admite hasta cuatro valores que van en el orden de las agujas del reloj

**4 valores -> padding: 'top' 'right' 'bottom' 'left';**

**3 valores -> padding: 'top' 'left/right' 'bottom';**

**2 valores -> padding: 'top/bottom' 'left/right';**

**1 valores -> padding: 'top/right/bottom/left';**

_Las comillas se han puesto para diferenciar solamente_

(_El padding a diferencia del margin alarga el contenido de la caja en consecuencia de su valor_)

**También a diferencia de el margin, el padding si aplica todos los cambios a los elementos en linea.**

## Border

_Es un shortHand al igual que el margin y el padding que agrega tres propiedades_

**_border-width: ancho del borde_**

**_border-style: estilo del borde_**

**_border-color: color del borde_**


```css
block{
    border: 1px solid rebeccapurple;
    /* Que es lo mismo que: */
    border-width: 1px;
    border-style: solid;
    border-color: rebeccapurple;
}
```

_Cada una de estas propiedades también son shortHand que modifican de forma individual su valor relativo:_

**Ej.:**
_**border-style: estilo del borde**_
	_border-top-style_
	_border-right-style_
	_border-left-style_
	_border-bottom-style_

_y así con las restantes._

(_Por lo que si lo hiciéramos individualmente cada uno, funcionaria correctamente_)
```css
.block{
    border-right-color: aqua;
}
```
_y así con cualquiera de las 3 * 4 -1 propiedades restantes_

### Box Sizing

_Existe una propiedad, que se utiliza para asignar los tamaños de un contenedor en función del espacio asignado inicialmente:_

**_box-sizing_**
```css
box-sizing: border-box;
```
_Esto lo que hace es realizar un calculo en función de los márgenes y otras propiedades asignadas respetando el tamaño asignado al principio_

**_[[Border Radius]]_**
**_[[Overflow]]_**
