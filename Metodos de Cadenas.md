# Metodos de Cadenas
---
`Las funciones de estos metodos, es buscar cadenas y devolvernos un valor`
 - **concat()** - junta dos  o mas cadenas y retornan una nueva
- **startsWith()** - si una cadena comienza con los caracteres de otra cadena, devuelve true, sino false.
- **endsWith()** - si una cadena puede encontrarse dentro de la otra cadena, devuelve true, sino false
- **includes()** - devuelve el indice del primer caracter de la cadena, si no existe, devuelve -1
- **lastIndexOf()** - devuelve el ultimo indice del primer caracter de la cadena, si no existe, devuelve -1
---
`Estos metodos se basan en modificar y rellenar nuestras cadenas`
- **pasStart()** [Propuesta de ECMA] - Rellenar cadena al principio con caracterers deseados
- **padEnd()** - [Propuesta de ECMA] - Rellenar cadena al final con los caracteres deseados
- **repeat()** - Devuelve la misma cadena pero repetida la cantidad de veces que le indiquemos.
---
`Estos metodos tambien modifican y transforman nuestra cadena, pero de una manera mas compleja`
- **split()** - Divide la cadena como le pidamos
- **substring()** - Nos retorna un pedazo de la cena que seleccionamos
- toLowerCase()** - convierte una cadena a minúscula
- **toUpperCase()** - convierte una cadena a mayúscula
- **toString()** - metodo que devuelve una cadena que representa al objeto específico
- **trim()** - elimina los espacios en blanco al final de una cadena
- **trimEnd()** - elimina los espacios en blanco al final de una cadena
- **trimStart()** - elimina los espacios en blanco al comienza de una cadena
---

        Todos los ejemplos con metodos de cadenas:

> concat()
```js
let cadena1 = "cadena de prueba";
let cadena2 = " hola";

let resultado = cadena1.concat(cadena2);

document.write(resultado);
```

> startsWith()
```js
let cadena1 = "cadena de prueba";
let cadena2 = "cadena ";

let resultado = cadena1.startsWith(cadena2);// si empieza con los mismo caracteres, da true, sino da false

document.write(resultado);
```

> endsWith()
```js
let cadena1 = "cadena de prueba";
let cadena2 = "prueba";

let resultado = cadena1.endsWith(cadena2);// si termina con los mismos caracteres, da true, sino da false

document.write(resultado);
```

> includes()
```js
let cadena1 = "cadena de prueba";
let cadena2 = "de prueba";

let resultado = cadena1.includes(cadena2);// si algun caracter se repite en la cadena, da true, sino da false

document.write(resultado);
```

> indexOf()
```js
let cadena1 = "cadena de prueba";
let cadena2 = "";

let resultado = cadena1.indexOf("prueba");// nos dice la pocision en la que se encuentra nuestra primer letra de la palabra
document.write(resultado[3]);// si vos queres sellecionar manualmente se hace asi (se selecciona el caracter del lugar 3)
```

>  lastIndexOf()
```js
let cadena1 = "cadena de prueba";
let cadena2 = "";

let resultado = cadena1.lastIndexOf("prueba");// nos dice la ubicacion de los ultimos caracteres que estamos buscando

document.write(resultado);
```
---
> padStart()
```js
let cadena1 = "abc";
let cadena2 = "";

let resultado = cadena1.padStart(6,"a");// nos agrega caracteres de la siguiente manera(los que sean necesarios)

document.write(resultado);
```

> padEnd()
```js
let cadena1 = "abc";
let cadena2 = "";

let resultado = cadena1.padEnd(6,"a");// nos agrega caracteres de la siguiente manera (los que sean necesarios)

document.write(resultado);
```

> repeat()
```js
let cadena1 = "abc";
let cadena2 = "";

let resultado = cadena1.repeat(5);// nos repita la cadena las veces que queramos

document.write(resultado);
```
---
> split()
```js
let cadena = "hola,como,estas";// se separa en (,) para que el metodo split separe las palabras como si fuera un array (tambien se puede separar con 2 espacios "  " y con palabras que esten en la cadena)

let resultado = cadena.split(",");// le decimos que nos separe la cadena cuando haya una coma (,)

document.write(resultado[1]);// aca le decimos que parte queremos separar, poniendo corchetes y elegiendo el numero correcto
```

> substring()
```js
let cadena = "ABCDEF";
// let cadena2 = "";

let resultado = cadena.substring(0,2); // nos muestra donde arranca pero no donde termina, por eso hay que saber bien que numero colocar

document.write(resultado);
```

> toLowerCase()
```js
let cadena = "ABCDEF";
// let cadena2 = "";

let resultado = cadena.toLowerCase();// convierte todo la cadena a miniscula

document.write(resultado);
```

> toUpperCase()
```js
let cadena = "abcdef";
// let cadena2 = "";

let resultado = cadena.toUpperCase();// convierte todo la cadena a mayuscula

document.write(resultado);
```

> toString()
```js
let cadena = 50;
// let cadena2 = "";

let resultado = cadena.toString();// convierte todo a un string, sea un numero o un array - (si en el resultado colocas como si fuera un array, te va a colocar el resultado de un string, es decir la primera letra)

document.write(3 + resultado);// funciona solo cuando concatenas con el signo (+), y si usas el signo (-) cambia la cuenta a negativa.
```

> trim()
```js
let cadena = "      prueba      ";
// let cadena2 = "";

let resultado = cadena.trim();// esto remueve los espacios en blanco que hay en la cadena

document.write(resultado.length);// con la propiedad length nos indica cuantos caracteres tiene nuestra cadena (ya que cada espacio suma)
```

> trimEnd()
```js
let cadena = "      prueba      ";
// let cadena2 = "";

let resultado = cadena.trimEnd();// esto remueve los espacios en blanco, pero del final de la cadena

document.write(resultado.length);// con la propiedad length nos indica cuantos caracteres tiene nuestra cadena (ya que cada espacio suma)
```

> trimStart()
```js
let cadena = "      prueba      ";
// let cadena2 = "";

let resultado = cadena.trimStart();// esto remueve los espacios en blanco, pero del inicio de la cadena

document.write(resultado.length);// con la propiedad length nos indica cuantos caracteres tiene nuestra cadena (ya que cada espacio suma)
```
---