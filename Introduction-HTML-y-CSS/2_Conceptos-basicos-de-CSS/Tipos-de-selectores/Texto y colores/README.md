# Texto y color en CSS
Cuando diseñe páginas web, trabajará mucho con colores y texto. Existen muchas formas diferentes de mostrar texto y otras tantas de definir los colores.
Esta lectura cubre cómo funcionan el texto y el color en CSS.
## Color
Los colores se utilizan, por ejemplo, en muchas propiedades CSS:
```css
p { 
  color: blue; 
}```

A partir de la versión 3 de CSS, existen cinco formas principales de hacer referencia a un color.
- Por valor RGB
- Por valor RGBA
- Por valor HSL
- Por valor hexadecimal
- Por nombres de color predefinidos

### Valor RGB
RGB es un modelo de color que suma los colores rojo (R), verde (G) y azul (B) para crear colores. Se basa en cómo ve los colores el ojo humano.
Cada valor se define como un número entre0 y255, que representa la intensidad de ese color.
Por ejemplo, el color rojo tendría el valor RGB de255,0,0 ya que la intensidad del color rojo sería del 100% mientras que el azul y el verde serían del 0%.
El color negro sería entonces0,0,0 y el color blanco255,255,255.
Cuando se utilizan valores RGB en CSS, se pueden definir utilizando la palabra clavergb:
```css
p { 
  color: rgb(255, 0, 0); 
}

### Valor RGBA
RGBA es una extensión de RGB que añade un canal alfa (A). El canal alfa representa la opacidad, o transparencia, del color.
Al igual que el RGB, se especifica en CSS mediante la palabra clavergba:
```css
p { 
  color: rgba(255, 0, 0, 0.8); 
}

### Valor HSL
HSL es un modelo de color más reciente definido como Tono (H), Saturación (S) y Luminosidad (L). El objetivo del modelo es simplificar la visualización mental del color que representa el valor.
Piense en un arco iris convertido en un círculo completo. Esto representa el Matiz. El valor del Tono es el valor del grado en este círculo, de 0 grados a 360 grados. 0 es rojo, 120 es verde y 240 es azul.
```css
p { 
  color: rgba(255, 0, 0, 0.8); 
}
![Circulo arcoiris]([URL_de_la_imagen](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/6W-NFfelTF-vjRX3pXxfHw_71bfe705b84941a1b8f51eea05a848e1_text_color_hue.png?expiry=1705536000000&hmac=e2pCFN6asTQZpamgQNJAc6PpViII19Z90IHt9dSr2Js)https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/6W-NFfelTF-vjRX3pXxfHw_71bfe705b84941a1b8f51eea05a848e1_text_color_hue.png?expiry=1705536000000&hmac=e2pCFN6asTQZpamgQNJAc6PpViII19Z90IHt9dSr2Js)
