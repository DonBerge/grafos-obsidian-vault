Si $G$ y $H$ son isomorfos, y $G$ es bipartito entonces $H$ es bipartito.

$G$ es bipartito, por lo tanto su conjunto de vértices puede particionarse en $2$ conjuntos $X$ e $Y$ donde $e=uv$ arista de $G$ cumple que $u \in X \land v \in Y$ o viceversa.

Como $G$ y $H$ son isomorfos, existe un isomorfismo $\sigma$ que preserva adyacencias.

Defino entonces las particiones de $V(H)$:
- $X' = \sigma(X)$
- $Y' = \sigma(Y)$

Dados dos vértices $u,v \in V(G)$ tal que $u'=\sigma(u) \land v'=\sigma(v)$.

Se cumple entonces que:
$u'v' \in E(H) \iff \sigma(u)\sigma(v) \in E(G) \overset{S.P.D.G}{\iff} \sigma(u) \in X \land \sigma(v) \in Y$
$\iff u' \in X' \land v' \in Y'$

Por lo tanto $H$ es bipartito.