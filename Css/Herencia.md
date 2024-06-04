_Existen propiedades que se heredan de una etiqueta a sus etiquetas hijo, ejemplo de esto es el color:_

```html
<div style="color: aqua;" >
        <h1 class="valor" >Esta es una prueba con estilo</h1>
        <h1>Esta es una prueba con estilo</h1>
</div>
```
_En este caso especifico, el color del div padre se hereda a los hijos y modifica en ambos el color_

**Esto no ocurre en todos los casos, por lo que podemos forzar la herencia con una palabra clave:**
 ```css
 .link{
  color: inherit;
 }
```
_Esto forzara heredar el color del padre de el elemento determinado y sirve para cualquier propiedad que no se herede por defecto y queramos heredarla_

**_Y lo contrario, que seria si esta heredando alguna propiedad que no queramos podemos hacerlo así:_**
```css
.link{
  color: inherit;
 }
```

