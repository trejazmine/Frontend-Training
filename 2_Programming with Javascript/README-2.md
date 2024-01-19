# Arrays, objects and funtions
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
