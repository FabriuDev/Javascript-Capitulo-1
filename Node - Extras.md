# Node - Extras
---

- #### closest();
--- 

- Ejemplo HTMl:

```html
    <div class="div">
        DIV 1
        <div class="div">
        DIV 2
        </div>
        <div class="div-3"></div>
    </div>
```

- Ejemplo JS:

```js
    const div = document.querySelector("div-3");

    console.log(div.closest(".div")); // lo que hace closest es buscar el CONTENEDOR mas cercano de forma ascendente, es decir aca el div que esta mas arriba es el contenedor (DIV 1), en cambio si colocamos el DIV-3 adentro del DIV 2, el contenedor seria DIV 2. *siempre busca el contenedor mas cercano*
```


