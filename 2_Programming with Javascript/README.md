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
  ### Declaraciones por escrito
  ### Enunciados condicionales
  ### Constructores en buble
  ### Bucle FOR
  ### Bucle WHILE
  ### Bucles anidados
