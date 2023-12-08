Un grafo $G=(V,E)$ se representa como dos conjuntos $V$ y $E$ donde $E \subseteq V^2$, es decir, $E$ se forma usando pares de elementos de $V$. El conjunto $V(G)$ se conoce como vértices del grafo y el conjunto $E(G)$ se conoce como aristas del grafo.

Se dice que si una arista $e=(u,v)$ con $u,v \in V$ entonces la arista $e$ une los vértices $u$ y $v$.
# Grafos especiales

## Grafo vacio
El grafo $(\varnothing, \varnothing)$ es el grafo vacío.

## Grafo trivial
El grafo que tiene un solo vértice y ninguna arista es el grafo trivial.

Es decir, $|V(G)| = 1$ y $E = \varnothing$

## Grafos simples

Una arista puede representarse también como un par de elementos de $V$, donde los vértices son aquellos elementos unidos por la arista.

Una arista que une un vértice consigo mismo es un lazo o bucle.

Si hay mas de una arista en el grafo que une el mismo par de vértice, se dice que es una multiaristas o arista paralela.

Aquellos grafos que no tienen ni aristas paralelas ni lazos son los llamados grafos simples.

En los grafos simples, una arista queda unívocamente determinada por los pares de vértices que los unen.

## Grafos completos
Se dice que un grafo simple es completo $\iff$ no se le pueden añadir mas aristas.
Es decir, su conjunto de aristas es $E = \{(u,v) : u,v \in V \}$

Un grafo completo de $n$ vértices se representa como el grafo $K_n$

## Caminos
Un camino de $n$ vértices se representa como $P_n$ donde
$$V(P_n)=\{x_i : 1 \leq i \leq n\} \hspace{2cm} E(P_n)=\{(x_i, x_{i+1}) : 1 \leq i < n \}$$
## Ciclos
Un ciclo de $n$ vértices se presenta como $C_n$ donde
$$V(C_n)=\{x_i : 1 \leq i \leq n\} \hspace{2cm} E(C_n)=\{(x_i, x_{i+1}) : 1 \leq i < n \} \cup \{(v_n,v_1)\}$$
## Grafos bipartitos
Un grafo $G$ es bipartito $\iff$ su conjunto de vértices puede particionarse en $2$ conjuntos $X$ e $Y$ de manera que $\forall e \in E(G)$, $e$ une un vértice de $X$ con un vértice de $Y$.

Explicación alternativa, un grafo es bipartito si sus vértices pueden pintarse de rojo y azul de manera que no haya ninguna arista que una vértices con el mismo color.

Aquel grafo simple bipartito al cual no se le pueden añadir mas aristas sin que deje de ser bipartito se dice que es bipartito completo y se denota $K_{n,m}$ donde $n$ y $m$ son los cardinales de las particiones.

## Hipercubo
Un hipercubo o $n-$cubo se define como aquel grafo donde el conjunto de vértices son las $n$-uplas $(a_1,\dots,a_n)$ con $a_i \in \{0,1\}$ para todo $i$ y dos $n-$uplas son adyacentes $\iff$ difieren en exactamente una componente. 

## Grafo rueda
Para $n \geq 3$ se define el grafo rueda de $n$ radios formado por un ciclo de $n$ vértices y un vértice adicional unido a todos los vértices del ciclo. 
$V(G) = \{v_1,\dots,v_{n+1}\}$
$E=\{(v_i,v_{i+1} : 1 \leq i < n\} \cup \{(v_n,v_1)\} \cup \{(v_i,v_{n+1}) : 1 \leq i \leq n\}$

### Grafo garra o claw
Es el grafo denotado por
$V(G) = \{v_1,v_2,v_3,v_4\}$
$E(G) = \{(v_1,v_2),(v_1,v_3),(v1,v_4)\}$