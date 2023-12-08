Un grafo $G$ es conexo $\iff$ $\forall u,v \in V(G) :$ existe un $uv$-camino

Si $H$ es un subgrafo conexo maximal de $G$ es una componente conexa del grafo.

El grafo trivial es conexo.

El grafo vacío no tiene componentes conexas.

### Condición suficiente de conectividad para grafos simples
Sea $G$ un grafo simple con $n$ vértices y $m$ aristas que cumple $m > \binom {n-1} 2$, entonces $G$ es un grafo conexo.

Esto lo pruebo por inducción en la cantidad de vértices del grafo.

CB) $n=3$
$\binom {n-1} 2 = \binom 2 2 = 1 < 2, 3$
Los únicos grafos de tres vértices con $2$ o $3$ aristas son $P_3$ y $C_3$, los cuales son conexos.

HI) $\forall n \in \mathbb N : G=(V,E)$ con $|V(G)|=n$, $|E(G)|=m$ y $m > \binom {n-1} 2$ $\implies$ $G$ es conexo.

PI)

Lema: $\forall v \in V(G)  \exists u \in V(G) :$ $uv \in E(G)$
	Suponiendo que existe un vértice $v$ que esta aislado. Entonces todas las aristas del grafo son de la forma $uw$ donde $u \neq v$ y $w \neq v$. La cantidad de pares de esta forma es $\binom {n-1} 2$, pero hay mas aristas del grafo que pares de estos elementos. Por principio del palomar, no puede haber un vértice aislado.

Sea entonces un vértice cualquiera del grafo.

$|V(G)| = n+1$

$m > \binom{n} 2 = \binom {n-1} 1 + \binom {n-1} 2 = n-1 + \binom {n-1} 2$

Dado un vértice $v$ cualquiera del grafo y el grafo $G-v$
$n-1 \geq d(v)$
$|E(G-v)| = |E(G)| - d(v) = m - d(v) > (n-1 - d(v)) + \binom{n-1} 2 \geq \binom{n-1} 2$
Entonces por HI el grafo $G-v$ es conexo y por el lema anteriormente demostrado, el grafo es conexo.