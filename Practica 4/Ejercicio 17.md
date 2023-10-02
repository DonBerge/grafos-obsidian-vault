Pruebo por inducción en la cantidad de aristas del dígrafo

CB) $|E|=0$
Es el caso del grafo sin aristas.
$0=\sum_{v \in V(D)} d^+(v) = \sum_{v \in V(D)} d^-(v)=0$
HI) $\forall n \in \mathbb N$, el dígrafo $D$ con $n$ aristas cumple que $\sum_{v \in V(D)} d^+(v) = \sum_{v \in V(D)} d^-(v)$
PI)
Remover una arista cualquiera resulta en un dígrafo con $n$ aristas por lo que
$\sum_{v \in V(D\backslash e)} d^+(v) = \sum_{v \in V(D\backslash e)} d^-(v)$

Ahora al volver a añadir dicha arista, el grado de salida de un vértice aumenta en $1$ y el grado de entrada de otro vértice(no necesariamente uno distinto) también aumenta en $1$ por lo que:
$\sum_{v \in V(D\backslash e)} d^+(v) = \sum_{v \in V(D\backslash e)} d^-(v)$
$=$
$\sum_{v \in V(D\backslash e)} d^+(v)+1 = \sum_{v \in V(D\backslash e)} d^-(v)+1$
=
$\sum_{v \in V(D} d^+(v) = \sum_{v \in V(D)} d^-(v)$

$\blacksquare$
