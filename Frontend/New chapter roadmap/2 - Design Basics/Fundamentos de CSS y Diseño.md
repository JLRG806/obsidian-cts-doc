
CSS es un lenguaje que define el diseño y disposición de páginas web. En otras palabras, CSS controla el aspecto de las páginas web cuando se cargan en un navegador. A este diseño lo llamamos el “estilo” de la página.

Diferencia entre HTML Y CSS

HTML (lenguaje de marcado de hipertexto) determina el contenido de una página web, incluidos texto, enlaces, imágenes, vídeos, etc. Un archivo HTML enumera todas las "cosas" de una página, pero no especifica cómo se ven cuando se muestran. mostrado en un navegador. CSS, como ahora sabemos, controla el estilo de estos elementos. CSS garantiza que el contenido HTML aparezca a los usuarios de la forma en que lo diseñaron los diseñadores. Quizás se pregunte: ¿Por qué separar estos dos lenguajes? Es una pregunta razonable. Ya que HTML y CSS funcionan juntos. La respuesta es que separar el estilo y el contenido hace que el desarrollo de sitios web sea mucho, mucho más fácil

Beneficios de usar CSS:

Menos codificación: los desarrolladores pueden usar CSS para aplicar el mismo estilo a varias páginas y elementos de página en un sitio web, lo que ahorra una gran cantidad de tiempo y reduce la posibilidad de errores

Más opciones de estilo: puedes hacer mucho con CSS, mucho más de lo que permitía el sistema de estilo HTML original

Mejor rendimiento: CSS reduce la cantidad de código de estilo repetitivo. Menos código significa archivos más pequeños, y archivos más pequeños significan tiempos de carga de página más rápidos.

La estructura de una regla de CSS luce así:

![[Pasted image 20240607085132.png]]

p { propiedad: valor }

si se quisiera agregar mas cosas a un solo selector, deberia ser asi: 
p { propiedad: valor ; (el punto y coma es importante) propiedad: valor ; propiedad valor }

En este ejemplo anterior podemos ver como se pueden agregar mas de dos declaraciones.

Y ahora, como conectamos el CSS a un HTML. 

Cada archivo de css puede tener un nombre en concreto pero siempre debe crearse con la extensión *css* como por ejemplo:

style.css. 

Importante la extensión *css* para que el archivo se interprete como una hoja de estilo.

En este caso llamaremos a nuestro archivo "mystyle.css" y haremos un par de ejemplos para mostrar como funciona el CSS.

`<!DOCTYPE html>`  
`<html>`  
`<head>`  
`<link rel="stylesheet" href="mystyle.css">`  
`</head>`  
`<body>`  
  
`<h1>This is a heading</h1>`  
`<p>This is a paragraph.</p>`  
  
`</body>`  
`</html>`

### Selectores Básicos

Existen 3 tipos de selectores:

De tipo, de clase e ID e Universales.

#### De tipo 
Se refieren a cuando se le quiere aplicar estilo a un elemento HTML de un cierto tipo especifico.

En este ejemplo mostraremos que desearemos que todos los párrafos de nuestro HTML sean rojos.

HTML
![[Pasted image 20240625123511.png]]

CSS
![[Pasted image 20240625122809.png]]

Resultado
![[Pasted image 20240607102919.png]]
#### De clase e ID

De clase: Los selectores de clase seleccionan todos los elementos que tienen una clase específica en el elemento HTML.

Los selectores de ID: Los selectores de ID seleccionan un solo elemento HTML que tiene un ID específico. Los IDs son y tiene que ser únicos dentro de un documento HTML.

Los selectores de clase: seleccionan todos los elementos que tienen una clase específica. Las clases se definen en el HTML usando el atributo `class`.

El selector universal: selecciona todos los elementos en una página web. Se denota con el asterisco `*`.

Para poder crear un ejemplo real en el que facilmente podemos ver en que podemos usar los ID y las clases y clases universales. Realizaremos el siguiente ejercicio.

Crearemos las figuras de lego he iremos identificando elementos y sabremos que podría ser un ID y una clase. 

![[Pasted image 20240607124021.png]]

Como mencionamos anteriormente un elemento que tiene ID es aquel elemento que tiene que ser único en todo el documento HTML, en este caso el navbar seria ese elemento y los elementos que tendrían una clase especifica serian las cartas de las figuras lego, por que todas tienen el mismo estilo y estructura.

Realizaremos parte por parte para ir logrando la landing que deseamos.

Parte 1 - Navbar

![[codetoimg-snippet.png]]

Resultado

![[localhost_5500_02%20-%20CSS_.png]]

Parte 2 - Cartas de figuras

