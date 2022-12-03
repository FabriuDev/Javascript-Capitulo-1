# Bucles e interaccion (Parte 1)

`En JavaScript los bucles (loops) son utilizados para realizar tareas repetitivas con base en una condición. Las condiciones típicamente devuelven true (verdadero) o false (falso) al ser evaluados. El bucle continuará ejecutándose hasta que la condición devuelva false`

- existen todos estos tipos de bucles e interacciones:
  - while
  - do while
  - for
  - for on
  - for of
  - break
  - label
  - continue


#### Ejemplo de while:

```js
let numero = 0;//asigna una variante

while (numero < 5) {//se ejecuta la accion si se cumple la condicion
    numero++;//agrega un +1 al numero
    document.write(numero + "<br>");//agrega la variante mas un espacio en linea por cada numero
}
```
#### Ejemplo de do while:

```js
let numero = 0;//asigna una variable

do {//siempre se ejecuta
    document.write(numero);//muestra el resultado en pantalla
    numero++;//agrega un +1 al numero
}

while (numero < 5) {//se ejecuta de forma infinita si la condicion es true
}
```

#### Ejemplo de while con break:

```js
let numero = 0;//asigna una variable

while (numero < 1000) {//si numero es menor a 1000 ejecuta la accion
    numero++;//agrega un +1 al numero
    document.write(numero + "<br>");
    if (numero == 10){
        break;//formamos un if para que break se ejecute y se frene en el numero 10 y siga el programa
    }
}
```

#### Ejemplo de for:

- for tiene 3 caracteristicas, primero se coloca la declaracion, segundo la condicion y al final el incremento o el decremento.

```js
for (let i = 0; i < 6; i++){//primero creamos la variable i y la igualamos a 0, luego creamos la condicion i < 6 que es true, y al final agregamos un +1.
    document.write(i + "<br>");
}
```
#### Ejemplo de for con break:

```js
for (let i = 0; i < 20; i++){
    if (i == 12){//termina el bucle en el numero 12, es decir que no lo muestra
        break;
    }
    document.write(i + "<br>");
}
```

#### Ejemplo de for con continue:

```js
for (let i = 0; i  5; i++){
    if (i == 3){//hace que se saltee el 3 y continue hasta el 5
        continue;
    }
    document.write(i + "<br>");
}
```