# [Nothing is Something](https://www.youtube.com/watch?v=OMPfEXIlTVE) [00:35:52] by **Sandi Metz** (2015)

How to program without using if?
Explica como utilizar el patron strategy para obtener
combinaciones de House con distintos formatos y distintos sort_algorithms
Que con herencia estamos limitados para obtener esto.
Para explicar utiliza la comparacion del metodo en diferentes branches.
Ahi se da cuenta de que lo que varia es el orden.
Entonces contruye 2 estrategias de ordenamiento, la que no hace nada DefaultOrder y la otra RandomOrder
La estrategia es identificar que es lo que se hace distinto en cada branch del condicional, darle 
un nombre y crear 2 objetos que tomen la responsabilidad de ese comportamiento.

