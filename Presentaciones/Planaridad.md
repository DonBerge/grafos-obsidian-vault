## Problema de introducción
---
<u>Problema del suministro de servicios:</u> Se desea suministrar a 3 casas de agua, luz y electricidad. Para ello, se proveen 3 fuentes de cada servicio que deben conectarse a las casas mediante caños/cables, ¿es posible hacerlo de manera que no haya ningún Cruze entre caños/cables?.

## Formalización, grafos planares
---
El problema puede formalizarse como sigue, se pone un vértice por cada fuente de servicio y a su vez un vértice por cada casa, luego se conecta cada fuente con cada casa mediante una arista, el grafo resultante es un $K_{3,3}$

Un grafo $G$ que puede dibujarse en el plano de manera que ninguna arista se cruce con otra se dice que es planar, resolver el problema del suministro equivale a responder si $K_{3,3}$ es planar.

El grafo $K_4$ por ejemplo es un grafo planar, **inserte dibujito**

Vemos que el grafo divide el plano en varias regiones, algunas de estas regiones están encerradas por aristas mientras que otras no lo están. A estas regiones delimitadas por las aristas del grafo las llamamos *caras* del grafo.

Observación: Si $G$ es un grafo no simple, entonces es planar sii el subgrafo $G'$ formado al eliminar las multiaristas y los bucles de $G$ es simple.

<u>Grafo dual</u>: Llamamos $G^*$ al grafo dual de un grafo plano $G$, donde cada vértice de $G^*$ es una cara de $G$ y además por cada arista $e \in G$ que esta en la frontera de las caras $X,Y$ se añade una nueva arista $e' \in G^*$ que une los vertices de las caras $X,Y$

**Dibujar grafos duales de dos inmersiones planas de $K_4$ y ver que no son iguales**

Si se tiene que el grafo es conexo, entonces toda cara esta delimitada por un camino cerrado, lo que nos lleva a la siguiente definición:
<u>Definición:</u> Sea $G$ un grafo y $F$ una cara de $G$, se define $long(F)$ como la longitud del camino cerrado mas corto que contiene a todas las aristas de la frontera de $F$.

Observación: $long(F) = d_{G^*}(F)$

Corolario: Si $G$ tiene $f$ caras $F_1,\dots,F_f$ entonces $\sum_{i=1}^f long(F_i) = 2|E(G)|$
	Dado que $|E(G^*)|=|E(G)|$ se tiene que:
	$$\sum_{i=1}^f long(F_i)=\sum_{i=1}^f d_G^*(F_i)=2|E(G^*)|=2|E(G)|$$

## Formula de Euler
Para todo grafo plano y conexo con $v$ vertices, $a$ aristas y $c$ caras vale la siguiente formula:
$$v-a+c=2$$
Demuestro por inducción en la cantidad de vértices:
CB) $v=1$
No hay aristas y la única cara es la cara exterior: $v-a+c = 1-0+1 = 2$, vale la formula.
HI) La formula de Euler vale para todo grafo con a lo sumo $v$ vértices.
PI) Sea un grafo plano y conexo con $n+1$ vértices, $m$ aristas y $c$ caras. Puesto que hay al menos dos vértices y el grafo es conexo, hay una arista $uv$ que no es un bucle. Si se contrae dicha arista, es decir, se borran los vértices $u$ y $v$, se añaden un vértice $w$ y se conectan los vértices $N(u) \cup N(v)$ con $w$. Se tiene que el grafo luego de contraer la arista tiene $n'=(n+1)-1$ vértices, $m'=m-1$ y $f=f'$ luego de aplicar la contracción por HI se tiene que:
$$n'-m'+f'=2$$
Y reemplazando:
$$2=(n+1)-1-(m-1)+f=(n+1)-m+f$$
Y la formula de Euler vale.

Corolario: Si $G$ es un grafo planar conexo con $n$ vértices y $m$ aristas con al menos un ciclo de largo $k\geq 3$ y la longitud de cada ciclo es al menos $k$ se tiene que:
$$m \leq \frac k {k-2} (n-2)$$
	Suponiendo que $G$ es conexo,
	Vimos antes que $2m = \sum_{F \in \text{caras de G}} long(F)$ y como cada ciclo tiene largo al menos $k$ se tiene que $long(F) \geq k$, luego
	$2m \geq kf$ y $f \leq 2/k \cdot m$, luego por la formula de Euler:
	\ 
	$2=n-m+f \leq n - m + 2/k \cdot m = n - (k-2)/k \cdot m$
	Y trabajando algebraicamente se tiene que:
	$m \leq (n-2) \cdot k/(k-2)$
	\ 
	En el caso de que $G$ no sea conexo se pueden añadir sucesivas aristas a $G$ hasta formar un grafo conexo $G'$, luego:
	$|E(G)| < |E(G')| \leq (|V(G')|-2) \cdot k/(k-2) \leq (|V(G)|-2) \cdot k/(k-2)$
	Dato curioso, la formula tiene números enteros solo cuando $k=3$ o $k=4$

Corolario: Todo grafo planar tiene un vértice de grado al menos $5$:
	Si esto no fuese así todos los vértices tienen grado $6$ o mas, sigue que hay al menos $3$ vértices entonces $|E(G)| = \sum_{v \in V(G)} d(v)/2 \geq 6/2 \cdot |V(G)| = 3|V(G)|$
	Y el corolario anterior no se cumple, absurdo.

Usando la formula anterior se puede llegar a que si $K_5$ fuese planar:
Los ciclos de $K_5$ tienen largo al menos $3$, por lo tanto $k=3$
$|E(K_5)| = 10 \leq 3|V(K_5)|-6 = 15-6 = 9$, ABS!
Y por lo tanto $K_5$ no es planar.

Y si $K_{3,3}$ fuese planar:
$K_{3,3}$ es bipartito, puede tener ciclos de longitud al menos $4$, tomando $k=4$
$|E(K_{3,3})| = 9 \leq 2|V(K_{3,3})|-4 = 2\cdot 6 - 4 = 8$

Y por lo tanto $K_{3,3}$ no es planar. Esto nos dice que el problema del suministro no tiene solución.

## Caracterización de grafos planares
---
Todo subgrafo $H$ de un grafo planar $G$ es planar, eso se consigue dibujando una inmersión plana de $G$ y borrando vértices y aristas hasta llegar hasta $H$.

Un grafo $H$ se consigue a partir subdivisión de una arista $e=uv$ de $G$ si $H$ se obtiene borrando la arista $e$, agregando un vértice $w$ y agregando dos aristas $uw$ y $wv$.

Definición: Un grafo $G_1$ es homeomorfo a un grafo $G_2$ sii ambos se consiguen a partir de un mismo grafo $G$ aplicando sucesivas subdivisiones de aristas.

Notar que el hecho de aplicar subdivisiones de aristas no afecta a la planaridad del grafo $G$, por lo tanto se tiene el siguiente resultado: Un grafo $G$ es planar $\iff$ todo grafo homeomorfo a $G$ es planar.

Esto junto al hecho de que $K_5$ y $K_{3,3}$ son grafos no planares minimales, conlleva al teorema de Kuratowski.
$G$ es planar $\iff$ no contiene ningún subgrafo homeomorfo a $K_5$ o $K_{3,3}$.