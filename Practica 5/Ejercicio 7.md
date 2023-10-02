Suponiendo que el grafo comienza en un vértice $v$ de una partición $X$ del grafo.

Se pueden elegir $n$ aristas para formar el ciclo hamiltoniano.
Luego se pueden elegir $n-1$ aristas, a partir de aquí se llega a otro vértice de la partición $Y$. Debido a que uno de los vértices de la partición $X$.
Desde este nuevo vértice se pueden elegir $n-1$ aristas(porque un vértice de $Y$ ya esta visitado).
Desde el nuevo vértice de $Y$ se pueden elegir $n-2$ aristas(porque $2$ vértices ya están visitados).
Y así se tiene el resultado:
$n\cdot (n-1) \cdot (n-1) \cdot (n-2) \cdot \dots \cdot 2 \cdot 1 \cdot 1$
$=n! \cdot (n-1)!$

Este conteo cuenta un mismo ciclo dos veces, ya que cuenta un ciclo por una arista empezada y luego cuenta el mismo ciclo por la arista que termina. Así que hay que dividir el resultado por $2$

El resultado final es $\frac 1 2 \cdot n! \cdot (n-1)!$ 

En cuanto a la cantidad de caminos hamiltonianos, para cada ciclo hamiltoniano distinto se puede borrar una de sus $n$ aristas por lo que la cantidad de caminos hamiltonianos va a ser $\frac 1 2 \cdot n! \cdot (n-1)! \cdot n = \frac 1 2 (n!)^2$
