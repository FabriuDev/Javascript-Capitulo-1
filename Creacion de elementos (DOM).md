## Creacion de elementos
---
- createElement()
- createTextNode()
- appendChild()
- createDocumentFragment()
---

- Ejemplo 1:
```js
const contenedor = document.querySelector(".contenedor");

const item = document.createElement("LI"); // sirve para crear un elemento HTML y siempre se usa en MAYUSCULAS.

item.innerHTML = "esto es un item de la lista"; // esto sirve para crear un texto dentro del elemento LI

contenedor.appendChild(item); // usamos appendChild para agregar un hijo al padre, es decir estamos agregando al "item" el elemento LI y al mismo tiempo el innerHTML esta colocando un texto, al ejecutar esta accion, se muestra un nodo dentro de otro nodo

console.log(item);

```

- Ejemplo 2:
```js
const contenedor = document.querySelector(".contenedor");

const fragmento = document.createDocumentFragment(); // crea un documento fragmentado con el contenido que le vayamos a asignar

for (i = 0; i < 20; i++){
    const item = document.createElement("LI");
    item.innerHTML = "esto es un item de la lista";
    fragmento.appendChild(item); // llamamos al fragmento + appendChild y como parametro le damos "item" para que coloque el texto que pusimos.
}

contenedor.appendChild(fragmento); // de esta manera llamamos a contenedor para que lo muestre en pantalla y en el codigo

console.log(contenedor); // ejecutamos contenedor en la consola.
```
