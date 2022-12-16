## Metodos de Parents (DOM)
---
- #### parentElement
- #### parentNode
---

- #### Ejemplo HTML:

```html
    <div class="contenedor">
        <h2 class="h2">Un H2 Comun</h2>
        <h4>Un H4 Comun</h4>
        <p>Un Parrafo Comun</p>
    </div>
```
- `Nosotros queremos preguntarle a javascript cual es el parentElement o parentNode, en ambos casos nos dira que la etiqueta div con la clase "contenedor" es el padre, pero en casos muy especificos nos dira otra cosa.`

```js
    const h2_nuevo = document.createElement("H2")
    const h2_antiguo = document.querySelector(".h2"); 
    
    console.log(h2_antiguo.parentElement); // nos va decir quien es el contenedor del h2_antiguo.
```

- Ejemplo 2:

```js
    const h2_nuevo = document.createElement("H2")
    const h2_antiguo = document.querySelector(".h2"); 
    
    console.log(h2_antiguo.parentNode); // de esta forma tambien nos dice el elemento que los contiene.
```

- Ejemplo 3:

```js
    const h2_nuevo = document.createElement("H2")
    const h2_antiguo = document.querySelector(".h2"); 
    
    console.log(h2_antiguo.parentNode); // en cambio si colocamos el H2 creado por JS nos va decir que es "NULL" ya que el node o padre del elemento esta creado fuera del html y no lo reconoce como padre. 
```