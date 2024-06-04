[Un sitio web donde podriamos ver si estamos haciendo un codigo bueno en Css es " CSS Specificity Graph Generator "]

_La siguiente forma hace nula la especificidad de nuestro navegador_
```css
h1.title {
background-color: red !important ;
}
```
_Aplica si o si el estilo sin tener en cuenta especificaciones anteriores (no es recomendada)_

### La especificidad en css funciona bajo las siguientes normas:

_**Etiquetas y pseudoelementos --------- 001**_

_**Clases, atributos y pseudoclases --------- 010**_

_**id -------------------------------- 100**_

_**Estilos en linea --------- 1000**_

_Esto funciona en forma binaria, cada elemento tomara una especificidad lo que afectara el resultado final_


_**El Cascade funciona siempre que la especificidad sobre el elemento sea la misma**_

