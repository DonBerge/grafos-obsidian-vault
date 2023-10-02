Probar el algoritmo de Fleury:
Sea $G$ un grafo conexo par


Elegir un vértice $u$ cualquiera
$W=\{\}$
$x = u$
$F = G$
$while(d_F(x) \geq 1)$:
	Seleccionar una arista $e=xv$ incidente en $x$ que no sea de corte de $F$
	Si todas las aristas son de corte entonces elegir cualquiera
	$W += xev$
	$x = v$
	$F = F \backslash e$
$W$ es un circuito euleriano en $G$

La idea, ir recorriendo el grafo siempre priorizando las aristas que no son de corte.

En ningún momento del algoritmo se repite una arista de $G$(esto debido a que las aristas se toman de $F$ y luego se eliminan del mismo). Por lo que en todo momento se tiene que $W$ es un recorrido.

El algoritmo termina cuando no hay mas aristas para extender el recorrido de Euler, por lo que dicho recorrido es maximal. 

En el algoritmo de Fleury, el primer y ultimo vértice del recorrido es el vértice $u$.
Si el algoritmo termina en un vértice $y$) Si se termino en el vértice $y$ se tiene que $d_F(y)=0$, si la primer arista recorrida por el algoritmo fue para acceder al vértice $y$ entonces tras recorrer una cantidad par de sus aristas se tiene que la ultima arista fue usada para salir del vértice $y$ lo cual indica que no se termino en el vértice $y$. Por absurdo se tuvo que utilizar la primera arista de $y$ para salir, por lo que $y=u$.

Esto indica que el algoritmo de Fleury produce un circuito en el grafo.

El circuito del algoritmo es un circuito de Euler)
En cada paso del algoritmo que no es de terminación(es decir $d_F(x)\geq 1$), el grafo $F$ es un grafo donde una componente conexa es no trivial y todas las demás son triviales.

Lo pruebo por inducción en la cantidad de pasos
CB) $i=0$
Se tiene que $F=G$, que por hipótesis es conexo y cumple la hipótesis.
HI) En el $i$-esimo paso del algoritmo de Fleury se tiene que $F$ tiene una componente conexa no trivial y todas las demás son triviales.
PI)
$d_F(x)\geq 1 \implies$ $x$ pertenece a la componente no trivial. 

En cada paso hay $2$ posibilidades
La arista $e$ es una arista que no es de corte) Remover la arista $e$ del grafo $F$ no aumenta la cantidad de componentes conexas. Por lo que se cumple la hipótesis.
La arista $e$ es una arista de corte) Si esto ocurre entonces $d(x) = 1$, es decir, hay una única arista de corte.

Eliminar esta arista del grafo puede producir una componente no trivial y otra trivial. Aquí $d_F(x) \geq 1$ y el algoritmo continua. Se cumple la hipótesis.

En caso contrario produce dos componentes triviales y el algoritmo termina. La hipótesis se sigue cumpliendo ya que se llego al paso de terminación($d_F(x) = 0$)

Pruebo que $d(x) = 1$ en este caso por reducción al absurdo.

Suponiendo que $d(x) \geq 2$, existe en particular otra arista $e'$ que es de corte en el grafo en el grafo $F$.

Lema: Si un grafo $H$ tiene una arista de corte $e$ entonces las componentes conexas $X$ e $Y$ del grafo $H \backslash e$ tienen al menos un vértice de grado impar cada una.
	Pruebo el lema para $X$, la prueba para $Y$ es análoga.
	Si $X$ tiene todos sus vértices de grado par entonces el extremo de $e$ que pertenece a la componente $X$ tiene grado impar.
	Si $X$ tiene al menos un vértice de grado impar entonces necesariamente tiene que tener otro vértice de grado impar(sino $\sum_{v \in V(X)} d(v) \neq 2|E(X)|$). Dado que la arista $e$ solo puede aumentar el grado de un vértice de $X$ en 1. Se cumple el lema.

Suponiendo sin perdida de generalidad que el algoritmo toma la arista $e$, como dicha arista es de corte. El algoritmo no va a poder regresar al vértice $x$. Por lo que la arista $e'$ no va a poder ser elegida por el algoritmo.

Una vez que el algoritmo termine, va a quedar una componente conexa no trivial con aristas no elegidas. Sea $Y$ dicha componente, por el lema anterior, dicha componente tiene un vertice de grado impar.

Ahora si al grafo $F$ se le suman todas las aristas de $W$ el resultado es el grafo $G$. Como las aristas
de $W$ afectan a la paridad del grado de los vértices de $Y$. Esto quiere decir que el grafo $G$ tiene al menos un vértice de grado impar. Lo cual es falso por hipótesis.

Este absurdo proviene de que $d(x) \geq 2$
Por lo tanto $d(x) = 1$, la hipótesis se cumple

$\square$

Esto indica que al terminar el algoritmo se tiene que el grafo $F$ solo esta formada por grafos triviales y el conjunto $W$ es un circuito que tiene todas las aristas del grafo $G$. $W$ es un circuito euleriano.

$\blacksquare$