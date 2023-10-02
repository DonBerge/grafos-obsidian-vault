8)
a) Dos grafos $C_3$ conectados por una arista $e$, los vértices de corte son los extremos de la arista $e$
b) El grafo $K_6$
Si se elimina un vértice $v$ de $K_6$, sigue habiendo un camino cualquiera entre dos vertices $u$ y $w$
Respuesta si.
$E(K_6) = \{(a,b) : a,b \in V\} = \bigsqcup_{b \in V} \{(a,b) : a \in V\}$
$E(K_6 - v) = \bigsqcup_{b \in V} \{(a,b) : a \in V\} - \{(a,v) : a \in V\} = \bigsqcup_{b \in V - v} \{(a,b) : a \in V-v\}$
$=\{(a,b) : a,b \in V-v\}$
Dos vertices cualesquiera siguen conectados
c)
Dado un grafo $G$ con un vertice $v$.
$v$ es de corte $\iff$ $\exists u,w \in V :$ todos los caminos entre $u$ y $w$ pasan por $v$

$\impliedby$)
Sea el grafo $G-v$, en dicho grafo los vértices $u,w$ están desconectados(si no lo están existe un camino entre $u$ y $w$ que no pasa por $v$ lo cual es absurdo).

$G-v$ tiene al menos dos componentes conexas separadas(una donde esta $u$ y otra donde esta $w$)

En $G$ dichas componentes no están presentes(ya que existe un camino entre $u$ y $w$ que pasa por $v$)
por lo que $G$ tiene menos componentes que $G-v$, $v$ es un vértice de corte.

$\implies$
Pruebo la contrarrecíproca: $\forall u,w \in V :$ existe un camino entre $u,w$ que no pasa por $v$ $\implies$ $v$ no es de corte

Dado el grafo $G-v$, se tiene que todo par de vértices que estaban conectados en $G$ lo siguen estando en $G-v$(ya que ninguna arista del camino tiene a $v$ como extremo, dichas aristas siguen perteneciendo al grafo $G-v$)

Por lo que eliminar $v$ no afecta a la conectividad del grafo, $v$ no es de corte