Analizaremos la carta de la figura detenidamente y veremos los elementos que lo conforman. En este caso podemos ver que tiene:

- Un borde por toda la carta
- Dentro de la carta tiene dos elementos. Uno que es la imagen en si y el segundo elemento es una previa información de la figura.
- En el segundo elemento de la carta tiene 3 elementos. El primer elemento es un titulo, el segundo una descripción y el tercero un link para ir a ver a la información de la figura.

![[Pasted image 20240610111842.png]]

Sabiendo todos elementos que tiene este elemento vamos a ponerlo en practica.

Estructura HTML

![[codetoimg-snippet 1.png]]

Estilo de CSS

![[codetoimg-snippet (1).png]]

Resultado

![[Pasted image 20240610125133.png]]

Parte 3 - Estructurando la landing con las figuras

![[Pasted image 20240612095631.png]]
#### Universal 

El selector universal selecciona todos los elementos en una página web. Se denota con el asterisco `*`.
### Flexbox & Grid

Es un modelo de diseño CSS que proporciona una forma eficiente de distribuir elementos dentro de un contenedor y alinearlos de manera dinámica. La idea principal es darle al contenedor la capacidad de alterar el ancho/alto (y el orden) de sus elementos para llenar mejor el espacio disponible (principalmente para adaptarse a todo tipo de dispositivos y tamaños de pantalla).

![[Pasted image 20240612105044.png]]

Los elementos se distribuirán siguiendo el eje `main axis`(de `main-start`a `main-end`) o el eje transversal (de `cross-start`a `cross-end`).

Para definir que un contenedor sera flexible deberia de definirse asi:

![[Pasted image 20240612113953.png]]

La propiedad `flex-direction` indica la dirección los **hijos** del contenedor flexible.

![[Pasted image 20240612114145.png]]

Realizaremos el ejemplo de estas propiedad con las figuras de lego por que estos siguen en orden de dirección.

![[Pasted image 20240612115047.png]]

El div con el identificador `#new_lego_figures_collection_list` es el padre que su espacio es flexible. En este caso el primer ejemplo seria row, que en las fotos anteriores las cartas ya están en esa dirección.

![[Pasted image 20240612115950.png]]

En dirección **column**, los elementos seran ordenados en dirección vertical

![[Pasted image 20240612120401.png]]

En dirección **row-reverse**, los elementos seran ordenados alreves en dirección horizontal.

![[Pasted image 20240612120846.png]]

En dirección **column-reverse**, los elementos seran ordenados alreves en dirección vertical.

![[Pasted image 20240612120950.png]]

flex-wrap, es esa propiedad que se utiliza en un contenedor flexible para controlar si los elementos (hijos) dentro del contenedor deben permanecer en una sola línea o si pueden envolver a la siguiente línea si no hay suficiente espacio disponible. Su valor por defecto es **no-wrap**, esto quiere decir que si los hijos se encuentran en un row por ejemplo esa linea seguira y seguira creciendo horizontalmente sin ningun limite.

La propiedad `justify-content` es una propiedad que se aplica para controlar la alineación y distribución de los elementos flexibles a lo largo del eje principal del contenedor. El eje principal es determinado por la dirección en la que el contenedor flex está orientado (`flex-direction`).

A continuación aplicaremos las diferentes propiedades de `justify-content`

`justify-content: flex-start`

![[Screenshot 2024-06-17 at 10.58.01.png]]

`justify-content: flex-end`

![[Screenshot 2024-06-17 at 10.59.01.png]]

`justify-content: center`

![[Screenshot 2024-06-17 at 10.59.32.png]]

`justify-content: space-between`

![[Screenshot 2024-06-17 at 10.59.58.png]]

`justify-content: space-around`

![[Screenshot 2024-06-17 at 11.03.52.png]]

`justify-content: space-evenly`

![[Screenshot 2024-06-17 at 11.04.44.png]]

Si quieres seguir investigando mas sobre flexbox y seguir probando propiedades con el ejemplo que tenemos, aquí tienes mas información: https://css-tricks.com/snippets/css/a-guide-to-flexbox/ 
### Mobile First Design

El Mobile First Design es la metodología que busca adaptarse prioritariamente al formato mobile y a partir del cuál adaptaremos el resto de variantes al resto de dispositivos. Una metodología que busca adaptar la navegación en base al comportamiento del usuario, mayoritariamente activo a través de su dspositivo móvil.

La filosofía mobile first design, consiste en realizar una página web primero para móviles e ir adaptando el diseño para pantallas más grandes de menor a mayor tamaño. Permite centrarse en los elementos y acciones más importantes, crear una buena experiencia para el usuario y generar la mejor usabilidad posible.

(Demo de Mobile First Design, incluira Figma y Website)
