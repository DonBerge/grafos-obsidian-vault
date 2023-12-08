Pruebo por inducción en la cantidad de vértices

CB) $n=0$
	El grafo vacío, trivialmente no tiene matchings
	$n=1$
	Un grafo con un solo vértice, este grafo no tiene matchings.
HI) Todo árbol $T$ con $n$ vértices tiene como mucho un matching perfecto.

PI)
	Si $T$ es un árbol con $2$ o mas vértices, entonces tiene al menos una hoja $h$. La única forma de que un matching perfecto sature la hoja es usando la única arista que la conecta. Luego el árbol $T-h$ es un árbol que por hipótesis inductiva, tiene un único matching perfecto. Por consiguiente, $T$ tiene a lo sumo un matching perfecto. 
