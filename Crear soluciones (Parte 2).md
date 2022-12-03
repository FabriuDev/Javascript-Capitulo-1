# Crear soluciones (Parte 2)
---
### PROBLEMA 1

- mini sistema de validacion en un boliche: se tiene que saber si son mayores de edad y quien entra gratis despues de las 2AM y quien tiene que pagar la entrada.

`Solucion:`
```js
let free = false;

const validarCliente = (time)=>{// funcion que explica la hora exacta de las personas que ingresan
    let edad = prompt("Cuantos años tenes master?");// variable con prompt, preguntando la edad de las personas
    if (edad > 17) {// se valida si sos mayor a (17)
        if (time >= 2 && time < 7 && !free) {//se valida si time es mayor o igual a 2AM y time es menor a 7AM y free que se asigno como false, pasa a ser true 
            alert("Podes pasar GRATIS porque sos la primer persona despues de las 2 AM");// si todo lo anterior se cumple, se confirma este alert.
            free = true;//esto se usa para que funcione solo una vez lo de entrar gratis
        } else{// si no se valida lo anterior, vas a tener que pagar la entrada
            alert(`Son las ${time}:00hs y podes pasar, pero tenes que pagar 500$`)
        }
    } else {// y si tu edad es menor a 18, directamente no pasas
        alert("sos menor capo, tomate el buque")
    }
}
// se ponen muchas funciones para decir los horarios de entrada de cada persona
validarCliente(23);
validarCliente(24);
validarCliente(0.2);
validarCliente(0.6);
validarCliente(1);
validarCliente(2);
validarCliente(2.4);
validarCliente(3);
```
---
### PROBLEMA 2

- mini sistema de asistencias e inasistensias en un colegio, se tiene que saber la cantidad de alumnos que hay, la cantidad de veces que asistieron a clases en el mes y sacar el 10% de inasistencias en todo caso de reprobar.

```js
let cantidad = prompt('cuantos alumnos son?');
let alumnosTotales = [];

for (i = 0; i < cantidad; i++) {
    alumnosTotales[i] = [prompt("nombre del alumno " + (i+1)),0];//esto es un array dentro de otro array
}

const tomarAsistencia = (nombre,p)=>{//funcion que nos pide el nombre y la posicion en la lista
    let presencia = prompt(nombre);//aca le vamos a decir si la persona esta presente, poniendo (A o P)
    if (presencia == 'p' || presencia == 'P') {//si presencia es igual p o P se suma +1
        alumnosTotales[p][1]++;//aca estamos seleccionando un elemento del array que esta dentro de otro array
    }
}

for (i = 0; i < 30; i++){//esto es para ejecutar 30 veces el bucle, por los 30 dias del mes aprox
    for (alumno in alumnosTotales) {//esta recorriendo el 2do array, con el nombre alumno(indice)
        tomarAsistencia(alumnosTotales[alumno][0],alumno);//el primer alumno tiene el nombre y ademas se le agrega el alumno que determina la pocision.
    }
}

for (alumno in alumnosTotales){
    let resultado = `${alumnosTotales[alumno][0]}:<br>
    ________Presentes: <b>${alumnosTotales[alumno][1]} </b> <br>
    ________Ausencias: <b>${30 - parseInt(alumnosTotales[alumno][1])}</b>`;
    if (30 - alumnosTotales[alumno][1] > 18) {
        resultado+= "<b style='color:red'> REPROBADO POR INASISTENCIA</b><br><br>";
    } else {
        resultado+= "<br><br>";
    }
    document.write(resultado);
}
```
---

### PROBLEMA 3

- Calculadora basica de suma,resta,division y multiplicacion.

```js
const suma = (num1,num2)=>{
    return parseInt(num1) + parseInt(num2);
}
const restar = (num1,num2)=>{
    return parseInt(num1) - parseInt(num2);
}
const dividir = (num1,num2)=>{
    return parseInt(num1) / parseInt(num2);
}
const multiplicar = (num1,num2)=>{
    return parseInt(num1) * parseInt(num2);
}

alert('Que operacion queres realizar?');
let operacion = prompt('1: suma, 2: resta, 3: dividir, 4: multiplicación');

if (operacion == 1) {
    let numero1 = prompt('primer numero para sumar');
    let numero2 = prompt('segundo numero para sumar');
    let resultado = suma(numero1,numero2);
    alert(`tu resultado es ${resultado}`);
}
else if (operacion == 2) {
    let numero1 = prompt('primer numero para restar');
    let numero2 = prompt('segundo numero para restar');
    let resultado = restar(numero1,numero2);
    alert(`tu resultado es ${resultado}`);
}
else if (operacion == 3) {
    let numero1 = prompt('primer numero para dividir');
    let numero2 = prompt('segundo numero para dividir');
    let resultado = dividir(numero1,numero2);
    alert(`tu resultado es ${resultado}`);
}
else if (operacion == 4) {
    let numero1 = prompt('primer numero para multiplicar');
    let numero2 = prompt('segundo numero para multiplicar');
    let resultado = multiplicar(numero1,numero2);
    alert(`tu resultado es ${resultado}`);
}
else {
    alert('No se ha encontrado la operacion.')
}
```