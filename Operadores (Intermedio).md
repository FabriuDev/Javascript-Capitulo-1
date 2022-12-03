# Operadores (Intermedio)

---

## Operadores de Comparacion

`Los operadores de comparacion comparan dos expresiones y devuelven un valor Boolean que representa relacion de sus valores`

- Ejemplo de igualdad (Pregunta si son el mismo dato):

```js
let numero1 = 10;
let numero2 = 10;

document.write(numero1 == numero2) true
```

- Ejemplo de Desigualdad

```js
let numero1 = 23;
let numero2 = 13;

document.write(numero1 != numero2) true
```

- Ejemplo de Igual Estricta (Todo Igual)

```js
let numero1 = 23;
let numero2 = 23;

document.write(numero1 === numero2) true
```

- Ejemplo de Estrictamente diferente (Todo diferente)

```js
let numero1 = 23;
let numero2 = '23';

document.write(numero1 !== numero2) true
```

- Ejemplo de mayor a

```js
let num1 = 20;
let num2 = 20;

document.write(num1 > num2) false
```

- Ejemplo de menor a

```js
let num1 = 15;
let num2 = 20;

document.write(num1 < num2) true
```

- Ejemplo de mayor o igual a

```js
let num1 = 20;
let num2 = 20;

document.write(num1 >= num2) true
```

- Ejemplo de menor o igual a

```js
let num1 = 10;
let num2 = 20;

document.write(num1 <= num2) false
```

---

## Operadores Logicos

`Los operadores logicos nos devuelven un resultado a partir de que se cumpla (o no) una condicion, su resultado es booleano, y sus operandos son valores logicos o asimilables a ellos.`

- Ejemplo de los 3 operadores logicos:

```js
let valor1 = true;
let valor2 = true;

let resultado = valor1 && valor2;
let resultado2 = valor1 || valor2;
let resultado3 = !valor1;

document.write()
```

    Significado de &&: 
    false + true = false
    true + true = true
    false + false = false
---
    Significado de ||:
    false + true = true
    false + false = false
    true + true = true
---
    Significado de !valor:
    hace que el valor cambie de forma opuesta a partir del signo !
---
### Ejercicios

```js
num1 = 12;
num2 = 24;
num3 = 25;
num4 = 92;
num5 = 91;

op = (num1 < num2 || num2 < num3) && (!(num1 && num5 != num3));

document.write(op)
```