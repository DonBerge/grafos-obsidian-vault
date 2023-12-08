Un grafo es autocomplementario si es isomorfo a su complemento

## Teoremas respecto a grafos autocomplementarios
Si $G$ es autocomplementario entonces $G$ es conexo)
	Esto se prueba combinando otros dos teoremas
	1. Si $G$ es conexo cualquier grafo isomorfo a el también lo es.
	2. Si $G$ es disconexo su complemento es conexo.
	Si $G$ es un grafo autocomplementario disconexo entonces su complemento es conexo, pero como también es isomorfo a el entonces $G$ es disconexo. Esto es absurdo por lo tanto un grafo autocomplementario es siempre conexo.
Si $G$ es autocomplementario con $n$ vértices entonces $|E(G)| = \frac{n(n-1)} 4$
	Dos grafos isomorfos tienen la misma cantidad de aristas por lo que
	$|E(G)| = |E(\overline G)| = \frac {n(n-1)} 2 - |E(G)|$
	Y de esto resulta:
	$|E(G)| = \frac{n(n-1)}{4}$
Si $G$ es autocomplementario con $n$ vértices entonces $n=4k$ o $n=4k+1$ con $k \in \mathbb Z^+$
	Se tiene que $|E(G)|=\frac{n(n-1)}{4}$
	$|E(G)|$ es un numero entero por lo que las posibilidades son
	1. $n$ es divisible por $4$ y resulta $n=4k$ con $k$ entero positivo.
	2. $n-1$ es divisible por $4$ y resulta $n=4k+1$ con $k$ entero positivo.
	3. $n$ y $n-1$ son ambos divisibles por $2$ lo cual es imposible ya que implicaría que $n$ es al mismo tiempo un numero par e impar.-
	Por lo tanto se cumple la propiedad.
$C_n$ es autocomplementario $\iff$ $n=5$
	$\implies$)
		$|E(C_n)| = n = \frac{n(n-1)} 4$
		(si $n\neq 0$)
		$1 = \frac{(n-1)} 4$
		$n = 5$
	$\impliedby$)
		Se prueba definiendo un isomorfismo explicito en $C_5$ y $\overline{C_5}$
