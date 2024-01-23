# SECCION 1: Introduccion a la programacion funcional
## 1. Introducción a la programación funcional
Código de ejemplo:
```javascript
// Declaración de variables
var currencyOne = 100;
var currencyTwo = 0;
var exchangeRate = 1.2;

// Función de conversión de divisas
function convertirDivisa(importe, tasa) {
    return importe * tasa;
}

// Asignación del resultado a currencyTwo
currencyTwo = convertirDivisa(currencyOne, exchangeRate);

// Registro en la consola
console.log(currencyTwo); // Resultado esperado: 120
```

## 2. Valores de retorno de las funciones
Muchas funciones, por defecto, devuelven el valor deundefined. Un ejemplo es la `funciónconsole.log()`.
Dado que la función `console.log()` está construida de forma que no tiene el valor de retorno establecido explícitamente, obtiene el valor de retorno por defecto de `undefined`.

Ahora codificaré mi propia implementación de `console.log()`, que no devuelve el valor de `undefined`:
```javascript
function consoleLog(val) {
    console.log(val)
    return val
}
```
Estoy utilizando la funciónconsole.log() dentro de mi declaración de función personalizadaconsoleLog. Y estoy especificando que devuelva el valor de su argumento.

-***¿Por qué es útil esto?*** Es útil porque puedo utilizar valores de retorno de una función dentro de otra función.

-***¿Qué significa todo esto?*** Significa que al permitirme JavaScript utilizar la palabra clave `return` como se ha descrito anteriormente, puedo tener múltiples llamadas a funciones, devolviendo datos y manipulando valores, basándome en cualquier reto de codificación que tenga ante mí. Poder devolver valores personalizados es uno de los fundamentos que hacen posible la programación funcional.

## 3. Llamada a funciones y recursividad
- ***Ejemplo:*** Inicialmente crea un bucle infinito. Luego, se mejora la función introduciendo una condición de parada con una instrucción `if`. El código resultante registra los números 3, 2, 1 y luego se detiene, ilustrando la **recursión**.

    Código de ejemplo:
    ```javascript
    // Función recursiva sin condición de parada
    function example() {
        console.log("1");
        console.log("2");
        console.log("3");
        example(); // Bucle infinito
    }
    
    // Mejora con condición de parada
    let counter = 3;
    
    function exampleImproved() {
        console.log(counter);
        counter--;
    
        if (counter === 0) {
            return;
        }
    
        exampleImproved();
    }
    
    // Llamada a la función mejorada
    exampleImproved();
    ```

- Este código muestra la diferencia entre una función recursiva sin condición de parada y una versión mejorada que se detiene después de imprimir los números 3, 2, 1.

## 4. Ámbito con var, let y const
El alcance determina la accesibilidad del código y qué partes del programa pueden acceder a diferentes partes del código.

### a. Tipos de Ámbito
   - **Global:** Todo el código fuera de las funciones.
   - **Local:** Código dentro de una función. Solo se puede acceder a variables en la función en la que se declaran.

### b. Ámbito de Bloques (ES6)
   - Introducción del ámbito de bloques en ES6.
   - Las variables declaradas con `let` o `const` tienen alcance dentro del bloque de código donde se crean.
   - No pueden ser accedidas desde fuera del bloque.

### `var` (ES5)
   - Antes de ES6, la única opción era declarar variables con la palabra clave `var`.
   - Características:
      - Puede usarse antes de declararla (hoisting).
      - Puede ser redeclarada en el mismo ámbito.
      - Su ámbito es global si se declara fuera de una función.

### c. Diferencias entre `var`, `let` y `const` (ES6)
   - Sintaxis similar entre `var`, `let` y `const`, con el cambio de la palabra clave.
   - `let` y `const` son más estrictos que `var`.
   - No se puede usar una variable `let` o `const` antes de declararla.
   - Pueden ser redeclaradas con `let` y no con `const`.
   - `let` y `const` están limitadas al bloque.

### c. Recomendaciones de Uso
   - Sugerencia de usar `let` si el valor puede cambiar y `const` si el valor es constante.
   - Se aconseja a los nuevos desarrolladores recordar esta regla para elegir entre `var`, `let` y `const`.

**Código de Ejemplo:**
```javascript
// ES5 con var
var user = "Miranda";

// ES6 con let o const
let userES6 = "Miranda";
const pi = 3.14;
```
- Este código ilustra la sintaxis de declaración de variables en ES5 con `var` y en ES6 con `let` y `const`.

## 5. Comparación de var, let y const
- **`var`**
   - Se puede acceder a una variable declarada con `var` antes de la inicialización.
   - Ejemplo de intentar acceder a una variable no declarada (`console.log(user)`), lo que genera un error de referencia.
   - Se puede declarar y volver a declarar la misma variable `var` sin errores.

- **`let`**
   - No se puede acceder a una variable `let` antes de declararla.
   - La redeclaración de una variable `let` genera un error de sintaxis.
   - Puede reasignarse después de ser declarada.

- **`const`**
   - Debe inicializarse al declararla; de lo contrario, arroja un error de sintaxis.
   - Se puede acceder a una variable `const` antes de la inicialización, pero se obtiene una referencia indefinida.
   - No se puede redeclarar ni reasignar; genera errores de tipo.

***Recomendaciones:***
   - Comparación de las palabras clave `var`, `let` y `const`.
   - Var es más indulgente, let es más estricta y const es la más estricta.
   - Recomendación de elegir entre let y const según si se reasignarán o no los valores.
   - Sugerencia de practicar y elegir entre let o const en el JavaScript moderno.

**Código de Ejemplo:**
```javascript
// Ejemplo con var
console.log(user); // Error de referencia
var user = "Mark";
console.log(user); // Salida: Mark

// Ejemplo con let
// console.log(userLet); // Error de referencia
let userLet;
console.log(userLet); // Salida: undefined
userLet = "Anna";
// let userLet = "John"; // Error de sintaxis: El identificador 'userLet' ya ha sido declarado
console.log(userLet); // Salida: Anna

// Ejemplo con const
// const userConst; // Error de sintaxis: Falta el inicializador en la declaración const
// console.log(userConst); // Referencia indefinida
const userConst = "Alice";
// const userConst = "Bob"; // Error de sintaxis: La asignación a una variable constante está prohibida
console.log(userConst); // Salida: Alice
```
