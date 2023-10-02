Si $G[X,Y]$ es un grafo bipartito
a) $\sum_{v \in X} d(v) = \sum_{v \in Y} d(v)$
	Cada arista unida a un vértice de una partición $S$ aporta $1$ unidad a la suma de los grados de la partición.
	Como el grafo es bipartito todas las aristas son de la forma $(x,y)$ donde $x \in X$ y $y \in Y$.
	Por lo tanto si una arista aporta a la suma de $X$ también apunta a una suma de $Y$ y se tiene que $\sum_{v \in X} d(v) = \sum_{v \in Y} d(v)$
b) Si $G$ es a su vez $K$ regular con $k \geq 1$ entonces $|X|=|Y|$
	$\sum_{v \in X} d(v) = \sum_{v \in Y} d(v)$
	$|X| \cdot k = |Y| \cdot k$
	$|X| = |Y|$