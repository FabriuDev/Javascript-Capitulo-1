# Propiedades de Sibling (Hermanos)
---
- #### nextSibling
- #### previuosSibling
- #### nextElementSibling
- #### previousElementSibling
---

- Ejemplo HTML:

```html
    <div class="contenedor">
        <h2 class="h2">Un H2 Comun</h2>
        <h4>Un H4 Comun</h4>
        <p>Un Parrafo Comun</p>
    </div>
```

- Ejemplo 1:

```js
    const h2_antiguo = document.querySelector(".h2");

    console.log(h2_antiguo.nextSibling); // mostramos en consola el siguiente NODO hermano
```

- Ejemplo 2:

```js
    const h2_antiguo = document.querySelector(".h2");

    console.log(h2_antiguo.previousSibling); // mostramos en consola el anterior NODO hermano
```

- Ejemplo 3:

```js
    const h2_antiguo = document.querySelector(".h2");

    console.log(h2_antiguo.nextElementSibling); // mostramos en consola el siguiente ELEMENTO hermano del H2
```

- Ejemplo 4:


```js
    const h2_antiguo = document.querySelector(".h2");

    console.log(h2_antiguo.previousElementSibling); // mostramos en consola el anterior ELEMENTO hermano del H2
```