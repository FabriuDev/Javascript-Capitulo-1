# Crear soluciones (Parte 3)
---

- crear las funciones y caracteristicas basicas de los celulares.
  - hacer 3 celulares
  - diferenciar si es de alta gama o no
  - administrar las aplicaciones para descargar, seleccionar 2 apps de las 7 destacadas.

> Problema 1

```js
class Celular{//creacion de clase
    constructor(color,peso,rdp,rdc,ram){//definiendo las caracteristicas y asignando los valores
        this.color = color;
        this.peso = peso;
        this.resolucionDePantalla = rdp;
        this.resolucionDeCamara = rdc;
        this.MemoriaRam = ram;
        this.encendido = false;
    }
    botonDeEncendido(){
        if(this.encendido == false){
            alert("Celular prendido");
            this.encendido = true;
        } else {
            alert("Celular apagado");
            this.encendido = false;
        }
    }
    reiniciar(){
        if(this.encendido == true){
            alert("El telefono se esta reiniciando")
        } else {
            alert("El telefono esta apagado");
        }
    }
    tomarFoto(){
        alert(`Capturando foto con una resolucion de: ${this.resolucionDeCamara}`);
    }
    grabarVideo(){
        alert(`Grabando video con una resolucion de: ${this.resolucionDeCamara}`);
    }
    mobileInfo(){
        return `Color: <b>${this.color}</b><br>
                Peso: <b>${this.peso}</b><br>
                Tamaño: <b>${this.resolucionDePantalla}</b><br>
                Resolucion de Video: <b>${this.resolucionDeCamara}</b><br>
                Memoria ram: <b>${this.MemoriaRam}</b><br>`
    }
}

const celular1 = new Celular("Rojo","130g","5'","Full HD","2GB");//definiendo los valores de cada atributo
const celular2 = new Celular("Verde","120g","4.6'","HD","1GB");//definiendo los valores de cada atributo
const celular3 = new Celular("Azul","105g","7'","4k","4GB");//definiendo los valores de cada atributo




celular1.botonDeEncendido();//ejecutando las acciones del celular
celular1.tomarFoto();
celular1.grabarVideo();
celular1.reiniciar();
celular1.botonDeEncendido();

document.write(`
    ${celular1.mobileInfo()} <br>
    ${celular2.mobileInfo()} <br>
    ${celular3.mobileInfo()}`);
```
---

>Problema 2

```js
class Celular{//creacion de clase
    constructor(color,peso,rdp,rdc,ram){//definiendo las caracteristicas y asignando los valores
        this.color = color;
        this.peso = peso;
        this.resolucionDePantalla = rdp;
        this.resolucionDeCamara = rdc;
        this.MemoriaRam = ram;
        this.encendido = false;
    }
    botonDeEncendido(){
        if(this.encendido == false){
            alert("Celular prendido");
            this.encendido = true;
        } else {
            alert("Celular apagado");
            this.encendido = false;
        }
    }
    reiniciar(){
        if(this.encendido == true){
            alert("El telefono se esta reiniciando");
        } else {
            alert("El telefono esta apagado");
        }
    }
    tomarFoto(){
        alert(`Capturando foto con una resolucion de: ${this.resolucionDeCamara}`);
    }
    grabarVideo(){
        alert(`Grabando video con una resolucion de: ${this.resolucionDeCamara}`);
    }
    mobileInfo(){
        return `Color: <b>${this.color}</b><br>
                Peso: <b>${this.peso}</b><br>
                Tamaño: <b>${this.resolucionDePantalla}</b><br>
                Resolucion de Video: <b>${this.resolucionDeCamara}</b><br>
                Memoria ram: <b>${this.MemoriaRam}</b><br>`;
    }
}

class celularAltaGama extends Celular {
    constructor(color,peso,rdp,rdc,ram,rdce){
        super(color,peso,rdp,rdc,ram);
        this.resolucionDeCamaraExtra = rdce;
    }
    grabarVideoLento(){
        alert("Estas grabando en camara lenta");
    }
    reconocimientoFacial(){
        alert("Vamos a iniciar un reconocimiento facial");
    }
    infoAltaGama(){
        return this.mobileInfo() + `Resolucion de camara extra: ${this.resolucionDeCamaraExtra}`;
    }
}

const celular1 = new celularAltaGama("Rojo","130g","5.2","4k","3GB","Full HD");
const celular2 = new celularAltaGama("Negro","125g","6","4k","4GB","HD");

document.write(`
        ${celular1.infoAltaGama()} <br><br>
        ${celular2.infoAltaGama()} <br>`)
```

> Problema 3

```js
class App {
    constructor(descargas,puntuacion,peso){
        this.descargas = descargas;
        this.puntuacion = puntuacion;
        this.peso = peso;
        this.iniciada = false;
        this.instalada = false;
    }
    abrir(){
        if(this.iniciada == false && this.instalada == true){
            this.iniciada = true;
            alert("Aplicacion Encendida");
        }
    }
    cerrada(){
        if(this.iniciada == true && this.instalada == true){
            this.iniciada = false;
            alert("Aplicacion Cerrada");
        }
    }
    instalar(){
        if(this.instalada == false){
            this.instalada = true;
            alert("Aplicacion Instalada correctamente");
        }
    }
    desinstalar(){
        if(this.instalada == true){
            this.instalada = false;
            alert("Aplicacion Desinstalada");
        }
    }
    appInfo(){
        return `
        Descargas: <b>${this.descargas}</b><br>
        Puntuacion: <b>${this.puntuacion}</b><br>
        Peso: <b>${this.peso}</b><br>`;
    }
}

// app.instalar();      // funciones basicas de las aplicaciones
// app.abrir();
// app.cerrada();
// app.desinstalar();

const app = new App("1M","3.7 Estrellas","240Mb"); // caracteristicas de las aplicaciones
const app2 = new App("50.000","2.8 Estrellas","540Mb");
const app3 = new App("750.000","4.5 Estrellas","900Mb");
const app4 = new App("20.000","5 Estrellas","320Mb");
const app5 = new App("10.000","1.8 Estrellas","650Mb");
const app6 = new App("800","2.3 Estrellas","52Mb");
const app7 = new App("5.650","4.1 Estrellas","92Mb");

document.write(`
    ${app.appInfo()}<br>
    ${app2.appInfo()}<br>
    ${app3.appInfo()}<br>
    ${app4.appInfo()}<br>
    ${app5.appInfo()}<br>
    ${app6.appInfo()}<br>
    ${app7.appInfo()}<br>`); // descripcion en pantalla de las aplicaciones
```