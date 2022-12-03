# Condicionales
---
### Ejemplo de condionales:

```js
let nombre = 'fabrizio';
let apellido = 'rodriguez'

// se utiliza un solo if
if (nombre == 'fabrizio' && apellido == 'rodriguez') { // si la condicion se cumple, se ejecuta la accion. 
    alert(`tu nombre es ${nombre} ${apellido}`);
}
//se pueden utilizar muchos else if
else if (apellido == 'rodriguez') { // si la condicion se cumple, se ejecuta la accion.
    alert(`tu apellido es ${apellido}`);
}
// se utiliza un solo else
else { // si nada de lo anterior se cumple, se utiliza else.
    alert(`Usuario no disponible`);
}
```