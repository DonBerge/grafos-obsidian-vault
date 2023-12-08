a)

El grafo de Petersen es un grafo $3$-regular.

Si no existe un matching perfecto entonces el grafo no es $1$-factoreable.

Suponiendo que existe 1 matching perfecto, al eliminar dicho matching se tiene un grafo $2$-regular, por lo que dicho grafo esta compuesto solo por ciclos.

Se pueden formar varias componentes conexas con ciclos, solo las que están compuestas únicamente por ciclos pares pueden formar un matching perfecto.

La única pareja de este tipo es la que forma un $C_4$ y un $C_6$, sin embargo dicha pareja no puede formarse ya que el grafo de Petersen no tiene ningún $C_4$ como subgrafo.

Por lo tanto el grafo resultante de eliminar el matching perfecto no tiene mas matchings perfectos. Como consecuencia el grafo de Petersen no puede ser $1$-factoreable.

b)
Pruebo por inducción en $n$
CB) $n=1$
	Tiene una única arista que une dos vértices, esa única arista es el matching perfecto del 1-factoreo
HI) $\forall n \in \mathbb N$: $K_{n,n}$ es $1$-factoreable
PI)
	Sea el grafo $K_{n+1,n+1}$.
	Dada la partición $X = \{v_1,\dots,v_{n+1}\}$ y $Y = \{u_1,\dots,u_{n+1}\}$. Las aristas $u_iv_i$ con $i \in 1,\dots, n$ forman un matching perfecto. Al eliminar esas aristas del grafo se tiene un $K_{n,n}$ que por HI tiene un $1$-factoreo. Al añadir los matchings de dicha factorización con las aristas de antes se tiene un $1-$factoreo de $K_{n+1,n+1}$.