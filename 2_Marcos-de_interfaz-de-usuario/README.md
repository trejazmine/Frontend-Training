# [Marcos de interfaz de usuario](https://github.com/trejazmine/Frontend-Training/tree/main/2_Marcos-de_interfaz-de-usuario)
  En este módulo se aprenderá a utilizar el framework Bootstrap para construir interfaces responsivas y las ventajas de trabajar con frameworks de interfaz de usuario.
# 1. Introduccion a los marcos y bibliotecas de interfaz de usuario
## Introducción al diseño responsivo
### Diseño responsivo
  El diseño responsivo significa que una página web puede estirarse o encogerse automáticamente según la pantalla en la que se muestre.
  Es la combinación de tres técnicas: cuadrículas flexibles, imágenes fluidas y consultas multimedia.

Por ejemplo, si desea que el fondo de su sitio web aparezca azul en una pantalla con un tamaño de pantalla inferior o igual a 700 píxeles.
```css
@media only screen and (max-width: 700px) {
  body {
    backgroud-color: blue;
  }
}
```
Al igual que en un teléfono móvil, puedes usar una regla multimedia para establecer el fondo en función del tamaño de la pantalla.
  En el diseño responsivo, el valor de píxel especificado suele denominarse punto de interrupción.

### Punto de interrupción 
- Es el punto en el que el contenido y el diseño de un sitio web se adaptarán para ofrecer la mejor experiencia de usuario posible. 
- Un punto de interrupción puede funcionar de diferentes maneras en tres redes diferentes:

| Rejilla fija | Rejilla fluida | Rejilla hibrida |
|---|--- |---|
| Columnas y márgenes flexibles | Contenido flexible que va de borde a borde según el tamaño de la pantalla |  Ancho fluido   |
| La cuadrícula fija tiene un contenido fijo que no cambia en un rango de puntos de interrupción específico, mientras que los márgenes flexibles ocupan el espacio restante de la pantalla | Los pilares crecen o se contraen para adaptarse al espacio disponible | Son fijas con componentes |

## Bootstrap
  Bootstrap es una biblioteca de código CSS y JavaScript que facilita la construcción rápida de sitios web atractivos y responsivos. 
  Ofrece componentes reutilizables y una rejilla responsive predefinida, simplificando el desarrollo web. S
  Bootstrap es una colección de trozos de código preescrito en CSS y JavaScript que le permite crear sitios web más rápidamente que si tuviera que crear cada trozo de código desde cero. 

### [1. Primeros pasos en Bootstrap](https://github.com/trejazmine/Frontend-Training/tree/main/2_Marcos-de_interfaz-de-usuario/1_Primeros-pasos)

### [2. Uso de los estilos de Bootstrap](https://github.com/trejazmine/Frontend-Training/tree/main/2_Marcos-de_interfaz-de-usuario/2_Uso-de-estilos)
  El video presenta la clase CSS de Bootstrap, destacando su utilidad para el diseño responsivo de sitios web. Se explica que no es necesario rediseñar el sitio para cada dispositivo, ya que Bootstrap ofrece clases y modificadores que facilitan la adaptación a diferentes tamaños de pantalla.
  Se menciona la importancia de entender los in fixes y modificadores. Los in fixes se utilizan para puntos de ruptura responsivos en el sistema de cuadrícula de Bootstrap, con diferentes abreviaturas para cada tamaño de pantalla, como SM, MD, LG, XL, y XXL.
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
### [3. Rejilla Bootstrap](https://github.com/trejazmine/Frontend-Training/tree/main/2_Marcos-de_interfaz-de-usuario/3_Rejillas)
  El sistema de rejilla de bootstrap nos ayuda a crear diseños de páginas web a través de una serie de filas y columnas que albergan nuestro contenido.
  Para la rejilla, bootstrap utiliza un sistema de rejilla de 12 columnas que puede ser fluido o fijo.
  Siempre tiene un contenedor, filas y columnas (siempre comienza con el contenedor).
**El contenedor contiene almohadillas y alinea su contenido.**
  Su anchura se determina en función del punto de ruptura responsive actual.
