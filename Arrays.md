# Arrays
---

- un array es un arreglo, es decir que un arreglo contiene mas cualidades que por ejemplo una variable, es mucho mas detallado y complejo.

- un array puede ser una caja de te, que adentro contiene bolsitas de te, y esas bolsitas de te son una diferente a la otra, de tal manera que tambien estan ordenadas de diferente forma, etc.


`Ejemplo de array`

```js
let frutas = ['manzana','banana','pera',6,'mango',22];//se colocan entre corchetes y de forma separada por comillas.

document.write(frutas[0,1,6])//se colocan corchetes con el lugar de cada elemento (empezando siempre desde el cero)
```

`Ejemplo de array Asociativo`

```js
let pc = {
    nombre: 'La Poderosa'
    procesador: 'Ryzen 5'
    ram: '16GB'
    espacio: '500GB'
};

let pcCompleta = `el nombre de mi pc es <b>${nombre}</b> <br>
                el procesador es: <b>${procesador}</b> <br>
                la memoria ram es: <b>${ram}</b> <br>
                el espacio es de: <b>${espacio}</b>`;

document.write(pcCompleta);
```