## SELECTOR DE ELEMENTOS
Seleccionar elementos HTML basándose en su tipo de elemento
```css
h1 { 
    color: green; /* declaration block */
}
```
## Selector ID
Seleccionar un elemento específico para estilizarlo
```css
#header1 { 
    color: blue;
}
```
## SELECTORES DE CLASE 
Selecciona elementos con el nombre de clase especificado 
```css
.navigation { 
    margin: 2px;
  }
```

## ELEMENTO CON SELECTOR DE CLASE
Método más específico para seleccionar elementos HTML.
Selecciona primero el elemento HTML y después la clase CSS o ID.
```css
p.introduction { 
    margin: 2px;
    color:brown;
}
```
## SELECTORES DESCENDIENTES
Son útiles si necesita seleccionar elementos HTML que están contenidos dentro de otro selector.
Seleccionará todos los elementosh1 que estén contenidos dentro del elemento con el IDblog. La regla CSS.
```css
#blog h1 {
    color: purple;
}
```
También se pueden seleccionar varios descendientes.
```css
#blog div h2 {
    color: palevioletred;
}
```
## SELECTORES HIJOS
Los selectores hijos son más específicos que los selectores descendientes. Sólo seleccionan elementos que son descendientes inmediatos (hijos) de un selector (el padre).*/
```css
#blog > h1 {
    color: yellowgreen;
}
```
## *pseudoclase :hover*
Cambia el color del hipervinculo al pasar el mouse por encima
```css
a:hover {
    color: orange;
}
```