![Rejillas](https://github.com/trejazmine/Frontend-Training/blob/main/2_Marcos-de_interfaz-de-usuario/3_Rejillas/rejillas.png?raw=true)
  Bootstrap permite la configuración de diferentes disposiciones según el dispositivo, utilizando reglas CSS específicas del punto de ruptura.
### [4. Componentes de Bootstrap](https://github.com/trejazmine/Frontend-Training/tree/main/2_Marcos-de_interfaz-de-usuario/4_Componentes)
  Bootstrap incluye un conjunto preconfeccionado de elementos de interfaz de usuario y estilos para ayudarle a construir su sitio web.
```html
<div class="col-12 col-lg-6">
    <div class="card">
        <img src="calamari.jpg" class="card-img-top" />
        <div class="card-body">
            <h2 class="card-title">Fried Calamari <span class="badge bg-primary">New</span></h2>
            <p class="card-text">Squid, buttermilk,</p>
        </div>
    </div>
</div>
```
- `col-12`: La columna ocupará todo el ancho disponible en dispositivos pequeños (menos de 576 píxeles). En dispositivos más pequeños, la columna ocupará las 12 columnas disponibles.
- `col-lg-6`: La columna ocupará la mitad del ancho disponible en dispositivos grandes (igual o superior a 992 píxeles). En dispositivos grandes, la columna ocupará 6 de las 12 columnas disponibles.
- `card`: Es un contenedor que se utiliza para presentar contenido de manera estructurada.
- `card-img-top`: Se aplica a la imagen dentro de la tarjeta y coloca la imagen en la parte superior de la tarjeta.
- `card-body`: Se aplica al contenedor que alberga el contenido principal de la tarjeta, como el título y el texto.
- `card-title`: Especifica el estilo para el título de la tarjeta.
- `badge bg-primary`: ***Un badge es un pequeño elemento que se utiliza para etiquetar o resaltar información. bg-primary establece el color de fondo del badge como azul primario.***
- `card-text`: Especifica el estilo para el texto de la tarjeta.

### 5. Uso de la documentación de Bootstrap
  Bootstrap incluye documentación detallada sobre la configuración y el uso de las funciones disponibles en su biblioteca.
  La documentación de Bootstrap está disponible actualmente en el siguiente [enlace](https://getbootstrap.com/docs).
#### 5.1 Formularios
  ##### a. Estilos de formularios
  Bootstrap incluye reglas CSS para mejorar el estilo visual de los elementos de entrada.
  Esta tabla describe los diferentes elementos de formulario HTML y qué clase CSS de Bootstrap debe utilizarse para ellos.
  | Elemento de formulario | Clase CSS |
  | :-- | :-- |
  | `input` | `form-control`|
  | `input type="checkbox"` | `form-check-input`|
  | `input type="radio"` | `form-check-input`|
  | `input type="range"` | `form-range`|
  | `select` | `form-select`|
  ##### b. Interruptores
  Bootstrap incluye reglas CSS para dar estilo a los elementos de entrada de casilla de verificación como conmutadores. Para ello:
    1. Añada lainput a un elementodiv. 
    2. En el elementodiv, aplique las clases CSSform-check yform-switch. 
    3. En el elementoinput, añada la clase CSSform-check-input.
  ```html
  <div class="form-check form-switch">
    <input class="form-check-input" type="checkbox">
  </div>
  ```
  ##### c. Grupos de entrada
  Son útiles para proporcionar **contenido adicional al campo de entrada.** Para ello:
    1. Añada elinput a un elementodiv.
    2. Aplique las clases CSS `input-group` en el elementodiv.
    3. Añada un elemento `span` antes y/o después del elemento `input` y aplíquele la clase CSS `input-group-text`. El contenido del texto se añade entonces dentro del elemento `span`.
  ```html
  <div class="input-group">
    <span class="input-group-text">$</span>
    <input type="text" class="form-control">
    <span class="input-group-text">.00</span>
  </div>
  ```
  ##### d. Etiquetas flotantes
  Son útiles para proporcionar **contenido adicional al campo de entrada.** Para ello:
    1. Añada el input a un elemento `div`.
    2. Aplique las clases CSS `input-group` en el elemento `div`.
    3. Añada un elemento `span` antes y/o después del elemento `input` y aplíquele la clase CSS `input-group-text`. El contenido del texto se añade entonces dentro del elementospan.
  ```html
  <div class="input-group">
    <span class="input-group-text">$</span>
    <input type="text" class="form-control">
    <span class="input-group-text">.00</span>
  </div>
  ```
  ##### e. Etiquetas flotantes
    Ayudan a  proporcionar información del formulario al usuario como parte de la propia entrada. La información permanece visible si el usuario está interactuando con el elemento o si el elemento tiene contenido. Para ello:
      1. Añada el input a un elemento `div`. En el elemento `div`, aplique las clases CSS `form-floating`.
    ```html
    <div class="form-floating">
      <input type="email" class="form-control" id="addressInput" placeholder="Address">
      <label for="addressInput">Address</label>
    </div>
    ```
### 6. Otros marcos y bibliotecas CSS
[Foundation](https://get.foundation/),[Pure.css](https://purecss.io/),[Tailwind CSS](https://tailwindcss.com/), [UIKit](https://getuikit.com/) y [MVP.css]([UIKit](https://getuikit.com/))
# 2. Introduccion a React

### 1. Contenidos estaticos y dinamicos

### 2. Aplicaciones de una sola página

## REACT

### 1. Funcionamiento

### 2. DOM virtual

### 3. Jerarquia de componentes
