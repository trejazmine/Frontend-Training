# Conceptos básicos de alineación
Exploremos cómo alinear texto y elementos HTML utilizando CSS.
Centrémonos primero en la alineación horizontal. La alineación vertical es más difícil, así que la exploraremos más adelante.
## Alineación de texto
Alinear texto dentro de un elemento HTML es muy sencillo. Para ello, se utiliza la propiedad CSStext-align. En el siguiente ejemplo, la regla CSS está estableciendo que el texto de todos los elementos de párrafo esté alineado al centro.
```css
p {
    text-align: center;
}
```
La alineación del texto puede establecerse enleft,right,center yjustify.

La alineaciónjustify extiende el texto para que cada línea del texto tenga la misma anchura.

La alineación por defecto esleft para idiomas que son de izquierda a derecha como el inglés. Para las lenguas que van de derecha a izquierda, como el árabe, la alineación por defecto esright.

## Alineación de elementos HTML
La alineación de los elementos HTML es más complicada que la del texto. Para alinear elementos HTML, debe tener en cuenta el modelo de caja y el flujo del documento de lecciones anteriores. La alineación de un elemento HTML se realiza cambiando las propiedades de su modelo de caja y cómo afecta al flujo del documento.

### Alineación central de elementos HTML
Para alinear al centro un elemento, usted establece un ancho en el elemento y empuja sus márgenes hacia fuera para llenar el espacio disponible restante del elemento padre como en la siguiente estructura HTML:
```html
<div class="parent">
  <div class="child">
  </div>
</div>
```
### Valor HSL
HSL es un modelo de color más reciente definido como Tono (H), Saturación (S) y Luminosidad (L). El objetivo del modelo es simplificar la visualización mental del color que representa el valor.
Piense en un arco iris convertido en un círculo completo. Esto representa el Matiz. El valor del Tono es el valor del grado en este círculo, de 0 grados a 360 grados. 0 es rojo, 120 es verde y 240 es azul.
```css
p { 
  color: rgba(255, 0, 0, 0.8); 
}
```
