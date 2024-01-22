
---

# CAPITULO 2: Arrays, objects and funtions
## Funciones
- Las funciones en JavaScript permiten agrupar un conjunto de instrucciones relacionadas bajo un nombre.
- El principio "DRY" (Don't Repeat Yourself) es esencial para evitar repeticiones en el código.

### a. Funciones Básicas
- Se presenta una función simple sin parámetros llamada `saludar`, que imprime "¡Hola, mundo!" en la consola.
```javascript
function saludar() {
console.log("¡Hola, mundo!");
}
saludar();  // Llamada a la función
```
### b. Funciones con Parámetros:**
- Se introduce la noción de parámetros en funciones para hacerlas más flexibles.
- Se muestra la función `sumarDosNumeros` que toma dos parámetros (a y b) y muestra la suma en la consola.
```javascript
function sumarDosNumeros(a, b) {
   let resultado = a + b;
   console.log(`La suma de ${a} y ${b} es: ${resultado}`);
}
sumarDosNumeros(10, 20);  // Llamada con argumentos
```
### c. Uso de Parámetros y Argumentos:**
- Se destaca que los parámetros actúan como variables dentro de la función.
- Los valores reales que se pasan a estos parámetros se llaman argumentos durante la llamada a la función.
```javascript
function sumarDosNumeros(a, b) {
   let resultado = a + b;
   console.log(`La suma de ${a} y ${b} es: ${resultado}`);
}
sumarDosNumeros(5, 7);  // Llamada con otros argumentos
```
## Almacenamiento de datos en matrices
Las matrices en JavaScript son utilizadas para almacenar y organizar secuencias de elementos.
Se compara el concepto con un tren de mercancías, donde cada vagón tiene un número y se coloca en una secuencia.
Las matrices permiten organizar y acceder a elementos de forma secuencial.
Evitan la necesidad de crear variables individuales para cada elemento, facilitando la gestión de colecciones.

- **Creación de una Matriz:**
  Se muestra cómo crear una matriz vacía utilizando la sintaxis de corchetes.
  ```javascript
  let tren1 = [];
  ```

- **Añadir Elementos a la Matriz:**
  Se añaden vagones al tren utilizando la misma variable `tren1`.
  ```javascript
  tren1 = ["trigo", "maíz", "carbón", "petróleo", "acero"];
  ```

- **Acceso a Elementos por Índice:**
  Se destaca que JavaScript asigna un número de índice a cada elemento de la matriz, comenzando desde 0.
  Se muestra cómo acceder al contenido de un vagón utilizando su número de índice.
  ```javascript
  let cargaDelVagon0 = tren1[0];  // Acceso al vagón 0 (trigo)
  ```
## Introducción a los objetos
En programación, los objetos se utilizan para relacionar grupos de datos.
Se utiliza un ejemplo de construcción de un personaje gerente de tienda en un juego de venta de galletas.
  -  ***Ejemplo 1:***
     Se introduce la creación de un objeto llamado `gerenteDeTienda` utilizando la notación de puntos.
     ```javascript
     gerenteDeTienda.movimiento = 5;
     gerenteDeTienda.habilidadesSociales = 8;
     ```
     
  -  ***Ejemplo 2:***
     Se construye un nuevo objeto llamado `subdirector` utilizando la notación literal del objeto.
     ```javascript
     var subdirector = {
       nombre: "Ejemplo",
       edad: 30,
       habilidades: ["ventas", "organización"]
     };
     ```

  -  ***Ejemplo 3:***
     Se muestra cómo añadir nuevas propiedades a un objeto existente utilizando la notación de puntos.
     ```javascript
     gerenteDeTienda.siguienteLogro = "Mejor Vendedor";
     subdirector.ubicacion = "Oficina Central";
     ```
## Fallos y errores
   - Exploración de la frustración causada por mensajes de error.
   - Diferenciación entre fallos y errores.

Ejemplo de Función sin Errores:
   ```javascript
   function sumarNumeros(a, b) {
     let resultado = a + b;
     console.log(resultado);
   }
   sumarNumeros(1, 2);  // Resultado esperado: 3
   ```

Ejemplo de Coerción y Error:
   ```javascript
   function concatenarCadenas(str, num) {
     let resultado = str + num;
     console.log(resultado);
   }
   concatenarCadenas("1", 2);  // Resultado inesperado: "12"
   ```

## Error de Referencia:
   ```javascript
   // Este código generaría un error de referencia
   console.log(variableNoDefinida);
   ```

### 5. Tipos Comunes de Errores:
   - Error de Tipo:
     ```javascript
     // Este código generaría un error de tipo
     let numero = 5;
     console.log(numero.pop());
     ```

### 6. Manejo de Errores en JavaScript:
   - Resalta que JavaScript intenta informar errores enviando mensajes a la consola.
   - Definición de errores como fragmentos de código defectuosos que impiden la ejecución.

### 7. Herramientas de JavaScript para Detectar Errores:
   - Menciona la importancia de las herramientas de JavaScript para detectar y manejar errores durante el desarrollo.

# Pruebe los bloques de captura

2. Uso de `try`, `catch`, y `throw`:
   - La sentencia `try` envuelve un bloque de código que puede lanzar un error.
   - La sentencia `catch` atrapa el error y ejecuta un bloque de código para manejarlo.
   - La palabra clave `throw` se utiliza para lanzar manualmente un error.

3. Ejemplo de Error de Referencia:
   ```javascript
   try {
     console.log(a + b);  // a y b no están definidas
   } catch (err) {
     console.error("Hubo un error:", err);
   }
   ```

4. Lanzar un Error Manualmente:
   ```javascript
   try {
     throw new ReferenceError("Hubo un error de referencia");
   } catch (err) {
     console.error("Error personalizado:", err.message);
   } finally {
     console.log("Mi programa no se detiene");
   }
   ```

5. Ventajas del Uso de `try` y `catch`:
   - Aunque un error ocurra, el programa no se detiene.
   - Ejemplo que demuestra que el código sigue ejecutándose después de un error.

## Valores indefinidos, nulos y vacíos
### 1. Tipo de Datos `null`
   - Representa la ausencia intencional de cualquier valor de objeto.
   - Se puede obtener como resultado de ciertos métodos integrados, como `match`.

### 2. Tipo de Datos `undefined`
   - Utilizado cuando un valor aún no está definido o no puede asignarse.
   - Ejemplos incluyen funciones que no devuelven nada, variables no asignadas, y asignación posterior.
 
- *** Diferencias y Escenarios de Uso ***
   - `null` y `undefined` se utilizan en situaciones específicas.
   - Ejemplos de cómo JavaScript asigna automáticamente `undefined` a variables no asignadas.

5. Valor de Marcador de Posición
   - `undefined` actúa como un marcador de posición para un valor no especificado pero reconocido por el motor de JavaScript.

6. Escenario de Objeto y Propiedad
   - `undefined` se obtiene al intentar acceder a una propiedad de un objeto que no existe.

### 3. Cadena Vacía
   - Una cadena sin caracteres en su interior.
   - Se puede construir con comillas simples o dobles sin caracteres entre ellas.
