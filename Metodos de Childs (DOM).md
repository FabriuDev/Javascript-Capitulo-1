## Metodos de Childs
---

- replaceChild() - Remplaza un child por uno nuevo
- removeChild() - Remueve un child
- hasChildNodes() - Verifica si el Elemento seleccionado tiene hijos

`Comenzando desde el ejemplo en HTMl`
```html
    <div class="contenedor">
        <h2 class="h2">un h2 comun</h2>
        <h4>un h4 comun</h4>
        <p>un parrafo comun</p>
    </div>
```
---

- Ejemplo 1:
```js
const contenedor = document.querySelector(".contenedor");

const h2_nuevo = document.createElement("H2");
h2_nuevo.innerHTML = "Titulo"; // con innerHTML le cambiamos el contenido a Titulo por ejemplo

const h2_antiguo = document.querySelector(".h2"); // identificamos el h2_antiguo del contenedor

contenedor.replaceChild(h2_nuevo, h2_antiguo); // le decimos a contenedor que queremos remplazar el h2_nuevo por h2_antiguo, de esta forma (new, old)
```

- Ejemplo 2:
```js
const contenedor = document.querySelector(".contenedor");

const h2_nuevo = document.createElement("H2");
h2_nuevo.innerHTML = "Titulo";

const h2_antiguo = document.querySelector(".h2"); // identificamos el h2_antiguo del contenedor

contenedor.removeChild(h2_antiguo); // le decimos a contenedor que queremos remover el h2_antiguo y lo elimina
```

- Ejemplo 3:
```js
const contenedor = document.querySelector(".contenedor");

const h2_nuevo = document.createElement("H2");
h2_nuevo.innerHTML = "Titulo";

const h2_antiguo = document.querySelector(".h2");

let respuesta = contenedor.hasChildNodes(); // el metodo hasChildNodes nos da un valor booleano si el ELEMENTO tiene hijos o NO

if (respuesta) {
    document.write("El elemento tiene hijos");  // estamos verificando de una manera muy facil si tiene o no hijos.
} else {
    document.write("El elemento NO tiene hijos");
}
```

