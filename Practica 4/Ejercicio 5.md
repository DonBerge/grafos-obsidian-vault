a)
Para cualquier numero natural $n$, $gcd(n,1) = 1$
Esto implica que el vértices $1$ esta conectado a todos los demás vértices(el grafo es conexo). Por lo que $G$ tiene una única componente conexa

b)
Para cualquier numero natural $n$, $gcd(n,n+1) = 1$

Sea $gcd(n,n+1) = k$
$\frac n k$ es un numero natural
$\frac{n+1} k$ es un numero natural
$\frac{n+1}{k} = \frac n k + \frac 1 k$
$\frac 1 k$ tiene que ser un numero natural. Por lo tanto $k$ divide a $1$ y resulta $k=1$.

Es claro entonces que existe el camino simple:
$1 \to 2 \to 3 \to \dots \to 15 \to 1$

No puede existir un camino simple mas largo que este ya que eso implicaría repetir vértices.

La longitud mas larga de un camino simple en el grafo $G$ es $15$