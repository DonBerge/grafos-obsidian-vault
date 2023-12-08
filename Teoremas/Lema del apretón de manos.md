$$\forall G=(V,E) : \sum_{v \in V} d(v) = 2|E|$$
## Demostración
La demostración la hago por inducción matemática en la cantidad de aristas del grafo

CB) $|E|=0$
En este caso todos los vértices tienen grado $0$ y la sumatoria se cumple
HI) $\forall n \in N: G=(V,E) \land |E| = n \implies \sum_{v \in V} d(v) = 2|E|$
PI) $|E(G')| = n+1$
Sea $e=(u,w)$ una arista del grafo.
$G' = G \backslash e$ es un grafo con $|E(G')|=n$, por lo tanto $\sum_{v \in V} d(v) = 2|E(G')|$
$\sum_{v \in V(G')} d(v) = 2|E(G')|$
$\implies$
$\sum_{v \in V(G')} d(v) + 2 = 2|E(G')| + 2$

Si $u = w$, $e$ es un lazo y el grado de $u$ aumenta en $2$.
$\sum_{v \in V} d(v) + 2 = 2|E(G')| + 2$
$\implies$
$\sum_{v \in V(G')} d(v) + d(w) + 2= 2|E(G')|+2$
$\implies$
$\sum_{v \in V(G)} d(v) = 2(|E(G')|+1) = 2|E(G)|$

Si $u \neq w$, el grado de cada vértice aumenta en $1$
$\sum_{v \in V} d(v) + 2 = 2|E(G')| + 2$
$\sum_{v \in V} d(v) + (d(u)+1) + (d(w) + 1) = 2(|E(G')|+1)$
$\sum_{v \in V} d(v) = 2|E(G)|$

La propiedad se cumple

$\blacksquare$
