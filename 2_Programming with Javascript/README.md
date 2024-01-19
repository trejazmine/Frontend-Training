# PROGRAMMING WITH JAVASCRIPT
## 1. Bienvenido a la programacion
### Comentarios
- Comentarios de una sola línea 
```javascript
// this is a comment!
```
- Comentarios multilínea
```javascript
/*
this
is
a
multi-line
comment
*/
```
- En la **consola** de **Herramientas para desarrolladores** colocamos:
  ```javascript
  console.log("Hello, World");
  console.log("Hello, World"); //En este fragmento de código, hay algunos añadidos: el tamaño de la fuente es diferente y el color es azul: 
  ```
### a. Variables
```javascript
var person = " John"; // declaracion de variable/asigancion de valor 
console.log("Hello", person);

```
### Tipos de datos
- Cadena (String): Ideal para almacenar valores de texto como nombres y descripciones. Se deben usar comillas simples o dobles para construir cadenas.
- Número (Number): Adecuado para almacenar valores numéricos, como precios. Tiene un rango amplio, pero está limitado por las capacidades de cálculo de JavaScript.
- Booleano (Boolean): Con solo dos valores posibles (verdadero o falso), es útil para la toma de decisiones en el código.
- Nulo (Null): Representa la ausencia de valor y se utiliza cuando se desea indicar explícitamente que una variable no tiene ningún valor.
- Indefinido (Undefined): Se refiere a una variable a la que aún no se le ha asignado ningún valor.
- BigInt: Introducido en ES6, es adecuado para manejar números más grandes que el tipo de datos number.
- Símbolo (Symbol): Se utiliza como identificador único y es útil para evitar confusiones al tener varias cajas con la misma etiqueta.
### Operadores
#### a. Operadores de asignación (aritmética):
- Suma: +
- Resta: -
- Multiplicación: *
- División: /

#### b. Operadores de comparación:
- Mayor que: >
- Menor que: <
- Igual a: == (se utiliza dos veces)
- Igualdad estricta: ===
- Diferente de: !=
- Desigualdad estricta: !==
- Asignación de suma:+=

#### c. Operadores lógicos:
- AND (&&): Verifica que dos o más condiciones sean verdaderas.
- OR (||): Verifica que al menos una de las condiciones sea verdadera. 
- NOT (!): Devuelve un valor falso si el resultado es verdadero.

```javascript
console.log(2+2); //4
console.log(18-10); //2
console.log(8*5); //40
console.log(10/2); //5
console.log(1>2); //false
console.log(10==10); //true
```
### Números
#### a. Números enteros y decimales
   - `123`: Representa un número entero.
   - `123.456`: Representa un número decimal.

#### b. Operaciones matemáticas básicas
   - Suma: `2 + 2` devuelve `4`.
   - Resta: `4 - 2` devuelve `2`.
   - Multiplicación: `4 * 4` devuelve `16`.
   - División: `16 / 4` devuelve `4`.
   - Exponenciación: `10 ** 2` (10 a la potencia de 2) devuelve `100`.
   - Resto (Módulo): `9 % 8` devuelve `1`, y `16 % 8` devuelve `0`.

#### c. Uso de paréntesis para controlar el orden de las operaciones
   - `(2 * 4) + 8` devuelve `16`.
   - `2 * (4 + 8)` devuelve `24`.

### Strings (cadenas)
Es una colección de caracteres encerrados entre comillas simples, comillas dobles. 
Tal colección de caracteres se conoce como ***tipo de datos cadena***. 
- ***¿Qué ocurre cuando se utiliza el operador + sobre dos cadenas?*** Se unen en una sola cadena.
- ***¿Qué ocurre cuando se utiliza el operador + sobre una cadena y un número?*** Se unen en una sola cadena.
  
  ### Booleanos
Este tipo de dato se utiliza para evaluar si una afirmación es verdadera o falsa.
```javascript
var score = 100;
score //100

100 == "100" // true (compara solo el valor)
100 === "100" // false (strict equality operator: compara el valor y tipo de dato)

1 != 1 // true (compara solo el valor)
1 !== "1" // false (compara el valor y tipo de dato)
```

## 2. Condicionales y bucles
### Declaraciones escritas
#### a. Sentencia if
La sentencia `if` comprueba una condición y ejecuta un bloque de código si la condición es verdadera.
```javascript
let resultadoExamen = 45;

if (resultadoExamen > 40) {
  console.log("¡Aprobado!");
}
```
#### b. Sentencia if-else
La sentencia `if-else` maneja dos resultados posibles de una condición. Si la condición es verdadera, se ejecuta un bloque; de lo contrario, se ejecuta otro bloque. Ejemplo:
```javascript
let resultadoExamen = 35;

if (resultadoExamen > 40) {
  console.log("¡Aprobado!");
} else {
  console.log("No ha aprobado.");
}
```
#### c. Sentencia else-if
Cuando se necesitan múltiples condiciones, se utiliza `else-if` para agregar bloques adicionales de comprobación. Por ejemplo:
```javascript
let resultadoExamen = 25;

if (resultadoExamen > 40) {
  console.log("¡Aprobado!");
} else if (resultadoExamen > 30) {
  console.log("Aprobado, pero puede mejorar.");
} else {
  console.log("No ha aprobado.");
}
```
### Enunciados condicionales
#### a. Sentencia if-else
Se utiliza para ejecutar bloques de código basados en si una condición es verdadera o falsa.
 ```javascript
 let resultado = 50;
 
 if (resultado > 40) {
   console.log("Pasa la prueba");
 } else {
   console.log("No pasó la prueba");
 }
 ```

