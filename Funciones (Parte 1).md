# Funciones (Parte 1)
---
>Una función en JavaScript es similar a un procedimiento — un conjunto de instrucciones que realiza una tarea o calcula un valor, pero para que un procedimiento califique como función, debe tomar alguna entrada y devolver una salida donde hay alguna relación obvia entre la entrada y la salida.

- Como se declara una function:


```js
function saludar() {//asi se declara una function
}

saludar()//aca se ejecuta la function
```

- de que formas se usan?

```js
function saludar() {
    alert('Hello')
    return "Goodbye"//esto se retorna y se finaliza la function, lo que sigue despues de esto no sale en la function

}

let saludos = saludar()// esto se puede usar asi, o como en el primer ejemplo
```
---
- Funciones con parametros:

```js
function suma(num1,num2){//lo que esta entre parentesis es un parametro, y sirve para definir las variables y diferenciarlas de las demas funciones
    let resultado = num1 + num2;
    document.write(resultado);//esto se ejecuta en este bloque
}

suma(50,50)
```

- ejemplo con return:

```js
function suma(num1,num2){
    let resultado = num1 + num2;
    return resultado
}

let resultado = suma(50,50);//aca estamos diciendo que la variable resultado contiene el valor suma(), por lo tanto lo que este adentro de los parentesis es el valor de cada variable.
document.write(resultado); //ahora se ejecuta resultado y no suma(), ya que es lo mismo pero asignado a la variable resultado.
```

```js
function saludar(nombre){
    let frase = `Hola ${nombre}, como estas? `;
    document.write(frase)
}

saludar('Anonimo');
```
---

- Funciones flechas:

```js
const saludar = (nombre)=>{//esto es una function flecha, esta mucho mas optimizada y no requiere tantos recursos
    document.write(`hola ${nombre}, como estas?`);
}
saludar('pepe')
```