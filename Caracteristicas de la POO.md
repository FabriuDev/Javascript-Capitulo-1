# Caracteristicas de la POO
---

- Distinción entre clase y objeto. La distinción entre clase y objeto es una de las claves de este tipo de programación que la hace única.
- Reutiliza el código y evita su duplicación.
- Encapsula la información.
- Polimorfismo.

```js
class Animal {
    constructor(especie,edad,color){
        this.especie = especie;
        this.edad = edad;
        this.color = color;
        this.info = `soy un ${this.especie}, tengo ${this.edad} años y soy de color ${this.color}`;
    }
    verInfo(){
        document.write(this.info + "<br>");
    }
}

class Perro extends Animal {//de esta forma le estamos diciendo que herede las propiedades anteriores
    constructor(especie,edad,color,raza){//aca le decimos que tipo de datos tiene el objeto
        super(especie,edad,color);//aca definimos que queremos que herede de la clase anterior
        this.raza = raza;//definimos raza con this.
    }
    ladrar(){//hacemos un metodo
        alert('Waww waw!!');
    }
}



const perro = new Perro('perro',3,'beige','bulldog');
const gato = new Animal('gato',5,'negro');
const cangrejo = new Animal('cangrejo',2,'rojo');

perro.ladrar();
gato.verInfo();
cangrejo.verInfo();
```

---

### Metodo Static

- Para usar el metodo STATIC no hace falta crear la definicion para ser ejecutado, solamente poniendo el nombre de la clase y la accion que queremos asignar, ya funcionaria.

```js
class Animal {
    constructor(especie,edad,color){
        this.especie = especie;
        this.edad = edad;
        this.color = color;
        this.info = `soy un ${this.especie}, tengo ${this.edad} años y soy de color ${this.color}`;
    }
    verInfo(){
        document.write(this.info + "<br>");
    }
}

class Perro extends Animal {
    constructor(especie,edad,color,raza){
        super(especie,edad,color);
        this.raza = raza;
    }
    static ladrar(){// creamos el metodo static con la accion que queremos ejecutar
        alert('Waw Waw!')
    }
}

// NO HAY un const que defina a perro, por lo tanto con static se ejecuta de igual manera

Perro.ladrar(); // aca se usa el nombre de la clase y con el static ya funciona
```

### Metodos Setters & Getters

- Los metodos Getters (Get) sirven para obtener un valor y los Setters (Set) sirven para definir un valor


```js
class Animal {
    constructor(especie,edad,color){
        this.especie = especie;
        this.edad = edad;
        this.color = color;
        this.info = `soy un ${this.especie}, tengo ${this.edad} años y soy de color ${this.color}`;
    }
    verInfo(){
        document.write(this.info + "<br>");
    }
}

class Perro extends Animal {
    constructor(especie,edad,color,raza){
        super(especie,edad,color);
        this.raza = null; // colacamos null para poder modificarlo con los metodos set y get.
    }
    set setRaza(newName){// asignamos el metodo set y definimos setRaza con el parametro newName, para guiarnos con ese nombre en la modificacion
        this.raza = newName;// lo asignamos en el this.raza para modificarlo
    }
    get getRaza(){
        return this.raza;// returnamos el valor de this.raza
    }
}

const perro = new Perro("Perro",4,"Marron","Marron");

perro.setRaza = "Doberman";// modificamos el valor de "newName"
document.write(perro.getRaza);// aca obtenemos el valor que nos dio getRaza en la pantalla
```