#### b. Sentencia switch
   - Se utiliza cuando hay múltiples condiciones y se quiere comparar un valor con varios casos posibles.
 ```javascript
 let place = "first";
 
 switch (place) {
   case "first":
     console.log("Gold");
     break;
   case "second":
     console.log("Silver");
     break;
   case "third":
     console.log("Bronze");
     break;
   default:
     console.log("No medal");
 }
 ```
- **Sintaxis de switch**
    - La sentencia switch evalúa una expresión y ejecuta el bloque de código correspondiente al caso que coincide con el valor de la expresión.
    - Se utiliza `break` para salir de la sentencia switch después de que se ejecuta un caso.
    - El bloque `default` se ejecuta si ninguno de los casos coincide.

##### *Diferencias y consideraciones:*
- La sentencia if-else puede volverse inmanejable con múltiples condiciones, especialmente si son muchas.
- La sentencia switch proporciona una forma más estructurada de manejar múltiples casos.
- Ambas estructuras son útiles en diferentes situaciones, y la elección entre ellas depende del contexto y la legibilidad del código.

### Bucles 
Son herramientas fundamentales para ejecutar tareas repetitivas. Comparados con las sentencias condicionales que ejecutan bloques de código una vez, los bucles permiten repetir el mismo bloque hasta que se cumple una condición.
- **Contador en Bucles**: El contador, también conocido como incrementador, es esencial en bucles. Actúa como un marcador que indica cuándo iniciar y terminar el bucle. En JavaScript, es común utilizar la letra "i" como contador.
#### a. Bucle For
El bucle `for` es estructurado y se utiliza para repetir un bloque de código un número específico de veces. Su estructura incluye la inicialización del contador, una condición y un incremento o decremento del contador.
```javascript
for (let i = 1; i <= 100; i++) {
  console.log(i);
}
```
#### b. Bucle While
El bucle while es similar al for. Se ejecuta mientras una condición sea verdadera, y el incremento del contador se realiza dentro del cuerpo del bucle.
```javascript
let i = 1;
while (i <= 100) {
  console.log(i);
  i++;
}
```
##### *Elección entre For y While:* 
- Tanto el bucle for como el while pueden lograr los mismos resultados. Sin embargo, algunos desarrolladores prefieren el for debido a su estructura autocontenida.

### Bucle FOR
- La estructura básica del bucle `for` consta de tres partes: el contador, la condición de salida y el incrementador. En el siguiente ejemplo, el bucle cuenta desde 1 hasta 3:
```javascript
//Este código cuenta desde 10 hasta 1 y luego imprime "¡Feliz Año Nuevo!".
for (let i = 10; i > 0; i--) {
  console.log(i);
}
console.log("¡Feliz Año Nuevo!");
```
  
### Bucle WHILE
- A diferencia del bucle `for`, el bucle `while` tiene algunas diferencias clave. En el bucle `while`, debes establecer el contador antes del bucle y especificar solo la condición de salida dentro de los paréntesis. Veamos un ejemplo:
```javascript
let contador = 3;
while (contador > 0) { //bloque de código dentro del bucle se ejecutará mientras la condición sea verdadera
  console.log(contador);
  contador = contador - 1;
}
console.log("¡Feliz Año Nuevo!");
```
### Bucles anidados
Cuando necesitas realizar más de una tarea al mismo tiempo, como procesar dos conjuntos de datos diferentes, puedes usar bucles anidados en JavaScript. Los bucles anidados te permiten colocar un bucle dentro de otro, ejecutando así múltiples tareas en paralelo.
```javascript
// Supongamos que estás creando un plan de dos semanas, donde necesitas imprimir la salida de cada número de día asociado a la semana. Utilizar bucles anidados es ideal para este escenario. Aquí hay un ejemplo práctico con bucles `for`:
for (let semana = 1; semana <= 2; semana++) {
  for (let dia = 1; dia <= 5; dia++) {
    console.log(`Semana ${semana}, Día ${dia}`);
  }
}
```

```javascript
// Otro ejemplo demuestra cómo usar bucles anidados para visualizar los meses de verano a lo largo de dos años:
for (let year = 2023; year < 2025; year++) {
  console.log(`Año: ${year}`);
  for (let mes = 6; mes < 9; mes++) {
    console.log(`-- ${mes}`);
  }
}
// Este código imprimirá los años 2023 y 2024, junto con los meses de verano (junio, julio, agosto) para cada año.
```
