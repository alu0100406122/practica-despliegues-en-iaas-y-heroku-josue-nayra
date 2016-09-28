Plugin Exercises!
===================

Este plugin permite introducir ejercicios interactivos, a modo de que el lector pueda, por ejemplo, escribir la solución de un problema para posteriormente el autor del gitbook pueda verificarla y validarla.

¿Cómo podemos instalar este plugin?
-------------
- Debemos instalar el siguiente paquete  y añadirlo a nuestro package.json: 

```
$ npm install gitbook-plugin-exercises --save-dev
```

- Una vez instalado, debemos incorporar el plugin en nuestro fichero book.json

``` 
{
    "plugins": ["exercises"]
}
```


¿Cómo podemos usar este plugin?
-------------

- Definición, sintaxis y estructura

Cada ejercicio debe definirse siguiente la siguiente estructura basada en 4 partes fundamentales:

> 1.- Mensaje u objetivo del ejercicio:


```
>> {% exercise %}
>> "Mensaje o enunciado del ejercicio"

```

> 2.- Código inicial que se muestra al usuario. Punto de partida:

```
>> {% initial %}
>> "Condiciones y datos iniciales que se muestran al usuario para que resuelta el mensaje"
```
> 3.- Solucion del ejercicio

```
>> {% validation %}
>> "Solucion del ejercicio"

```

> 4.- Código de validación de resultado

```
>> {% context %}
>> "Código que comprueba si el resultado del usuario es correcto"

```

> 5.- Fin del ejercicio

```
{% endexercise %}

```

Ejemplo
-------------

- Codigo

```
{% exercise %}
Definir una variable res que contenga el resultado de la siguiente operacion: (5-4).
{% initial %}
var res =
{% solution %}
var resultado = 1;
{% validation %}
assert(resultado == 1);
{% context %}

function magicFunc() {
    return 3;
}
{% endexercise %}

```
{% exercise %}
Definir una variable res que contenga el resultado de la siguiente operacion: (5-4).
{% initial %}
var res =
{% solution %}
var resultado = 1;
{% validation %}
assert(resultado == 1);
{% context %}

function magicFunc() {
    return 3;
}
{% endexercise %}

