# Capitulo 1 (Crear Soluciones)
---

- Cofla va a la heladeria y quiere comprar un helado + saber cuanto dinero le sobra!

```js
dineroCofla = prompt('Cuanto dinero tenes Cofla?');//variable
dineroCofla = parseInt(dineroCofla);//esto sirve para pasar a entero una cadena de texto

if (dineroCofla >= 0.6 && dineroCofla < 1) {// se cumple la condicion y se usa un solo if
    alert('cofla, Comprate el helado de agua');
    alert('y te sobran ' + (dineroCofla - 0.6));//para encadenar esta operacion, necesitamos (parentesis)
}

else if (dineroCofla >= 1 && dineroCofla < 1.6) {// se cumple la condiciony se pueden usar muchos else if
    alert('cofla, Comprate el helado de crema');
    alert('y te sobran ' + (dineroCofla - 1));
}

else if (dineroCofla >= 1.6 && dineroCofla < 1.7) {
    alert('cofla, Comprate el helado de Tercera marca');
    alert('y te sobran ' + (dineroCofla - 1.6));
}

else if (dineroCofla >= 1.7 && dineroCofla < 1.8) {
    alert('cofla, Comprate el helado de Segunda marca');
    alert('y te sobran ' + (dineroCofla - 1.7));
}

else if (dineroCofla >= 1.8 && dineroCofla < 2.9) {
    alert('cofla, Comprate el helado de Primera marca');
    alert('y te sobran ' + (dineroCofla - 1.8));
}

else if (dineroCofla >= 2.9) {
    alert('cofla, comprate un 1/4 de helado');
    alert('y te sobran ' + (dineroCofla - 2.9));
}

else {
    alert('Lo siento cofla! no te alcanza para nada')//si nada de lo anterior se cumple, sale esto
}
```