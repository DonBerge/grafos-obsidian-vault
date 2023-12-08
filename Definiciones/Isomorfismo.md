Un isomorfismo entre dos grafos $G=(V,E)$ y $H=(U,Q)$ es una función biyectiva de $V \to U$ que preserva adyacencias.

Mas formalmente
$f$ es un isomorfismo entre $G=(V,E)$ y $H=(U,Q)$ $\iff$ $f:V\to U$ es biyectiva y $uv \in E \iff f(u)f(v) \in Q$

Si existe un isomorfismo entre 2 grafos $G$ y $H$ se dice que $G$ es isomorfo a $H$ y se denota $G\simeq H$

Por ejemplo, $K_4$ es isomorfo a $W_3$

[[Drawing 2023-10-06 15.28.01.excalidraw]]

El isomorfismo buscado es $f(u_i) = v_i$

Tambien es posible denotar el isomorfismo como una matriz:
$$f = \begin{pmatrix} u_1 & u_2 & u_3 & u_4 \\ v_1 & v_2 & v_3 & v_4\end{pmatrix}$$
## Invariante via isomorfismo
Se dice que una propiedad $\mathcal P$ es invariante vía isomorfismo si $\forall G$ grafo que cumple $\mathcal P$ y $\forall H$ isomorfo a $G$ se tiene que $H$ cumple $P$

Aquí hay algunas invariantes vía isomorfismo

1. Misma cantidad de vértices de grado k
2. Misma cantidad de aristas uniendo vértices del mismo grado
3. Ser Conexo
4. Ser bipartito
5. Misma secuencia de grados
6. Sus complementos son a su vez isomorfos

Por lo general las invariantes son condiciones necesarias de isomorfismo pero no suficientes.
## Caracterización de isomorfismo
Dos grafos son isomorfos $\iff$ sus vértices pueden reordenarse de manera que sus matrices de adyacencia sean iguales.

## Caso especial: automorfismo
Un automorfismo de un grafo $G$ es un isomorfismo de $G$ en si mismo.