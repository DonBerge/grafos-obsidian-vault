Sea $G=(V,E)$ un grafo

Un grafo $H=(V',E')$ tal que $V' \subseteq V$ y $E'\subseteq E$ se dice que es un subgrafo de $H$.

### Subgrafo inducido
Sea $U \subseteq V(G)$), el subgrafo $H$ de $G$ inducido por el conjunto $U$ es el grafo que cumple que $V(H) = U$ y $E(H)=\{uv : u \in U \land v \in U\}$

### Grafo menos un vértice
Sea $v \in V(G)$, el grafo $G-v$ es el subgrafo de $G$ inducido por $V(G)-\{v\}$

### Grafo menos una arista
Sea $e \in E(G)$, el grafo $G \backslash e$ es el subgrafo de $G$ que cumple $V(G\backslash e) = V(G)$ y $E(G\backslash e)=E(G) - \{e\}$