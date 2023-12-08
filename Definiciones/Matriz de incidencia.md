Sea un grafo $G$ donde $|V(G)|=n$ y $|E(G)|=m$, la matriz de incidencia del grafo $G$ es una matriz $n \times m$ donde $A_{ij}=1$ si el vértice $v_i$ es incidente con la arista $e_j$.

Para el caso de la matriz de incidencia
$$\begin{pmatrix}
\ &e_1 & e_2 & e_3 & e_4 \\
v_1 & 1 & 1 & 1 & 0 \\
v_2 & 1 & 0 & 0 & 0 \\
v_3 & 0 & 1 & 0 & 1 \\
v_4 & 0 & 0 & 1 & 1
\end{pmatrix}$$

Se tiene que:
- La arista $e_1$ une los vértices $v_1$ y $v_2$.
- La arista $e_2$ une los vértices $v_1$ y $v_3$.
- La arista $e_3$ une los vértices $v_1$ y $v_4$.
- La arista $e_4$ une los vértices $v_3$ y $v_4$.

Para el caso de un grafo dirigido se tiene que
$$A_{ij} = \begin{cases}
-1 & \text{si la arista }e_j \text{ sale del vertice } v_i \\
1 & \text{si la arista }e_j \text{ entra del vertice } v_i \\
0 & \text{en cualquier otro caso}
\end{cases}$$