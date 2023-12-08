Un recorrido/circuito de Euler es un recorrido del grafo que visita todas las aristas del grafo exactamente una vez.

Si un grafo $G$ tiene un circuito euleriano se dice que $G$ es euleriano.
## Caracterización de grafos eulerianos
$G$ es euleriano $\iff$ todos sus vértices tienen grado par

$\implies$)
Si $G$ es euleriano tiene un circuito que visita todas sus aristas. Para cualquier vértice $u$ del circuito hay una sucesión $u e_1 v_1 e_2 \dots e_s v_k u$ que representa el circuito euleriano. Si resulta que $u$ tiene grado impar, entonces $u$ no puede ser el vértice final del circuito(dado que al consumir todas las aristas no se puede volver). Por lo que todos los vértices tienen grado par.

$\impliedby$)
Sea $W=u,e_1,v_1,\dots,e_k,v_k$ el recorrido de mayor longitud del grafo.
Todas las aristas incidentes en $v_k$ pertenecen a $W$(sino no seria maximal) por lo que se tiene que $u=v_k$ y $W$ es un circuito

Si $W$ no es un circuito de Euler, dado que $G$ es conexo, existe una arista por fuera de $W$ pero incidente en un vértice de $W$, sea dicha arista $e=u,v_s$ entonces $u,v_s,W,v_s$ es un recorrido de mayor longitud que $W$, absurdo.

