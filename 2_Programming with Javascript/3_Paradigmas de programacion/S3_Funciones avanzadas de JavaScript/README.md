# SECCION 3: Funciones avanzadas de JavaScript
## 1. Desestructuración de matrices y objetos
- ***Desestructuración (destructuring)***: Es similar a copiar propiedades de un objeto o matriz y aplicarlas a otra. La desestructuración permite extraer valores de objetos o matrices de una manera más concisa. A continuación, se proporciona un resumen del código y los conceptos presentados:

```javascript
// Ejemplo de desestructuración de un objeto
let { pi: Pie } = Math;
console.log(Pie); // Resultado esperado: Valor de Math.pi

// Intento fallido de desestructuración con nombre de propiedad incorrecto
let { pi: piMinuscula } = Math;
console.log(piMinuscula); // Resultado: undefined

// Comparación de valores desestructurados y original
console.log(piMinuscula === Math.pi); // Resultado: false

// Actualización del valor desestructurado
piMinuscula = 1;
console.log(piMinuscula === Math.pi); // Resultado: false
```

En este ejemplo, se utilizó la sintaxis de desestructuración (`let { propiedad: nuevoNombre } = objeto`) para extraer el valor de `Math.pi` y asignarlo a una nueva variable llamada `Pie`. Además, se intentó desestructurar un nombre de propiedad incorrecto, lo que resultó en `undefined`. Luego, se compararon los valores desestructurados y el valor original, demostrando que no están conectados.

## 2. Bucles `for-in` y `for-of` en Objetos
- Ejemplo con dos objetos: `coche` y `cocheDeportivo`. `cocheDeportivo` hereda propiedades de `coche` y tiene una propiedad adicional llamada `velocidad` establecida en 'rápida'. Se utilizan dos bucles para iterar sobre las propiedades de `cocheDeportivo`.

1. **Bucle `for...in`**:
   - Itera sobre todas las propiedades del objeto y su prototipo.
   - Puede incluir propiedades heredadas, como `motor` y `direccion`.
   - Puede no ser fiable al iterar solo sobre las propiedades del objeto.

```javascript
for (let prop in cocheDeportivo) {
  console.log(prop); // Muestra propiedades del objeto y su prototipo
}
```

2. **Bucle `for...of`**:
   - Itera solo sobre las propiedades propias del objeto.
   - Utiliza `Object.keys()` para obtener un array de las propiedades.
   - Es más fiable al iterar solo sobre las propiedades del objeto.

```javascript
for (let prop of Object.keys(cocheDeportivo)) {
  console.log(prop, cocheDeportivo[prop]); // Muestra solo propiedades del objeto
}
```

## 4. Trabajar con literales de plantilla
1. **Cadenas en ES5:**
   - Se utilizan comillas simples o dobles para definir cadenas.
   - No admiten fácilmente cadenas multilínea.

```javascript
let noMultiLine = "did you know, no multi-line in ES5";
console.log("did you know," + noMultiLine);
```

2. **Literales de Plantilla en ES6:**
   - Se definen con comillas inversas (backticks).
   - Permiten la creación sencilla de cadenas multilínea.

```javascript
let multiLine = `Literal
de
Plantilla`;
console.log(multiLine);
```

3. **Interpolación de Variables:**
   - Se pueden combinar con variables y expresiones.
   - Se utilizan `${variable}` para interpolación.

```javascript
let first = "Hello";
let second = "world!";
let combined = `${first} from the ${second}`;
console.log(combined);
```

> Se resalta la flexibilidad y la eliminación de restricciones al utilizar literales de plantilla, lo que mejora la experiencia de codificación al simplificar la creación de cadenas y la interpolación de variables en comparación con los métodos convencionales de ES5.

## 5. Estructuras de datos
1. **Objetos:**
   - Colección no iterable de pares clave-valor.
   - Útil para almacenar y acceder a valores bajo una clave.
   - Se utiliza en programación orientada a objetos.

```javascript
let student = {
  name: "John",
  grade: 90
};
```

2. **Arrays:**
   - Colección iterable ordenada de valores.
   - Útil para almacenar y acceder a valores bajo un índice.
   - Se trabaja comúnmente con bucles (e.g., `for`) para acceder y manipular datos.

```javascript
let grades = [90, 85, 92, 88];
```

3. **Mapas:**
   - Colección iterable de pares clave-valor.
   - Las claves pueden ser de cualquier tipo, no solo cadenas como en los objetos.

```javascript
let gradeMap = new Map();
gradeMap.set("John", 90);
gradeMap.set("Jane", 85);
```

