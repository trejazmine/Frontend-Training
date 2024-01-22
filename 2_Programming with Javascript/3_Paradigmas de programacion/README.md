# CAPITULO 1: Introduccion a la programacion funcional
## Introducción a la programación funcional
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

## Valores de retorno de las funciones
Muchas funciones, por defecto, devuelven el valor deundefined.
Un ejemplo es la `funciónconsole.log()`.
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

## Llamada a funciones y recursividad

## Introducción al ámbito de aplicación

## El paradigma de la programación funcional

## Visual Studio Code en Coursera

## Ámbito con var, let y const

## Comparación de var, let y const

# CAPITULO 2: Introduccion a la programacion orientada a objetos

# CAPITULO 3: Funciones avanzadas de JavaScript

