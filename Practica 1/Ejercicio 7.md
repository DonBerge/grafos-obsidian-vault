a) En un grafo simple $G(V,E)$ de $n$ vértices y $m$ aristas, $m \leq \binom n 2$
	Por el lema del apretón de manos: $\sum_{v \in V} g(v) = 2|E|$
	El máximo grado posible de un vértice en un grafo simple es $n-1$
	$2m = 2|E| = \sum_{v \in V} g(v) \leq \sum_{v \in V} n-1 = n(n-1)$
	$m \leq \frac{n(n-1)}2$
	$m \leq \binom n 2$

b) Describir los grafos simple donde $m = \binom n 2$
	Son los grafos donde $g(v)=n-1$, es decir, los grafos completos