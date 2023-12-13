Lema: Todo cubrimiento de un grafo $G$ es también un cubrimiento de un subgrafo inducido, es decir, $G-v$ $\forall v$

Por definición un cubrimiento de $G$ es un subconjunto $B$ de vértices tal que todas las aristas de $G$ tienen un extremo en $B$.

Si se borran todas las aristas en $v$, entonces $B$ sigue siendo un cubrimiento(puesto que no se añadieron nuevas aristas que no tengan extremo en $B$ y el mismo conjunto $B$ sigue intacto). Sea $E'$ el conjunto resultante de estas operaciones, se tiene que $B$ sigue siendo un cubrimiento y ninguna arista de $E'$ tiene extremo en $v$($v$ es un vértice de grado $0$), por ende el conjunto $B-v$ es un cubrimiento de $E'$ y por ende es un cubrimiento de $G-v$, por ende $\beta(G) = |B| \geq|B-v| = \beta(G)-1 \geq \beta(G-v)$