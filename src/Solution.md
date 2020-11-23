## Solución
La librería consta de una clase principal con dos métodos públicos que para resolver los dos problemas anteriormente planteados. Para resolver los problemas, se basa en el algoritmo de dijkstra y usa una cola de prioridad, implementada en PriorityQueue.php.

**1) Mostrar la ruta más rápida de un origen a un destino.**
```
getRoute(<origen>,<destino>)
```
Devuelve: array de 2 elementos: "distance" con el coste del viaje y "route", un array con las ciudades a recorrer.

Ejemplo:
```
<?php
require("FastestRoute.php");
$travel= new FastTravel($cities,$connections);
var_dump($travel->getRoute("Logroño","Ciudad Real"));

```
Resultado:
```
Array
(
    [distance] => 16
    [route] => Array
        (
            [0] => Logroño
            [1] => Zaragoza
            [2] => Lleida
            [3] => Castellón
            [4] => Ciudad Real
        )

)


```
**2) Mostrar la distancia más corta desde un origen dado a todos los destinos**
```
getDistances(<origen>)
```
Devuelve: array con las ciudades como claves y las distancias como valor.

Ejemplo:

```
<?php
require("FastestRoute.php");
$travel= new FastTravel($cities,$connections);
var_dump($travel->getDistances("Madrid"));

```
Resultado:
```
Array
(
    [Logroño] => 8
    [Zaragoza] => 5
    [Teruel] => 3
    [Madrid] => 0
    [Lleida] => 8
    [Alicante] => 10
    [Castellón] => 11
    [Segovia] => 15
    [Ciudad Real] => 17
)

```
