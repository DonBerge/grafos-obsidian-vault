Dado el grafo $G[X,Y]$ bipartito construyo una red de flujo $H$ definida como sigue:
- El vértice fuente $a$ esta unido a todos los vértices $X$ por aristas de peso 1.
- El vértice sumidero $z$ esta unido a todos los vértices de $H$ por aristas de peso 1.
- Las aristas que conectan los vértices $X$ e $Y$ tienen peso $\infty$.

Ahora ejecuto el algoritmo de Ford-Fulkerson a la red $H$.

Comenzando por el flujo nulo $f$

Empiezo por el vértice $a$, inicialmente todos los vértices cumplen la condición $f(a,x) < c(a,x)$(puesto que $f$ es un flujo nulo), así que queda determinado $U=X$.

Luego tomo un vértice $x \in U$ y aplico nuevamente el algoritmo, queda determinado $U=X+N(x)$.

El algoritmo puede seguir tomando vértices de $X$ pero eventualmente va a tomar un vértice $y$ de $Y$ y así terminar etiquetando al vértice $z$. Luego sea $x$ el predecesor de $y$, el camino $a \to x \to y \to z$ va a quedar con flujo $1$. Futuras iteraciones del algoritmo no podrán añadir el vértice $x$ a $U$(intentar añadirlo como vecino de $a$ no es posible ya que se satura la única arista que conecta $a$ con $x$, intentar añadirlo como vecino de un vértice $y$ no es posible ya que intentarlo conlleva a etiquetar al vértice $z$ y por lo tanto no considerarlo para el paso 3). Análogamente se puede llegar a que el vértice $y$ tampoco puede ser elegido.

El algoritmo termina cuando ningún vértice de $X$ puede saturar a otro vértice de $Y$.

Las aristas saturadas por el flujo no comparten extremos ni en $X$ ni en $Y$. Por lo tanto forman un matching máximo.

Puesto que el flujo es un numero finito, cualquier corte $(S,T)$ solo puede contener aristas saturadas por el vértice(caso contrario la capacidad mínima es infinita).