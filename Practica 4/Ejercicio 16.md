El grafo $G$ tiene un recorrido de Euler $\iff$ tiene exactamente dos vértices de grado impar.

$\implies$)
Por hipótesis $G$ tiene un recorrido de Euler que empieza y termina en dos vértices. Sean $u$ y $w$ dichos vértices, el grafo $G'$ con $V(G')=V(G)$ y $E(G')=E(G) \cup wu$ es euleriano y tiene todos sus vértices de grado par. La eliminación de la arista $wu$ da como resultado que tanto $u$ como $w$ son vértices de grado impar. Por lo que $G$ solo tiene dos vértices de grado impar.
$\impliedby$)
Por un argumento similar, si se añade una arista entre los vértices de grado impar se tiene que todos los vértices tienen grado par y el grafo aumentado es euleriano. Luego el recorrido formado al sustraer la arista recién agregada al circuito de Euler del grafo aumentado es el recorrido buscado.