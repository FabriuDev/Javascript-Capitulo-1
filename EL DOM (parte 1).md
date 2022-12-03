# EL DOM y...
- ### Metodos de seleccion de elementos
- ### Metodos de Atributos de un elemento.
- ### Atributos Globales
- ### Atributos de Inputs
- ### Atributo Style
---
`ADENTRANDONOS EN EL DOM:`

- Definición
- Concepto Extendido
- Nodo `(un nodo en el DOM es cualquier etiqueta del cuerpo, como un parrafo, el mismo body, incluso las etiquetas de una lista.`
---


- `Document: el nodo document es el nodo raíz, a partir del cual derivan el resto de nodos.`

- `Element: nodos definidos por etiquetas html.`

- `Text: el texto dentro de un nodo element se considera un nuevo nodo hijo de tipo text (texto)`

- `Attribute: los atributos de las etiquetas definen nodos, en (Javascript no los veremos como nodos, sino como información asociada al nodo de tipo element)`

- `Comentarios y otros: los comentarios y otros elementos como las declaraciones doctype en cabecera de los elementos HTML generan nodos.`


---

        Métodos de Selección de elementos
        *Se usa Document.*

- `getElementById() - Selecciona un elemento por ID.`
```js
Ejemplo: const parrafo = document.getElementById("parrafo");
         document.write(parrafo);   // estamos seleccionando el elemento "parrafo" que es <p id="parrafo"><p> sacado de HTML.
```

- `getElementsByTagName() - Selecciona todos los elementos que coincidan con el nombre de la etiqueta especificada.`
```js
Ejemplo 2: const parrafo = document.getElementsByTagName("p");
           document.write(parrafo);    // este atributo selecciona todos los elementos "p" que se encuentran en el archivo HTML
           document.write(parrafo[0]);  // esto no es un array, estamos seleccionando el primer elemento con la caracteristica de "p" de HTML.
```

- `querySelector() - Devuelve el primer elemento que coincida con el grupo especificado de selectores.`
```js
Ejemplo 3: const titulo = document.querySelector(".clase"); // aca usamos los selectores de CSS. (si usamos ID se usa #, y para las clases el punto.)
```

- `querySelectorAll() - Devuelve todos los elementos que coincidan con el grupo especificado de selectores.`
```js
Ejemplo 3: const titulo = document.querySelectorAll(".clase");// este atributo nos selecciona todos los elementos con la clase (.clase) y nos declara un NodeList, que tampoco es un array!
           document.write(titulo[0]); // aca estamos llamando al primer elemento de la NodeList
```
---
        Métodos para Definir, Obtener y Eliminar valores de atributos.
        *Se usan los elementos, no document.)

- `setAttribute() - Modifica el valor de un atributo.`
```js
Ejemplo 1: const titulo = document.querySelector(".clase");
        titulo.setAttribute("type", "number")   // remplaza el primer valor, por el segundo valor que seleccionemos.
```

- `getAttribute() - Obtiene el valor de un atributo.`
```js
Ejemplo 2: const titulo = document.querySelector(".clase");
           let valorDelAtributo = titulo.getAttribute("type");   
        document.write(titulo);    // de esta manera obtenemos el valor de type o de cualquier valor que este en pantalla. 
```

- `removeAttribute() - Remueve el valor de un atributo.`
```js
Ejemplo 3: const titulo = document.querySelector(".clase");
           let valorDelAtributo = titulo.removeAttribute("type"); // de esta manera estamos eliminando al elemento con el atributo "type".
```

---
        Atributos Globales

- `ContentEditable - indica si el elemento puede ser modificable por el usuario (bool)`
```js
Ejemplo 1: const titulo = document.querySelector(".clase");
         titulo.setAttribute("contentEditable", "true"); // esto significa que el contenido del texto es editable para el cliente.
```

- `Dir - indica la direccionalidad del texto`
```js
Ejemplo 2: const titulo = document.querySelector(".clase");
         titulo.setAttribute("dir", "rtl"); // rtl significa que el texto empieza de la "right" derecha y termina en "left" izquierda.
```

- `hidden - indica si el elemento aun no es, o ya no es, relevante.`
```js
Ejemplo 3: const titulo = document.querySelector(".clase");
         titulo.setAttribute("hidden", "true"); // no importa si es true o false, de todas maneras el elemento va a desaparecer. para que el elemento se muestre en pantalla si o si hay que eliminarlo.
```

- `tabindex - indica si el elemento puede obtener un focus de input`
```js
Ejemplo 4: const titulo = document.querySelector(".clase");
           titulo.setAttribute("tabindex", "0"); // se manejan con el valor number, las letras no funcionan.
```

- `title - contiene un texto con información relacionada al elemento al que pertenece`
```js
Ejemplo 5: const titulo = document.querySelector(".clase");
           titulo.setAttribute("title", "Nuevo Titulo"); // estamos cambiando el titulo (cuando pasamos el click por encima) de esta manera desde Javascript.
```
---

        Atributos de Inputs

`- className - nos nuestra el nombre que tiene la clase.`
```js
Ejemplo 1: const input = document.querySelector(".input-normal");
           input.className;
```
`- value - nos muestra el valor que tiene value en el input`
```js
Ejemplo 2: const input = document.querySelector(".input-normal");
           input.value;
```
`- type - podemos pedir que nos muestre el type y tambien asignarle un nuevo valor de la siguiente forma.`
```js
Ejemplo 3: const input = document.querySelector(".input-normal");
           input.type = "number";
```
- `accept - es para aceptar el tipo de archivo que le estamos pidiendo con el type "file".`
```js
Ejemplo 4: const input = document.querySelector(".input-normal");
           input.accept = "image/png";
```
`- form - si el boton esta fuera del form, pero tiene un ID, con el atributo form="" podemos hacer que la informacion que se ejecute en el input sea enviada al servidor como en el siguiente ejemplo.`
```html
Ejemplo 5: <form id="formulario-1">Nombre y apellido</form>
           <input type="submit" form="formulario">
```
`- minlength - le asignamos la cantidad minima de letras al input`
```js
Ejemplo 6: const input = document.querySelector(".input-normal");
           input.minLenth = 4; // aca ponemos la cantidad minima de letras
```

`- placeholder - sirve para especificar el tipo de input que es mediante un texto.`
```js
Ejemplo 7: const input = document.querySelector("input-normal");
           input.placeholder = "Escribe tu usuario";
```

`- required - significa que el campo del input ahora es requerido, de tal manera que aunque pongamos " " el campo tendra que si o si estar lleno.`
```js
Ejemplo 8: const input = document.querySelector(".input-normal");
           input.required = " "; // a partir de ahora el campo tiene que estar completado de manera obligatoria.
```
---
                Metodo Style
`- propiedades Camel Case`

`- Usos y ejemplos:`

```js
Ejemplos: const titulo = document.querySelector(".titulo");
           titulo.style.color = "#22a";
           titulo.style.backgroundColor = "#48b";
           titulo.style.padding = "30px";
           titulo.style.margin = "5px";
           titulo.style.border = "3px solid #555";
```




