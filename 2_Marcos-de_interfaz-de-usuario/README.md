# Marcos de interfaz de usuario
En este módulo se aprenderá a utilizar el framework Bootstrap para construir interfaces responsivas y las ventajas de trabajar con frameworks de interfaz de usuario.
# 1. Introduccion a los marcos y bibliotecas de interfaz de usuario
## Introducción al diseño responsivo
### Diseño responsivo
- El diseño responsivo significa que una página web puede estirarse o encogerse automáticamente según la pantalla en la que se muestre.
- Es la combinación de tres técnicas: cuadrículas flexibles, imágenes fluidas y consultas multimedia.

Por ejemplo, si desea que el fondo de su sitio web aparezca azul en una pantalla con un tamaño de pantalla inferior o igual a 700 píxeles.
```css
@media only screen and (max-width: 700px) {
  body {
    backgroud-color: blue;
  }
}
```
Al igual que en un teléfono móvil, puedes usar una regla multimedia para establecer el fondo en función del tamaño de la pantalla.
- En el diseño responsivo, el valor de píxel especificado suele denominarse punto de interrupción.

**Punto de interrupción** 
- Es el punto en el que el contenido y el diseño de un sitio web se adaptarán para ofrecer la mejor experiencia de usuario posible. 
- Un punto de interrupción puede funcionar de diferentes maneras en tres redes diferentes:

| Rejilla fija | Rejilla fluida | Rejilla hibrida |
|---|--- |---|
| Columnas y márgenes flexibles | Contenido flexible que va de borde a borde según el tamaño de la pantalla |  Ancho fluido   |
| La cuadrícula fija tiene un contenido fijo que no cambia en un rango de puntos de interrupción específico, mientras que los márgenes flexibles ocupan el espacio restante de la pantalla | Los pilares crecen o se contraen para adaptarse al espacio disponible | Son fijas con componentes |

## Bootstrap
Bootstrap es una biblioteca de código CSS y JavaScript que facilita la construcción rápida de sitios web atractivos y responsivos. Ofrece componentes reutilizables y una rejilla responsive predefinida, simplificando el desarrollo web. Su popularidad se debe a su capacidad para ahorrar tiempo, permitiendo a los desarrolladores crear prototipos y sitios visualmente atractivos sin la necesidad de profundos conocimientos en CSS. Al aprender Bootstrap, se adquieren habilidades valiosas, asegurando consistencia en el diseño y facilitando la colaboración en equipos y proyectos. Su versatilidad y prevalencia en la industria lo convierten en una herramienta fundamental para potenciar las habilidades de desarrollo web.

Bootstrap es una colección de trozos de código preescrito en CSS y JavaScript que le permite crear sitios web más rápidamente que si tuviera que crear cada trozo de código desde cero. 

### [1. Primeros pasos en Bootstrap:](https://github.com/trejazmine/Frontend-Training/tree/main/2_Marcos-de_interfaz-de-usuario/1_Primeros-pasos)

### [2. Uso de los estilos de Bootstrap](https://github.com/trejazmine/Frontend-Training/tree/main/2_Marcos-de_interfaz-de-usuario/2_Uso-de-estilos)
- El video presenta la clase CSS de Bootstrap, destacando su utilidad para el diseño responsivo de sitios web. Se explica que no es necesario rediseñar el sitio para cada dispositivo, ya que Bootstrap ofrece clases y modificadores que facilitan la adaptación a diferentes tamaños de pantalla.
- Se menciona la importancia de entender los in fixes y modificadores. Los in fixes se utilizan para puntos de ruptura responsivos en el sistema de cuadrícula de Bootstrap, con diferentes abreviaturas para cada tamaño de pantalla, como SM, MD, LG, XL, y XXL.
![In-fixes](https://github.com/trejazmine/Frontend-Training/blob/main/2_Marcos-de_interfaz-de-usuario/2_Uso-de-estilos/in-fixes.png?raw=true)
**Modifiers:** Primary, Secondary, Success, Info, Warning, Danger, Light, Dark
- Facilidad de cambiar el color de una alerta utilizando estos modificadores.
```html
<div class="col-lg-6"> <!-- cambiamos la regla para pantallas grandes (LG) -->
    <div class="alert alert-primary" role="alert"> <!-- primary is the modifier -->
        A message.
    </div>
</div>
```
### 3. Rejilla Bootstrap
El video destaca la importancia de la rejilla adaptable y los puntos de ruptura en el diseño responsivo de una página web, utilizando Bootstrap como herramienta. Bootstrap emplea un sistema de rejilla de 12 columnas que puede ser fluido o fijo, con un contenedor, filas y columnas como elementos clave.

Se muestra en el ejemplo de la página web de Little Lemon cómo se pueden añadir columnas a una fila y ajustar su anchura mediante clases CSS. Además, se explora la flexibilidad de Bootstrap al permitir la configuración de diferentes disposiciones según el dispositivo, utilizando reglas CSS específicas del punto de ruptura. En este caso, se apilan las columnas en dispositivos móviles y se muestran una al lado de la otra en dispositivos de escritorio.

Se destaca la eficacia del sistema de cuadrícula de Bootstrap para simplificar el desarrollo, ahorrando tiempo al adaptar automáticamente el contenido a diferentes dispositivos mediante sus reglas CSS y puntos de ruptura. La versatilidad del sistema de cuadrícula de Bootstrap lo posiciona como una herramienta poderosa y adecuada para la mayoría de las necesidades de desarrollo.

- El sistema de rejilla de bootstrap nos ayuda a crear diseños de páginas web a través de una serie de filas y columnas que albergan nuestro contenido.
- Para la rejilla, bootstrap utiliza un sistema de rejilla de 12 columnas que puede ser fluido o fijo.
- Siempre tiene un contenedor, filas y columnas (siempre comienza con el contenedor).
- **El contenedor contiene almohadillas y alinea su contenido.**
- Su anchura se determina en función del punto de ruptura responsive actual.
![Rejillas](https://github.com/trejazmine/Frontend-Training/blob/main/2_Marcos-de_interfaz-de-usuario/3_Rejillas/rejillas.png?raw=true)

### 4. Componentes de Bootstrap

### 5. Uso de la documentación de Bootstrap

### 6. Otros marcos y bibliotecas CSS

# 2. Introduccion a React

### 1. Contenidos estaticos y dinamicos

### 2. Aplicaciones de una sola página

## REACT

### 1. Funcionamiento

### 2. DOM virtual

### 3. Jerarquia de componentes