4. **Conjuntos:**
   - Colección donde cada elemento debe ser único.
   - Útil cuando se requiere mantener elementos únicos.

```javascript
let uniqueGrades = new Set([90, 85, 90, 92]);
```

## 6. Operador de dispersión
El operador de dispersión (`spread operator`) es una característica incorporada en la actualización ES6 del lenguaje. Este operador, representado por tres puntos (`...`), se presenta como una herramienta versátil para copiar propiedades de objetos y combinar elementos de matrices. Se ilustra su utilidad a través de un ejemplo práctico.

1. **Definición del Operador de Dispersión:**
   - El operador de dispersión se representa por tres puntos (`...`).
   - Actúa como una herramienta para copiar propiedades de objetos y combinar elementos de matrices.

2. **Uso con Matrices:**
   - Se comienza creando una matriz (`top3`) que contiene los tres mejores lugares para visitar en Roma.
   - Se define una función (`showItinerary`) que lista los lugares a visitar usando argumentos individuales.
   - La función se invoca utilizando el operador de dispersión con la matriz (`top3`), evitando enumerar manualmente cada elemento.

```javascript
let top3 = ["Coliseo", "Fontana de Trevi", "Ciudad del Vaticano"];

function showItinerary(lugar1, lugar2, lugar3) {
  console.log(`Visita ${lugar1}, luego visita ${lugar2}, y termina con una visita a ${lugar3}.`);
}

showItinerary(...top3);
```

3. **Ventajas del Operador de Dispersión:**
   - Simplifica la sintaxis al pasar elementos de una matriz a una función.
   - Evita enumerar manualmente cada elemento.

4. **Uso con Otras Matrices:**
   - Se demuestra cómo el operador de dispersión simplifica la llamada a la función con una matriz diferente (`top7`) que contiene siete lugares.

```javascript
let top7 = ["Lugar1", "Lugar2", "Lugar3", "Lugar4", "Lugar5", "Lugar6", "Lugar7"];

// Usando el operador de dispersión
showItinerary(...top7);
```

> En resumen, el operador de dispersión facilita la manipulación de elementos en matrices y mejora la claridad y concisión del código al evitar la necesidad de enumerar manualmente cada elemento al pasarlos a funciones.

## 7. Operador de descanso
El operador rest se utiliza para construir una "caja más pequeña" al empaquetar elementos en ella. A través de ejemplos prácticos, se ilustra cómo el operador rest puede ser útil, especialmente en situaciones en las que se necesita extraer solo algunos elementos de un conjunto más grande.

1. **Definición del Operador Rest:**
   - El operador rest se utiliza para empaquetar elementos en una estructura más pequeña, como un array.
   - Se representa con tres puntos (`...`).

2. **Uso del Operador Rest en un Itinerario de Viaje:**
   - Se crea una matriz (`top7`) con siete lugares que se desean visitar en Roma.
   - Se utiliza la desestructuración con el operador rest para organizar la lista, extrayendo los tres primeros lugares y el resto.
   - Ejemplo:

```javascript
const top7 = ["Coliseo", "Foro Romano", "Vaticano", "Fontana de Trevi", "Panteón", "Plaza Venecia", "Colina Palatina"];

const [first, second, third, ...secondVisit] = top7;

console.log(first); // "Coliseo"
console.log(second); // "Foro Romano"
console.log(third); // "Vaticano"
console.log(secondVisit); // ["Fontana de Trevi", "Panteón", "Plaza Venecia", "Colina Palatina"]
```

3. **Uso del Operador Rest en Funciones:**
   - Se crea una función (`addTaxToPrices`) que utiliza el operador rest como parámetro.
   - El operador rest agrupa el resto de los parámetros en una lista dentro de un array.
   - Se utiliza el método `map` para aplicar el tipo impositivo a cada artículo comprado.
   - Ejemplo:

```javascript
function addTaxToPrices(taxRate, ...itemsBought) {
  return itemsBought.map(item => `${item} with tax: ${(item * (1 + taxRate)).toFixed(2)}`);
}

const result = addTaxToPrices(0.1, 20, 30, 40);

console.log(result);
// ["20 with tax: 22.00", "30 with tax: 33.00", "40 with tax: 44.00"]
```

4. **Consideraciones Importantes:**
   - El parámetro rest debe ser el último en la definición de la función.
   - Cualquier otro parámetro después del operador rest resultará en un error.

> En resumen, el operador rest es una herramienta útil para agrupar el resto de los parámetros en una lista dentro de un array estándar de JavaScript. Se muestra su aplicación tanto en la manipulación de matrices como en funciones que requieren una cantidad variable de argumentos.


