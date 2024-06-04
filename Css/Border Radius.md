(_El border Radius es otro shortHand_)

Proporciona cuatro propiedades:

**_border-top-left-radius:_**

**_border-top-right-radius:_**

**_border-bottom-left-radius:_**

**_border-bottom-right-radius:_**

_cada una modifica su correspondiente borde._

```css
border-radius: 50px;
```
_Si asignamos un solo valor a esta propiedad lo asignamos 50px a cada borde de la caja_.

**Si no se le asigna ningún valor especifico a cada borde, este funcionara de la misma manera que las propiedades ya vistas: padding y margin.**

#### También pueden asignarse bordes en forma de elipse:

```css
/* esta asigna al borde definido un elipse con las dimensiones de ambos radios proporcionadas respectivamente en los ejes x y */
border-top-left-radius: 50px 100px;

/* y en estos casos se asigna a todos los bordes la misma elipse (x y) */
border-radius: 50px / 100px;

/* para obtener nuevos resultados*/
border-radius: 50px 100px / 100px 150px;
border-radius: 50px 100px 150px/ 100px 150px 200px;
border-radius: 50px 100px 150px 200px/ 100px 150px 200px 250px;
/* A ambos lados del slash cada diametroes respectivamente asignado a los bordes.*/
```
_Aunque la forma menos complicada de trabajar con elipses es trabajando con ellas de forma individual_
