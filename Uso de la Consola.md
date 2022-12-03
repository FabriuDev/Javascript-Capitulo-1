# Todo sobre la consola
---

> `funciones de registro:`

assert() = aparece un mensaje de error en la consola si la afirmación es falsa, si la afirmación es verdadera no aparece nada (no estandar)

clear() = limpia la consola

error() = muestra un mensaje de error en la consola web.

info() = emite un mensaje informativo en la consola web. 
en firefox y chrome, se muestra un pequeño icono “i” junto a estos elementos en el registro de la consola web.

log() = muestra un mensaje en la consola web (o del intérprete de javascript).

table() = esta funcion toma un argumento obligatorio: data, que debe ser un array o un objeto, y un parametro adicional: columns y nos muestra una tabla en consola.

warn() = imprime un mensaje de advertencia en la consola web.

dir() = despliega una lista interactiva de las propiedades del objeto javascript especificado. (no estandar)



> `funciones de conteo:`

count() = registra el numero de veces que se llama a count(). esta funcion toma como argumento opcional una etiqueta.

countReset() = resetea el contador console.count()


> `funciones de agrupacion:`

group() = crea un nuevo grupo en linea en el registro de la consola web.

grupEnd() = remueve un grupo en linea en el registro de la consola web.

groupCollapsed() = crea un grupo en linea pero contraido, el usuario debe expandirlo para verlo.

> `funciones de temporización:`

time() = inicia un temporizador.

timeEnd() = registra el valor actual de un temporizado.

timeLog() = detiene un temporizador.
