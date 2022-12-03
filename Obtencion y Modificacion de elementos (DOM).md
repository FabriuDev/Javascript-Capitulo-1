### Obtencion y modificacion de elementos
---
- `textContent` - devuelve el texto de cualquier nodo.

- `innerHTML` - devuelve el contenido html de un elemento.

- `outerHTML` - devuelve el código HTML completo del elemento.

---
`Ejemplo en HTML`
```html
<p class="titulo">Elemento a <b style="visibily: hidden;">Modificar</b></p>
```
---
`Ejemplo de textContent`
```js
const titulo = document.querySelector(".titulo");
let resultado = titulo.textContent; // devuelve el texto visible
```
---
`Ejemplo de innerHTML`
```js
const titulo = document.querySelector(".titulo");
let resultado = titulo.innerHTML; // devuelve todo el contenido HTML
```
---
`Ejemplo de outerHTML`
```js
const titulo = document.querySelector(".titulo");
let resultado = titulo.outerHTML; // devuelve todo el contenido HTML incluso la etiqueta del elemento.
```
---
`copia este ejemplo en tu codigo, para comprender mas facil`
```js
const titulo = document.querySelector(".titulo");
let resultado = titulo.textContent;
let resultado1 = titulo.innerHTML;
let resultado2 = titulo.outerHTML;

alert(resultado);
alert(resultado1);
alert(resultado2);
```

