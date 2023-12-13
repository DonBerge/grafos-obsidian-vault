Sean $n,a,b$ tres números enteros que cumplen:
$$2\sqrt{n} \leq a + b \leq n+1 \quad \land \quad n \leq ab \leq \frac{(n+1)^2}{4}$$
Existe un grafo $G$ tal que $\chi(G)=a$ y $\chi(G)=b$

Demostración: 
De la primera desigualdad surge:
$a+b-1 \leq n$
Y de la segunda surge:
$n \leq ab$

Construyo entonces el grafo $T$ donde los vértices se colocan en un rectángulo $a \times b$ tal que:
- La primera fila y columna están completas.
- Los siguientes $n-a-b+1$ vértices se colocan en las celdas restantes, siempre intentando llenar todas las filas posibles.
- Solo son adyacentes aquellos vértices que están en la misma columna.

El grafo $T$ es un grafo disconexo donde cada componente conexa es una clique. La clique máxima tiene tamaño $a$ por lo tanto $\chi(T)=a$.

Como las filas de $T$ son totalmente disconexas, en el complemento se formaran cliques en las filas, como hay una fila de largo $b$ se tiene que $b \leq \omega(\overline T)$ y dado que todo vértice del grafo esta conectado a al menos una fila no puede haber una clique de tamaño mayor a $b$, por lo tanto $b = \omega(\overline T) \leq \chi(\overline T)$.

Sea entonces la siguiente función de $V\to \{1,\dots,b\}$:
$f(v) = i \iff v \text{ pertenece a la i-esima columna del rectangulo}$ 

Este coloreo asigna un color a cada vértice según en que columna estén, como en el grafo $T$ todos los vértices de la misma columna están conectados, en el complemento no hay vértices adyacentes que estén en la misma columna. Por ende $f$ es un $b$-coloreo valido de $\overline T$ y resulta $\chi(\overline T)=b$

$T$ es por lo tanto un grafo que cumple que:
$$\chi(T) = a \quad \land \quad \chi(\overline T) = b$$
Y por lo tanto el teorema es valido.
$\blacksquare$