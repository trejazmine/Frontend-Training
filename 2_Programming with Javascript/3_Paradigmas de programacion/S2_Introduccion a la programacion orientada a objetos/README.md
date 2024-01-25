# SECCION 2: Introduccion a la programacion orientada a objetos

## 1. Introduccon a la programacion orientada a objetos

1. **Paradigmas de Programación:**
   - Los paradigmas de programación son clasificaciones o estilos de escribir código.
   - Se introduce el paradigma de Programación Orientada a Objetos (POO).
   - Contraste con la Programación Funcional: en POO, se organizan programas mediante objetos que agrupan datos y funciones relacionados.

2. **Ejemplo de Programación Funcional y POO:**
   - Se plantea el problema de calcular el costo total de comprar un par de zapatos.
   - En Programación Funcional, se separan claramente los datos de las funciones.
   - En POO, se crea un objeto (ej. purchase1) que contiene datos (variables) y funciones (métodos).

3. **Uso de `this` en Programación Orientada a Objetos:**
   - Se introduce la palabra clave `this` para referirse al objeto actual.
   - Ejemplo de cómo `this` simplifica el acceso a las propiedades y métodos del objeto actual.

4. **Reutilización de Código y Plantillas:**
   - Se muestra cómo mejorar la eficiencia reutilizando el mismo método en varios objetos.
   - Se destaca el uso de plantillas y cómo la palabra clave `this` contribuye a la reutilización de código.

```javascript
// Código de ejemplo de Programación Orientada a Objetos con `this`
function Purchase(shoes, tax) {
  this.shoes = shoes;
  this.tax = tax;
  this.totalPrice = function () {
    return this.shoes * (1 + this.tax);
  };
}

// Creación de objetos
let purchase1 = new Purchase(100, 0.2);
let purchase2 = new Purchase(50, 0.1);

console.log(purchase1.totalPrice()); // Output: 120
console.log(purchase2.totalPrice()); // Output: 55
```

## 2. Clases
1. **Introducción a Clases:**
   - Se necesitan clases para construir eficientemente muchos objetos con un conjunto específico de propiedades y métodos.
   - En JavaScript, las clases se crean con la palabra clave `class`, seguida del nombre de la clase y un constructor.

2. **Estructura de una Clase:**
   - Una clase tiene un constructor para asignar parámetros a las propiedades del objeto.
   - Pueden añadirse métodos a la clase sin la palabra clave `function`.

3. **Instanciación de Clases y Acceso a Métodos:**
   - Se muestra cómo instanciar una clase para crear un objeto.
   - Acceso a métodos de la clase en objetos instanciados mediante la notación de punto.

```javascript
// Código de ejemplo de uso de clases
class Purchase {
  constructor(shoes, tax) {
    this.shoes = shoes;
    this.tax = tax;
  }

  totalPrice() {
    return this.shoes * (1 + this.tax);
  }
}

// Creación de objetos
let purchase1 = new Purchase(100, 0.2);
let purchase2 = new Purchase(50, 0.1);

console.log(purchase1.totalPrice()); // Output: 120
console.log(purchase2.totalPrice()); // Output: 55
```

## 5. Herencia

1. **Herencia y Prototipos:**
   - La herencia en JavaScript está basada en prototipos.
   - El prototipo es un objeto que puede contener propiedades compartidas por varios objetos.
   - Se ilustra la herencia con un ejemplo usando un objeto `bird` y creando instancias como `eagle1` y `penguin1`.

2. **Uso de `Object.create` para Herencia:**
   - `Object.create` se utiliza para crear instancias de objetos que heredan propiedades de un prototipo.
   - La propiedad `can fly` se anula en `penguin1` para demostrar cómo se pueden anular propiedades heredadas.

3. **Sintaxis de Clases para Herencia:**
   - Aunque se puede usar `Object.create`, se sugiere el uso de la sintaxis de clases para herencias más complejas.
   - La sintaxis de clases en JavaScript sigue utilizando prototipos por debajo.

```javascript
// Código de ejemplo de herencia con prototipos
let bird = {
  hasWings: true,
  canFly: true,
  hasFeathers: true,
};

let eagle1 = Object.create(bird);
eagle1.canFly = true;

let penguin1 = Object.create(bird);
penguin1.canFly = false;

console.log(eagle1.canFly); // Output: true
console.log(penguin1.canFly); // Output: false
```

```javascript
// Código de ejemplo de herencia con clases
class Bird {
  constructor() {
    this.hasWings = true;
    this.canFly = true;
    this.hasFeathers = true;
  }
}

class Eagle extends Bird {
  constructor() {
    super();
    this.canFly = true;
  }
}

class Penguin extends Bird {
  constructor() {
    super();
    this.canFly = false;
  }
}

let eagle1 = new Eagle();
let penguin1 = new Penguin();

console.log(eagle1.canFly); // Output: true
console.log(penguin1.canFly); // Output: false
```

