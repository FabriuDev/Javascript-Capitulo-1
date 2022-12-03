# Metodos de Arrays
---
`Los metodos que se usan para transformar un array son los siguientes`
- pop() - elimina el ultimo elemento de un array y lo devuelve.
- shift() - elimina el primer elemento de un array y lo devuelve.
- push() - agrega un elemento al array al final de la lista.
- reverse() - invierte el orden de los elementos al inicio del array
- unshift() - agrega uno o mas elementos al inicio del array, y devuelve la nueva longitud del array.
- sort() - ordena los elementos de un array localmente y devuelve el array ordenado
- splice() - cambia el contenido de un array eliminando elementos existentes y/o agregando nuevos elementos
---
`Metodos accesores`
- join() - une todos los elementos de una matriz (u objeto similar) en una cadena y la devuelve.
- slice() - devuelve una parte del array dentro de un nuevo array empezando por inicio hasta fin (fin no incluido)
- Métodos ya vistos en cadenas: toString(), indexOf(), lastIndexOf(), includes()
---
filter() - crea un nuevo array con todos los elementos y los repite en bucle, sirve para hacer funciones tambien
forEach() - ejecuta la función callback una vez por cada elemento del array



            Todos los ejemplos de Metodos de Arrays:

> pop()
```js
let nombres = ["Juan","Coca","Jorge"]; // array


document.write("<b>Elementos originales: </b>" + nombres + "<br>");

let resultado = nombres.pop();// se asigna el metodo

document.write("Elemento removido: <b style='color:red'>" + resultado + "</b><br>");
document.write("Resultado: <b>" + nombres + "</b>");// explicado perfectamente en pantalla
```

> shift()
```js
let nombres = ["Juan","Coca","Jorge"];// array


document.write("<b>Elementos originales: " + nombres + "<br>");

let resultado = nombres.shift(); // se asigna el metodo

document.write("Elemento removido: <b style='color:red'>" + resultado + "</b><br>");
document.write("Resultado: <b>" + nombres + "</b>");
```

> push()
```js
let nombres = ["Juan","Coca","Jorge"];


document.write(nombres + "<br>");

let resultado = nombres.push("juancito");// nos agrega los array que queramos y nos dice la ubicacion de los mismos

document.write(resultado + "<br>");// si le pedimos el resultado nos dice la cantidad de elementos que hay
```

> reverse()
```js
let numeros = [1,2,3,4,5];

let resultado = numeros.reverse();// invierte el orden del array

document.write(resultado);
```

> unshift()
```js
let numeros = [3,4,5];// array original

document.write(numeros + "<br>");

numeros.unshift(0,1,2,);// lo que hace este metodo es agregarle numeros al array (los agrega al principio)

document.write(numeros);
```

> sort();
```js
let numeros = [1,7,2,6,3,4,,5,9];

document.write(numeros + "<br>");// original

numeros.sort();// sort transforma el array y lo ordena de mayor a menor, o en caso de las letras de la A - Z.

document.write(numeros);
```

> splice()
```js
let numeros = ["juan","coca","carlos","roberto","gustavo"];

document.write(numeros + "<br>");// original

numeros.splice(0,4,"nashe","tortilla","papanata"); // splice sirve para elegir de que parte queres empezar y hasta que parte queres eliminar, asi los remplazas con nuevos arrays.

document.write(numeros);

// explicacion mas compleja: el primer numero dentro de los parametros de splice, es el indicador de donde queremos empezar y el 2do numero es de donde queremos eliminar para colocar nuevos arrays para remplazar los anteriores, es decir si yo pongo splice.(0,2,"Hola","Chau"); - estoy diciendo que empiezo en el elemento 0 y empiezo a colocar los nuevos elementos despues del elemento 2 del array original.
```
---

> slice()
```js
let numeros = ["juan","coca","carlos","roberto","gustavo"];

document.write(numeros + "<br>");// original

let resultado = numeros.join("<br> Elemento: ");// join convierte los arrays en cadenas de texto, pero a diferencia de toString(), en join podes decir de que forma queres que se separen los arrays, puede ser con guiones, espacios o como vos quieras.

document.write("Elemento: " + resultado);
```

> Los siguientes metodos tambien funcionan en Arrays:
- toString();
- indexOf();
- lastIndexOf();
- includes();
---

> filter()
```js
let numeros = ["abecedario","manzana","pedro","pokemon","nashe","bobos"];// array

// filter esta usando como parametro una funcion flecha
let resultado = numeros.filter(numero => document.write(resultado + "<br>")); // cada vuelta que da el bucle filter, se ejecuta cada elemento del array y un espacio en linea (<br>) como muestra en el document.write
```

> filter() - crear un nuevo array:

```js
let numeros = ["abecedario","manzana","pedro","pokemon","nashe","bobos"];

let resultado = numeros.filter(numero => numero.length > 5);
 // cuando usamos length el array se transforma a un string, entonces nos dice que si cada string es mayor a 5 caracteres, se muestran en pantalla, y los que no cumplen con este requisito no se muestran.

document.write();
```
---