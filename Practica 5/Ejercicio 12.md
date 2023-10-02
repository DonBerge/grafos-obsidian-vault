Sea el grafo $G_n$ donde $V(G)$ son las posibles permutaciones de $[n]$ y dos vértices $p$ y $q$ son adyacentes $\iff$ $p_i \neq q_i$ $\forall i = 1,\dots,n$ 

Resolver el problema equivale a encontrar un camino hamiltoniano.

b)
$n=1$)
	Si, hay una sola permutación por lo que el resultado es $1$

$n=2$)
	Si, el camino hamiltoniano es $12$,$21$

$n=3$)
	No hay camino hamiltoniano porque el grafo es disconexo(son 2 grafos $C_3$ disconexos)

$n=4$)
	Hay solución, $1234$, $2341$, $3412$, $4123$, $3214$, $2143$, $1432$, $4321$, $3142$, $1423$, $4231$, $2314$, $3421$, $4213$, $2134$, $1342$, $2413$, $4132$, $1324$, $3241$, $4312$, $3124$, $1243$, $2431$
	(Nota de como llegar, empezar por $1234$ e ir rotando los dígitos a la izquierda, tras 4 permutaciones elegir otra permutación distinta y repetir hasta escribir 4 permutaciones)