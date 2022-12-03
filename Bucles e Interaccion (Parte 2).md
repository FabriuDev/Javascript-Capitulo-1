# Bucles e Interaccion (Parte 2)
---

        los bucles for in, for of y sentencia label

- Ejemplo de for in y for of:

```js
let animales = ['leon','perro','gato'];//esto es un array

for (animal in animales){//aca animal es igual a la pocision 0 del array
    document.write(animal + '<br>');//se ejecuta animal (0) y al ser un loop, se van ejecutando en cadena las demas palabras
}

document.write('<br>');//se ejecuta un espacio en linea

for (animal of animales){//aca pasa lo mismo, pero en vez de mostrarse el numero de la fila, se muestra el dato que contiene cada valor(['leon','perro','gato'])
    document.write(animal + '<br>');//se ejecuta diciendo cada valor en pantalla
}
```
`for in: devuelve indice`

`for of: devuelve valor`

---

- Ejemplo for in/of con Label:

```js
let array1 = ['juan','carlos','maria'];
let array2 = ['fabri','nashe',array1,'jorgelin'];

forPrimero: //esto es un label y separa el primer bucle del segundo a la hora de hacer un break o un continue
for (let array in array2) { //en este bucle se ejecuta el array2 hasta la posicion 2 ya que luego empieza el array1)
    if (array == 2) {//se usa un if para decir en que posicion termina el bucle


        for (let array of array1) { //en este bucle se ejecuta el array1
            document.write(array + '<br>');//se imprime la variable que se coloco en el for dejando lineas de espacio 
        }


    } else {
        document.write(array2[array] + '<br>'); //este else se imprime de todas maneras si los demas fallan, esta dentro del primer for
    }
}
```