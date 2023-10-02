a) $K_n$
$K_n$ es un grafo regular donde los vértices son de grado $n-1$
$K_n$ admite un circuito euleriano $\iff$ $n-1$ es par $\iff$ $n$ es impar
b) $K_{mn}$
Sean dos vértices de las particiones $x \in X$ e $y \in Y$ con $|X| = m$ y $|Y| = n$
$d(x) = n$
$d(y) = m$
Para que $K_{mn}$ admita un circuito euleriano, $m$ y $n$ deben ser ambos pares.
c) $Q_n$
El $n$ cubo es un grafo regular de grado $n$
Para que $Q_n$ admita un circuito euleriano, $n$ tiene que ser par
d)
Pruebo por inducción que en el grafo $T_n$ todos los vértices son de grado par
CB) $n=1$
$T_1 \simeq K_3$ que es $2$-regular
HI) $\forall n \in \mathbb N: T_n$ es regular con vértices de grado par
PI)
$V(T_{n+1}) = \bigcup_{i=0}^{n+1}\{v_{ij} : 0 \leq j \leq i\} = \bigcup_{i=0}^n \{v_{ij} : 0 \leq j \leq i\} \sqcup \{v_{n+1,j} : 0 \leq j \leq n+1\}$
$=V(T_n) \sqcup \{v_{n+1,j} : 0 \leq j \leq n+1\}$
(La unión es disjunta ya que los vértices del primer conjunto difieren de los del segundo por una componente)

Entonces el grafo inducido por el conjunto de vértices de $V(T_n)$ es isomorfo al mismo grafo $T_n$(por el isomorfismo identidad).

Por hipótesis de inducción, dichos vértices tienen grado par.

Ahora hay que analizar el resultado de añadir las aristas que fueron removidas.

Se tiene para los vértices del conjunto $\{v_{n+1,j} : 0 \leq j \leq n+1\}$ que

Si $j=0$:
$v_{n+1,0}$ es adyacente a $v_{n,0}$ y a $v_{n+1,1}$
Si $0 < j < n+1$:
$v_{n+1,j}$ es adyacente a $v_{n,j}$, $v_{n+1,j+1}$, $v_{n+1,j}$ y a $v_{n,j+1}$
Si $j=n+1$:
$v_{n+1,n+1}$ es adyacente a $v_{n,n+1}$ y a $v_{n+1,n}$

Todos estos vértices tienen grados pares

Y para los vértices del conjunto $\{v_{n,j} : 0 \leq j \leq n\}$
$v_{n,j}$ es adyacente a $v_{n+1}{j+1}$ y a $v_{n+1,j}$

El grado de los vértices aumenta en $2$ y la adyacencia par se mantiene

$T_{n+1}$ tiene todos sus vértices de grado par.
$\square$

Por lo tanto $T_{n+1}$ tiene un circuito euleriano

$\blacksquare$

e) $G_{m,n}$ tiene un circuito euleriano $\iff$ ($n = 2$ $\land$ $m = 2$) $\lor$ ($n=1$ $\land$ $m=1$)
Si $n=1$ y $m=1$: es el caso del grafo trivial que si es euleriano
Si $n=1$ y $m=2$ o viceversa: es el caso  de un $P_2$ que no es euleriano:
Si $n=2$ y $m=2$: es el caso de un $C_4$ que si es euleriano:

Si $m\geq 3$ y $n=1$ o viceversa: es el caso de un $P_3$ que no es euleriano.

Si $m\geq 3$ y $n\geq 2$:
El vértice $v_{1,2}$ es adyacente a los vértices $v_{1,1}$, $v_{1,3}$ y $v_{2,2}$
$v_{1,2}$ tiene grado 3, $G_{m,n}$ no es euleriano.
Si $n \geq 3$ y $m \geq 2$:
El vértice $v_{2,1}$ es adyacente a los vértices $v_{1,1}$, $v_{3,1}$ y $v_{2,2}$
$v_{2,1}$ tiene grado 3, $G_{m,n}$ no es euleriano.