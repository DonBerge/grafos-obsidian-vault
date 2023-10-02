a) $P_n$
Todas las aristas de $P_n$ son de corte ya que ninguna arista pertenece a un ciclo.
Si $n\geq 3$,los únicos vértices de corte son los que no son extremos del grafo. Caso contrario no hay vértices de corte.
b) $C_n$
Ninguna arista es de cortes ya que todas pertenecen a un ciclo(el mismo grafo es un ciclo).
Ningún vértice es de corte.
$\forall v \in V$ existe un camino de la forma $v \to u_1 \to u_2 \to \dots \to u_{n-1} \to v$
Si se elimina el vértice $v$ también se eliminan las aristas $vu_1$ y $u_{n-1}v$
El camino resultante queda
$u_1 \to u_2 \to \dots \to u_{n-1}$

Todos los vértices restantes quedan conectado por un camino, $v$ no es de corte

c) $K_n$
Si $n\geq 3$ entonces no hay aristas de corte.
Dada una arista $uv$, existe otro vértice $w$ con aristas $uw$ y $wv$
Se forma el ciclo: $u \to w \to v \to u$ la arista $uv$ no es de corte
Ningún vértice es de corte ya que para cualquier par de vértices $u$ y $w$ existe un camino entre ellos que no pasa por $v$(es la misma arista $uw$).