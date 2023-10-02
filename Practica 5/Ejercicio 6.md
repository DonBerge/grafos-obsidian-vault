Determinar si las siguientes familias de grafos admiten un ciclo o camino hamiltoniano. En el caso de que si, describa uno.
a) $K_n$
$K_1$ y $K_2$ admiten un camino hamiltoniano pero no son hamiltonianos.
Para $K_1$, el camino vacío es hamiltoniano.
Para $K_2$, el camino con la única arista $v_1v_2$ es hamiltoniano.
$K_n$ es hamiltoniano para todo $n\geq 3$
Dicho ciclo es el conjunto de aristas $\{v_{i}v_{i+1} : 1 \leq i \leq n-1\} \cup \{v_nv_1\}$

---

b) $K_{m,n}$
$K_{m,n}$ es hamiltoniano $\iff$ $m=n$ y $n\geq 2$

$\implies$)
Si $m \neq n$
Suponiendo que $K_{m,n}$ es hamiltoniano, entonces tiene un ciclo de $m+n$ vértices como subgrafo.
Para que haya un ciclo tiene que resultar que $m+n \geq 3$
Suponiendo sin perdida de generalidad que el primer vértice del ciclo pertenece al conjunto $X$ de la bipartición.

Los vértices impares tienen que pertenecer al conjunto $X$
Los vértices pares tienen que pertenecer al conjunto $Y$

La suma de $m$ y $n$ tiene que ser par.
Si $m>n$ o $n<m$ entonces necesariamente alguna arista va a unir vértices del mismo conjunto.

Por lo que no puede pasar que $m \neq n$. Absurdo.

Resulta $m=n$ y $n \geq 2$

$\impliedby$)
Por inducción en $n$
CB) $n=2$
$K_{2,2} \simeq C_4$ que es hamiltoniano.

HI) $K_{nn}$ es hamiltoniano $\forall n \geq 2$

PI)
Sean los conjuntos $X$ e $Y$ de la bipartición y $x \in X$ e $y \in Y$
El subgrafo inducido por los vértices $X-x \cup Y-y$ es isomorfo a $K_{nn}$
Existe un camino $v_1,v_2, \dots, v_{2n-1}, v_{2n}, v_1$
Suponiendo sin perdida de generalidad que $v_1 \in X$, $v_{2n} \in Y$
El ciclo hamiltoniano buscado es $v_1,v_2, \dots, v_{2n-1}, v_{2n}, x, y, v_1$
$K_{n+1,n+1}$ es hamiltoniano.

---
Para el caso del camino hamiltoniano, se tiene que $K_{mn}$ tiene un camino hamiltoniano $\iff$ $|m-n|=1$ o si bien $n=m=1$

Suponiendo sin perdida de generalidad que $n>m$

$K_{11} \simeq P_2$ que tiene un camino hamiltoniano

$K_{nn}$ es hamiltoniano$\iff n\geq 2 \land n=m$ 
Si se borra un vértice cualquiera de $K_{nn}$ se tiene un grafo isomorfo a $K_{n,n-1}$ con un camino hamiltoniano. Por lo que $K_{n,m}$ tiene un camino hamiltoniano $\iff$ $n=m-1$

---
El grafo $K_{mn}$ con $|m-n| \geq 2$ no tiene ni un ciclo ni un camino hamiltoniano

Si $K_{mn}$ tiene un ciclo hamiltoniano entonces tiene en particular un camino hamiltoniano(solo hay que borrar la ultima arista del camino).

Suponiendo que tiene un camino hamiltoniano, $v_1,v_2, \dots, v_{n+m}$

Suponiendo s.p.d.g que $n>m$ y $v_1 \in X$. Los vértices pares del camino pertenecen a $Y$ y los impares a $X$.

$m = \lfloor\frac{n+m}{2}\rfloor$
$n=\lceil\frac{n+m}{2}\rceil \geq m+2 = \lfloor \frac{n+m}{2} \rfloor + 2$
Y se tiene que:
$2 \leq \lceil\frac{n+m}{2}\rceil - \lfloor\frac{n+m}{2}\rfloor \leq 1$. Absurdo.

Luego el grafo no contiene un camino hamiltoniano. Por MT, el grafo tampoco puede tener un ciclo hamiltoniano.
