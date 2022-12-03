# Variables
---
- Usos para una variable:

```javascript
string = "cadena de texto";
number = 10 (numeros);
boolean = true/false;
```

- existen 3 tipos de variables para usar:

```javascript
var nombre = "Fabrizio R.";
let edad = 18;
const nacionalidad = "Argentino";
```

>**var**: es una variable que abarca todo el bloque, se puede modificar

>**let**: abarca contenido en un bloque especifico porque tiene menos alcance, se puede modificar

>**const**: es una variable constante, es decir que no se puede modificar, ya que es inicializada una sola vez

---
- Tipos de datos:

>**Undefined:** es una variable **no definida**, hasta que se le otorgue un valor.

>**Null**: es una variable **no definida** pero **de forma adrede**.

>**NaN**: es cuando utilizamos texto en una operacion numerica o viceversa.

>**Scope**: es hasta donde llega la variable en especifico, afuera de su bloque no existe.
---

- Prompt

**Prompt es una funcion que te pide un dato de forma alerta, este dato se transforma en el mismo que coloco el usuario.**

>es decir si el usuario puso "Perro amarillo" en la cadena de texto, ahora el prompt contiene el dato de "Perro amarillo"

**Ejemplo:** 

```javascript
let nombre = prompt("Introduzca su nombre aqui")

alert("Bienvenido " + nombre)
```

- Ahi lo que hicimos fue practicamente usar la  variante "nombre" con el contenido prompt que a su misma vez contiene lo que el usuario puso, es decir su nombre.

---