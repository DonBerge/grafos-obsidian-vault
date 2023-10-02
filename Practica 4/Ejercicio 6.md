a)
Eliminar un vértice del grafo no puede disminuir la cantidad de componentes conexas, solo aumentarlas.(nota si puede, es el caso de eliminar un vertice aislado)

Por lo que se tiene que $c(G) \leq c(G-v)$
Por lo que:
$c(G)-1 \leq c(G) \leq c(G-v)$

$c(G-v) \leq c(G) +d(v) - 1$ pendiente

b)
Si $G$ es conexo entonces $c(G)=1$
$c(G-v) \leq c(G) + d(v) - 1 = 1 + d(v) - 1 = d(v)$

c)
Del ejercicio $a$ se tiene que
$d(v) \geq c(G-v) - c(G) +1 \geq 1 + c(G) - c(G) +1 \geq 2$ 

d)
Si $c(G-v) = c(G)$ entonces para cualquier par de vértices $u,w$ de la componente conexa existe un camino simple que no pasa por $v$

Se tiene que $d(v)\geq 2$:
Si $v$ tiene un lazo entonces el ciclo buscado es el camino cerrado $v \to v$ que pasa por el lazo.
Si $v$ tiene dos aristas paralelas conectadas a un vértice $x$ entonces el ciclo pedido es $v\to x \to v$.
Si no entonces $v$ esta conectado a dos vértices $u,w$ distintos.
Sea $x_1 \to x_2 \to x_3 \to \dots x_k$ un camino simple donde $x_1 = u$, $x_k = w$ y $\forall i: x_i \neq v$ el bucle pedido es $v \to u=x_1 \to x_2 \to x_3 \to \dots x_k = w \to v$
