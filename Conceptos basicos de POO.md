# Conceptos basicos de POO
---

- ¿Que es POO? Es un paradigma de la programación en el que se crean objetos para la manipulacón de datos y donde, por lo general, cada objeto ofrece una funcionalidad especial. La idea básica de la POO es que usamos objetos para modelar cosas del mundo real. POO nos ayuda a la reutilización del código.

`ejemplo basico:`

```js
class animal {//esto es una clase
    constructor(especie,edad,color){//esto es el constructor de la clase
        this.especie = especie;//se usa el (this.) para asignar cada valor  del constructor
        this.edad = edad;
        this.color = color;
        this.info = `Soy ${this.especie}, tengo ${this.edad} años y soy de color ${this.color}`;
    }
    verInfo(){//esto es un metodo y funciona solo para este bloque
        document.write(this.info + "<br>");
    }
}

const perro = new animal('perro',4,'marron');//se asigna const para asignar el orden del objeto (especie,edad,color)
const cabra = new animal('cabra',3,'blanca');//se usa (new) seguido del nombre de la clase, para referirse al objeto
const pajaro = new animal('pajaro',2,'verde');

perro.verInfo();//se ejecuta el nombre de la variable const, seguido del metodo asignado en la clase.
cabra.verInfo();
pajaro.verInfo();
```