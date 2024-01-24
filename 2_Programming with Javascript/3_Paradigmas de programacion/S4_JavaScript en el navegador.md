# SECCION 4: JavaScript en el navegador
## 1. Módulos JavaScript
En este vídeo se abordó el tema de los módulos en JavaScript ES6, explorando su función, operación y limitaciones, así como la forma de utilizarlos en un entorno de navegador. A continuación, se proporciona un resumen de los puntos clave:

1. **Introducción a los Módulos:**
   - Los módulos en JavaScript son unidades de código independientes que se pueden reutilizar en diferentes partes de una aplicación.
   - Antes de los módulos, JavaScript utilizaba funciones globales definidas en el objeto `window`, lo que podía generar problemas con bibliotecas de terceros y múltiples desarrolladores.

2. **Historia de los Módulos en JavaScript:**
   - Antes de ES6, no existían funciones de módulo nativas en JavaScript.
   - CommonJS fue un intento de solucionar este problema, pero no era compatible con los navegadores debido a su sintaxis específica.

3. **Módulos ES6:**
   - ES6 (ECMAScript 2015) introdujo módulos nativos en JavaScript, proporcionando una forma más clara y eficiente de organizar y reutilizar código.
   - La etiqueta de script en HTML ahora puede tener un atributo `type` con el valor "module" para indicar que el script es un módulo ES6.

4. **Uso Básico de Módulos ES6 en un Navegador:**
   - Se puede importar un módulo usando la palabra clave `import` seguida del nombre del archivo del módulo.
   - Ejemplo de etiqueta de script en HTML:

```html
<script type="module">
  import greeting from './greeting.js';
  console.log(greeting);
</script>
```

> **Consideraciones al Ejecutar Módulos Localmente:**
   - Al ejecutar archivos HTML localmente, puede surgir un error de política de misma origen (CORS) debido a restricciones de seguridad del navegador.
   - Se recomienda utilizar un servidor local para evitar este problema y permitir la correcta importación de módulos.
  - Los módulos en JavaScript ES6 proporcionan una forma organizada y reutilizable de estructurar el código.
   - Aunque los módulos ES6 son ampliamente compatibles, es importante tener en cuenta las consideraciones de seguridad al ejecutar localmente.

En conclusión, el vídeo ofrece una introducción clara al uso de módulos en JavaScript ES6, mostrando cómo importar y utilizar módulos básicos en un entorno de navegador.

## 2. Manipulación del DOM de JavaScript
En este fragmento, se explora el Document Object Model (DOM) de JavaScript, comparándolo con un control remoto de televisión que permite cambiar el contenido de una página web. El DOM es un modelo en forma de árbol que representa la estructura de una página web en la memoria del navegador.

Se muestra cómo interactuar con el DOM utilizando las DevTools del navegador y la consola de JavaScript. Se realiza un ejemplo práctico de manipulación del DOM, donde se crea dinámicamente un elemento `<h2>`, se le asignan atributos y contenido de texto, y finalmente, se añade al cuerpo del documento.

A continuación se presenta el código asociado:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ejemplo de Manipulación del DOM</title>
</head>
<body>
  <!-- Contenido de la página -->

  <script>
    // JavaScript para manipular el DOM
    const h2 = document.createElement('h2'); // Crear un elemento h2
    h2.innerText = 'Esto es un encabezado h2'; // Establecer el texto interno

    // Añadir atributos
    h2.setAttribute('id', 'sub-heading');
    h2.setAttribute('class', 'secondary');

    // Comprobar la estructura HTML
    console.log(h2);

    // Añadir al DOM
    document.body.appendChild(h2);
  </script>
</body>
</html>
```
> Este código demuestra la creación de un elemento `<h2>` con atributos y su inserción en el DOM de la página web. Al ejecutarlo, se observa cómo el nuevo elemento se añade y muestra en el navegador.

## 3. Selectores JavaScript
**Uso de selectores en JavaScript para localizar objetos específicos** en un documento. Algunos de los métodos mencionados incluyen:

1. **`document.querySelector`**: Permite seleccionar el primer elemento que coincide con un selector CSS dado. Por ejemplo:
   ```javascript
   document.querySelector('p'); // Selecciona el primer párrafo
   ```

2. **`document.querySelectorAll`**: Devuelve una NodeList de todos los elementos que coinciden con un selector CSS especificado. Por ejemplo:
   ```javascript
   document.querySelectorAll('p'); // Selecciona todos los párrafos
   ```

3. **`document.getElementById`**: Busca un elemento por su atributo `id`. Por ejemplo:
   ```javascript
   document.getElementById('heading'); // Selecciona el elemento con el ID 'heading'
   ```

4. **`document.getElementsByClassName`**: Devuelve una HTMLCollection de elementos que tienen el nombre de clase especificado. Por ejemplo:
   ```javascript
   document.getElementsByClassName('txt'); // Selecciona elementos con la clase 'txt'
   ```

Se enfatiza que los selectores proporcionan una forma eficiente de acceder y manipular elementos en el DOM, ya sea por etiquetas, IDs o clases. Además, se señala la diferencia en el uso de singular ("elemento") para IDs y plural ("elementos") para nombres de clase. Si un elemento no se encuentra, se devuelve `null` para IDs y una colección vacía para nombres de clase.

## 5. Gestión de eventos
**Escucha de Eventos en JavaScript:**

En JavaScript, los eventos, como hacer clic en un botón, son activados por el usuario y pueden ser gestionados mediante código. Puedes seleccionar las partes de una página donde deseas escuchar eventos y ejecutar código en respuesta. Un ejemplo sería escuchar un clic en un botón "Añadir al carrito" para actualizar el contador de artículos en el carrito.

**Controlador de Eventos y Método `addEventListener`:**

- Un controlador de eventos es una función de JavaScript que gestiona eventos capturados.
- El método `addEventListener` es utilizado para escuchar eventos en elementos HTML.

**Ejemplo Práctico:**

1. Uso de `addEventListener`:

```javascript
const target = document.querySelector('body');

function handleClick() {
    console.log("Se hizo clic en el cuerpo.");
}

target.addEventListener('click', handleClick);
```

2. Alternativa con Atributos de Eventos HTML:

```javascript
function handleClick2() {
    console.log("Se hizo clic en el encabezado.");
}
```

En la consola de desarrolladores:

- Si haces clic en el cuerpo, se activará `handleClick`.
- Si haces clic en el encabezado, se activarán ambos `handleClick` y `handleClick2`.


## 6. Notación de objetos JavaScript - JSON
**Conversión de JSON a Objeto JavaScript:**

Para convertir una cadena JSON a un objeto JavaScript, se utiliza el objeto global `JSON` incorporado y su método `parse`. Por ejemplo:

```javascript
const JSONstr = '{"saludo": "hola"}';
const aPlainObj = JSON.parse(JSONstr);
aPlainObj.saludo = "adiós";
```

**Conversión de Objeto JavaScript a JSON:**

Para convertir un objeto JavaScript a una cadena JSON, se utiliza el método `stringify` del objeto JSON. Por ejemplo:

```javascript
const datos = { nombre: "Juan", edad: 25 };
const JSONstring = JSON.stringify(datos);
```

> **Consideraciones Importantes:**
- JSON no admite funciones ni comentarios JavaScript.
- Al aplicar `stringify` a un objeto que contiene un método, este se excluye.
- La representación JSON tiene claves y valores entre comillas dobles.
    - Estas conversiones son útiles al trabajar con datos de APIs, proporcionando un flujo de trabajo estándar para acceder y manipular propiedades de objetos mediante programación.
