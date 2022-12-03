## Obtentencion y Modificacion de Childs (hijos)
---

- firstChild (no recomendable)
- lastChild (no recomendable)
- firstElementChild
- lastElementChild
- childNodes
- children

`Partiendo de este Ejemplo de HTML ->`
```html
<div class="contenedor">
        <h2>un h2 comun</h2>
        <h4>un h4 comun</h4>
        <p>un simple parrafo</p>
</div>
```
---
- Ejemplo de firstChild:
```js
const contenedor = document.querySelector(".contenedor");

const primerHijo = contenedor.firstChild; // de esta manera accedemos al primer hijo de "contenedor", en este caso es texto ya que en el archivo HTML se deja espacio para que sea semanticamente ordenado a la vista.

console.log(primerHijo); // ejecutamos en consola
```
- Ejemplo de lastChild:
```js
const contenedor = document.querySelector(".contenedor");

const ultimoHijo = contenedor.lastChild; //  de esta manera llamamos al ultimo hijo de "contenedor", en este caso tambien puede ser texto debido a la colocacion de las etiquetas

console.log(ultimoHijo); // ejecutamos en consola
```
- Ejemplo de firstElementChild:
```js
const contenedor = document.querySelector(".contenedor");

const primerHijo = contenedor.firstElementChild; // de esta manera estamos llamando al primer Elemento de "contenedor", en este caso seria <h2>un h2 comun</h2>

console.log(primerHijo); // ejecutamos en consola
```
- Ejemplo de lastElementChild:
```js
const contenedor = document.querySelector(".contenedor");

const ultimoHijo = contenedor.lastElementChild; // de esta manera estamos llamando al ultimo Elemento de "contenedor", en este caso seria <p>un simple parrafo</p>

console.log(ultimoHijo); // ejecutamos en consola
```
- Ejemplo de childNodes:
```js
const contenedor = document.querySelector(".contenedor");

const hijos = contenedor.childNodes; // de esta manera estamos diciendo que nos muestre todos los hijos que tiene "contenedor".

console.log(hijos); // ejecutamos en consola
```
- Ejemplo de children:
```js
const contenedor = document.querySelector(".contenedor");

const hijos = contenedor.children; // de esta manera estamos diciendo que nos devuelva TODOS los hijos ELEMENTOS que tiene "contenedor".

console.log(hijos); // ejecutamos en consola
```
---


`datos extras:`

- `childNodes` no es un array, pero se puede recorrer con forEach()

```js
const contenedor = document.querySelector(".contenedor");
const hijos = contenedor.childNodes;

hijos.forEach(hijo => console.log(hijo));

console.log(hijos); // de esta forma estamos recorriendo un objeto (childNodes).
```
---
- `children` tampoco es un array, y en este caso no se usa forEach(), porque la coleccion html no se puede recorrer.

```js
const contenedor = document.querySelector(".contenedor");
const hijos = contenedor.children;

for (hijo in hijos){ // se usa "in" para recorrer el indice y se usa "of" para recorrer el valor de cada elemento.
    console.log(hijo);
}
```