# SECCION 3: Funciones avanzadas de JavaScript
## 1. Desestructuración de matrices y objetos
En este video se aborda la desestructuración de objetos y matrices en JavaScript. Se emplea la analogía de copiar formato de un texto a otro para explicar cómo se pueden extraer propiedades de objetos y crear variables independientes. Se destaca la importancia de la ortografía correcta al utilizar la palabra clave `let` para desestructurar propiedades.

A través de un ejemplo con el objeto matemático incorporado, se demuestra la desestructuración de la propiedad `PI` y se enfatiza la falta de conexión entre la variable desestructurada y la propiedad original. El código utilizado se centra en la palabra clave `let` y la comparación estricta (`===`) para verificar la independencia de las variables.

## 2. Bucles `for-in` y `for-of` en Objetos

En este video se explora la diferencia entre los bucles `for-in` y `for-of` al aplicarse a objetos en JavaScript. Se presenta un ejemplo con un objeto "coche" y un "coche deportivo" que hereda propiedades. Se utiliza un bucle `for-in` para iterar sobre propiedades, señalando su falta de fiabilidad al incluir propiedades del prototipo.

Se introduce el bucle `for-of`, que itera solo sobre las propiedades propias del objeto, proporcionando una salida más predecible. Se presenta una versión simplificada del código para resaltar las diferencias entre ambos bucles.

## 4. Trabajar con literales de plantilla

Este video se centra en la creación y uso de literales de plantilla en JavaScript ES6. Se inicia con una comparación de las limitaciones de las cadenas en ES5, destacando la falta de soporte para cadenas multilínea. Se presenta el concepto de literales de plantilla, permitiendo la creación de cadenas multilínea con comillas inversas.

Se explora la flexibilidad de los literales de plantilla al añadir líneas sin problemas de concatenación. Además, se muestra cómo realizar la interpolación de variables dentro de literales de plantilla, proporcionando una forma más efectiva y clara de construir cadenas.

Los códigos específicos no se proporcionaron, pero se mencionan elementos clave como la palabra clave `let`, la comparación estricta (`===`), y el uso de comillas inversas para literales de plantilla.


## 4. Estructuras de datos

Antes de codificar un programa para calcular la calificación promedio de exámenes de estudiantes, es crucial pensar en cómo representar los datos y cómo nombrar la solución. Las estructuras de datos en JavaScript, como objetos, arrays, mapas y conjuntos, son fundamentales para organizar los datos. Cada estructura se adapta a diferentes necesidades. Por ejemplo, los objetos son útiles para pares clave-valor, mientras que las matrices son ideales para colecciones ordenadas. Los mapas permiten claves de cualquier tipo, y los conjuntos garantizan elementos únicos.

## 5. Operador de dispersión

El operador de dispersión (spread) en JavaScript (ES6) simplifica la tarea de pasar elementos de matrices a funciones. Utilizando tres puntos (`...`), el operador de dispersión puede propagar elementos de una matriz, facilitando la llamada a funciones con varios argumentos. Comparado con enumerar manualmente cada elemento de la matriz al llamar a una función, el operador de dispersión ofrece una sintaxis más clara y concisa.

## 6. Operador de descanso

El operador de descanso (rest) permite construir estructuras de datos más pequeñas empaquetando elementos. En el contexto de una matriz, el operador de descanso puede extraer una parte específica y almacenar el resto en otra variable. Por ejemplo, se puede utilizar en la desestructuración para dividir una lista de destinos turísticos en dos grupos. Además, el operador de descanso es útil en funciones, permitiendo manejar un número variable de argumentos y facilitando la manipulación de datos dentro de la función.
