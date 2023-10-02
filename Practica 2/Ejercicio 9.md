a)
Lema: Si dos grafos son isomorfos, tienen la misma cantidad de aristas
	Sean $G_1 \simeq G_2$ dos grafos isomorfos.
	Dado que los isomorfismos preservan los grados de los vértices se tiene que
	$2|E(G_1)| = \sum_{v \in V(G_1)} d(v) = \sum_{v \in V(G_1)} d(\sigma(v_1)) = \sum_{v \in V(G_2)} d(v) = 2|E(G_2)|$
	$|E(G_1)| = |E(G_2)|$
Si $G$ es auto complementario entonces $G$ y $\overline{G}$ tienen la misma cantidad de aristas, por lo tanto si $|E(G)|=m$
$m = \binom n 2 - m$
$2m = \binom n 2$
$m = \frac{n(n-1)}{4}$

b)
La conectividad de un grafo es preservada por un isomorfismo
Si un grafo es disconexo entonces su complemento es conexo

Si un grafo autocomplementario es disconexo entonces su complemento es conexo, pero como su  complemento es a su vez isomorfo entonces es conexo. Absurdo

Por lo tanto un grafo autocomplementario tiene que ser conexo.

c)
$m = \frac{n(n-1)}{4}$ es un numero entero

No puede pasar que $n$ y $n-1$ sean ambos divisibles por $2$ asi que al menos uno de los $2$ tiene que ser divisible por $4$

$n = 4k$
$n-1 = 4k \implies n = 4k+1$
Con $k \in \mathbb N_0$