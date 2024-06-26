JavaScript es un lenguaje de programación que se usa principalmente para hacer que las páginas web sean interactivas. Por ejemplo, cuando haces clic en un botón y algo cambia en la página sin tener que recargarla, eso es gracias a JavaScript. Es el lenguaje que le da vida a las páginas web, permitiendo animaciones, formularios interactivos, juegos, y muchas otras cosas divertidas y útiles.

Es flexible y permite escribir código rápidamente para crear funcionalidades en las páginas web. No necesitas especificar el tipo de datos que estás usando, lo cual puede ser más fácil al principio, pero a medida que tu proyecto crece, puede volverse más difícil de manejar.

### Variables

Las variables son contenedores que almacenan datos. En JavaScript, puedes declarar una variable usando `var`, `let`, o `const`.

- `var` fue la forma original de declarar variables, pero tiene algunos problemas con el alcance (scope).
- `let` se usa para variables que pueden cambiar.
- `const` se usa para variables que no deberían cambiar.

let nombre = "Juan";  // Una variable que puede cambiar
const edad = 30;      // Una variable que no debería cambiar

### Tipos de datos

JavaScript maneja varios tipos de datos, como:

- **Números**: Enteros o decimales. Ej: `42`, `3.14`
- **Cadenas de texto**: Texto dentro de comillas. Ej: `"Hola, mundo!"`
- **Booleanos**: Verdadero o falso. Ej: `true`, `false`
- **Arreglos**: Listas de elementos de cualquier tipo. Ej: `[1, 2, 3]` , `["alejandro", "sergio", "oscar"]` , `[ { nombre: "Juan", edad: 30 }, { nombre: "Juan 1", edad: 32 }, { nombre: "Juan 2", edad: 33 } ]` 
- **Objetos**: Colecciones de pares clave-valor. Ej: `{ nombre: "Juan", edad: 30 }`. Nombre es la clave y "Juan" es el valor.

### Operadores

Los operadores se usan para realizar operaciones sobre variables y valores.

- **Aritméticos**: `+`, `-`, `*`, `/`
- **De comparación**: `==`, `===`, `!=`, `!==`, `>`, `<` (el triple igual lo que hace es que compara el valor y si los tipos son iguales)
- **Lógicos**: `&&`, `||`, `!`

### Operadores de control

**Condicionales (if, else)**: Permiten ejecutar código basado en una condición

if (edad > 18) {
    console.log("Eres adulto.");
} else {
    console.log("Eres menor de edad.");
}

**Bucles (for, while)**: Permiten repetir código.

for (let i = 0; i < 5; i++) {
    console.log(i);  // Imprime 0, 1, 2, 3, 4
}

let j = 0;
while (j < 5) {
    console.log(j);  // Imprime 0, 1, 2, 3, 4
    j++;
}

### Funciones

Las funciones son bloques de código reutilizables que realizan una tarea específica. Se definen usando la palabra clave `function` y se llaman usando su nombre.

function saludar(nombre) {
    return "Hola, " + nombre + "!";
}

let mensaje = saludar("Juan");  // mensaje es "Hola, Juan!"
console.log(mensaje);

Otra manera de realizar funciones es con `arrow function` que es una forma concisa y moderna de escribir funciones en JavaScript. Se introdujo en ES6 (ECMAScript 2015) y proporciona una sintaxis más compacta en comparación con las funciones tradicionales.
Estas funciones pueden o no retornar algo.

// Sin parámetros
const funcionArrow = () => {
    // Cuerpo de la función
};

// Con un parámetro
const funcionArrowConParametro = (parametro) => {
    // Cuerpo de la función
};

// Con múltiples parámetros
const funcionArrowConMultiplesParametros = (param1, param2) => {
    // Cuerpo de la función
};

// Si el cuerpo de la función tiene una sola línea, no es necesario usar llaves ni la palabra return
const funcionArrowUnaLinea = () => console.log("Hola, mundo!");

Habiendo visto de manera rápida lo que es javascript realizaremos un ejercicio practico para ver como se utilizan todas estas partes. Iremos desarrollando el ejercicio por partes.

Ejercicio: 
Tu tarea es simular el proceso completo de realizar un pedido, desde la selección de productos hasta la actualización del estado del pedido y la gestión del inventario.

1 - Datos del cliente

![[Pasted image 20240626110723.png]]

2 - Establecer métodos de pago 

![[Pasted image 20240626110704.png]]

3 - Establecer productos

![[Pasted image 20240626110819.png]]

4 - Crear el pedido con su respectiva información

![[Pasted image 20240626110857.png]]

5 - Calcular el total del pedido

![[Pasted image 20240626111327.png]]

![[Pasted image 20240626111258.png]]

6 - Mostrar el detalle del pedido

![[Pasted image 20240626111606.png]]

![[Pasted image 20240626111405.png]]

![[Pasted image 20240626111922.png]]

7 - Pagar el pedido 

![[Pasted image 20240626111735.png]]
![[Pasted image 20240626111748.png]]
![[Pasted image 20240626112014.png]]

8 - Mostrar el pedido actualizado

![[Pasted image 20240626112408.png]]