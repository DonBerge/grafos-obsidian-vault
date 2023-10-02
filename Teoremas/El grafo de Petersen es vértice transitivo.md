El grafo de Petersen es isomorfo al grafo de Knesser $K(5,2)$

Es decir, cada vértice puede etiquetarse con un subconjunto de ${1,2,3,4,5}$ con 2 elementos y donde dos vértices son adyacentes si su intersección es vacía.

Dados dos vértices $\{x,y\}$ $\{u,v\}$ con $\{x,y\} \neq \{u,v\}$, ¿existe un auto morfismo $f$ tal que $f(\{x,y\}) = \{u,v\}$?

Sea la función $g: \{x,u,y,v,z\} \to \{x,u,y,v,z\}$ donde $\{x,u,y,v,z\} = \{1,2,3,4,5\}$ y $g$ esta definida como:
$g := \begin{pmatrix} x & y & u & v & z \\ u & v & x & y & z\end{pmatrix}$

Y la función $f$ definida de $V$ a $V$ como: $f(\{a,b\}) = \{g(a),g(b)\}$

$g$ es biyectiva porque es invertible y su propia inversa es g:
$g(g(x)) = g(u) = x$
$g(g(y)) = g(v) = y$
$g(g(u)) = g(x) = u$
$g(g(v)) = g(y) = v$
$g(g(z)) = g(z) = z$

$f$ es biyectiva porque es invertible y su propia inversa es la misma f:
$f(f(\{a,b\})) = f(\{g(a),g(b)\} = \{g(g(a)),g(g(b))\} = \{a,b\}$

Sean los vértices adyacentes $\{a,b\}$ y $\{c,d\}$

$\{a,b\}$ y $\{c,d\}$ son adyacentes
$\implies$
$\{a,b\} \cap \{c,d\} = \varnothing$
$\implies$
$a \neq c \land a \neq d \land b \neq c \land b \neq d$
$\implies$(definición función inyectiva)
$g(a) \neq g(c) \land g(a) \neq g(d) \land g(b) \neq g(c) \land g(b) \neq g(d)$
$\implies$
$\{g(a),g(b)\} \cap \{g(c),g(d)\} = \varnothing$
$\implies$
$f(\{a,b\}) \cap f(\{c,d\}) = \varnothing$
$\implies$
$f(\{a,b\})$ y $f(\{c,d\})$ son adyacentes

$f$ es un automorfismo del grafo de Petersen que cumple que $f(\{x,y\}) = \{g(x),g(y)\} = \{u,v\}$.

El grafo de Petersen es vértice transitivo
