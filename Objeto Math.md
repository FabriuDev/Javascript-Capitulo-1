#   Objeto Math
---

> Metodos:

- sqrt() - Devuelve la raiz cuadrada positiva de un numero
- cbrt() - Devuelve la raiz cubica de un numero
- max() - Devuelve el mayor de cero o mas numeros.
- min() - Devuelve el mas pequeño de cero o mas numeros
- random() - Devuelve un numero pseudo-aleatorio entre 0 y 1.
- round() - Devuelve el valor de un numero redondeado al entero mas cercano
- fround() - Devuelve la representacion flotante de precisión simple mas cercana de un número
- floor() - Devuelve el mayor entero menor que o igual a un número
- trunc() - Devuelve la parte entera del número x, la eliminacion de los dígitos fraccionarios.

> Propiedades:

- PI - ratio de la circunferencia de un círculo respecto a su diámetro, aproximadamente 3.14159…
- SQRT1_2 - Raiz cuadrada de 1/2 ; Equivalente, 1 sobre la raíz cuadrada de 2, aproximadamente 0.707…
- SQRT2 - Raiz cuadrada de de 2, aproximadamente 1.414...


- E - Constante de EULER, la base de los algoritmos naturales 2,71828
- LN2 - Logaritmo natural de 2, aproximadamente 0.693
- LN10 - Logaritmo natural de 10, aproximadamente 2.303
- LOG2E - Logaritmo de E con base 2, aproximadamente 1.443
- LOG10E - Logaritmo de E con base 10, aproximadamente 0.434

---

`Ejemplos con el Objeto Math`

```js
let numero = Math.sqrt(25); // devuelve la raiz cuadrada positiva de un numero
```

```js
let numero = Math.bcrt(); // devuelve la raiz cubica de un numero.
```

```js
let numero = Math.max(1,85,100,542,88); // devuelve el numero mayor
```

```js
let numero = Math.min(1,85,100,542,88); // devuelve el numero menor
```

```js
let numero = Math.random(); // devuelve un numero random entre 0 y 1
// ejemplo 2 si queres que sea un numero entre 1 y 100 y sin coma es asi:

let numero = Math.random()*100;
numero = Math.round(numero); // esto redondea el numero para arriba al numero entero mas cercano.
```

```js
let numero = Math.floor(numero); // esto redondea el numero para abajo, (4.9 = 4) y asi con todos los numeros
```

> En todo caso que queramos que salga un numero entre el 1 y 100 es asi:
```js
let numero = Math.random()*99; // estamos multiplicando el 0 y 1 por 99.
let numero = Math.floor(numero+1); // de esta manera le estamos sumando +1
```

```js
let numero = Math.fround(9.462528364583859); // devuelve la representacion flotante de precision simple mas cercana de un numero.
```

```js
let numero = Math.trunc(9.9); // elimina la fraccion devolviendo solo el numero entero.
```
