a)
Como $G$ es un subgrafo de inducido de $G_M$, se tiene que $\omega(G_M) \geq \omega(G)$
Ninguno de los vértices $u$ están conectados entre si y el vértice $w$ solo esta conectado a los vértices $u$.
Por lo que una clique de $G$ solo puede extenderse con al menos un vértice $u$.

S.P.D.G que la clique máxima esta formada por los vértices $\{v_1,\dots,v_k\}$ y se extiende la clique usando un vértice $u_j$.

Para que la clique crezca tiene que pasar que $v_j,v_i \in E(G)$ para todo $i \in [k]$, esto quiere decir que $\{v_1,\dots,v_k,v_j\}$ es una clique de mayor tamaño. Lo cual es absurdo ya que se parte del supuesto que se tenia una clique máxima.

Por lo que la clique máxima de $G$ es también máxima en $G_M$, $\omega(G_M)=\omega(G)$

b)
Sea $f$ un coloreo optimo de $G$
Puesto que todos los vecinos de $v_i$ son también vecinos de $u_i$, a ambos vértices se les puede asignar el mismo colores. Intentar usar menos colores terminara en dos vértices del mismo color unidos, por lo que este coloreo es optimo.
Luego como $w$ esta unido a todos los vértices $u$, $w$ se necesita al menos un color mas para colorear $w$ por lo que $\chi(G_M)=\chi(G)+1$.

c)
Se puede hacer la construcción de $G_M$ sobre $G_M$ $k$ veces para construir el grafo $H$ pedido.

Si $G$ es bipartito, probar que existe un matching $M$ tal que $\frac{|E|}{\Delta(G)} \leq |M|$
Si existe un matching $M$ que lo cumpla entonces para cualquier matching mas grande que $M$ se va a cumplir, en particular se tiene que cumplir para el matching máximo del grafo. Entonces se tiene que $\frac{|E|}{\Delta(G)} \leq \alpha'(G) = \beta(G)$

Por lo que hay que probar que: $|E| \leq \beta(G)\cdot \Delta(G)$

La propiedad es cierta ya que para los vértices $\{v_1,\dots,v_k\}$ de un cubrimiento mínimo de $G$

$|E| \leq \sum_{i=1}^k d(v_i) \leq \beta(G) \cdot \Delta(G)$

$283.\overline{3}$