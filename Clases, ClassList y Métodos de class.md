### Clases, ClassList y Métodos de classList
---
`Definición y usos:`

- add() - `añade una clase`
```js
Ejemplos: const titulo = document.querySelector(".titulo");
          titulo.classList.add("grande") // este es el metodo para agregar una clase usando classList
```
- remove() - `remueve una clase`
```js
Ejemplos: const titulo = document.querySelector(".titulo");
          titulo.classList.remove("grande") // este es el metodo para remover una clase usando classList
```
- item() - `devuelve la clase del indice especificado`
```js
Ejemplos: const titulo = document.querySelector(".titulo");
          let valor = titulo.classList.item(0) // de esta manera estamos pidiendo la clase en la posicion numero 0.
          document.write(valor); // no hace falta el document.write es solamente un ejemplo grafico de lo que se selecciona
```
- contains() - `verifica si ese elemento posee o no, la clase especificada.`
```js
Ejemplos: const titulo = document.querySelector(".titulo");
          titulo.classList.contains("grande") // este metodo verifica si existe la clase que le estamos asignando o no, usando el metodo booleano.
```

- replace() - `remplaza una clase por otra`
```js
Ejemplos: const titulo = document.querySelector(".titulo");
          titulo.classList.replace("grande","chico"); // aca si existe la clase "grande", la remplaza por la clase "chico" y da true, en cambio si la clase "grande" no existe no cambia nada y da false.
```

- toggle() - `si no tiene la clase especificada, la agrega, si ya la tiene, la elimina.`
```js
Ejemplos: const titulo = document.querySelector(".titulo");
          titulo.classList.toggle("grande") // tambien si queremos que agregue siempre la clase o la elimine siempre, debemos poner "true" o "false" para especificar el metodo.

          titulo.classList.toggle("grande",false) // ahi la borra siempre
          titulo.classList.toggle("grande",true) // ahi la agrega siempre
```