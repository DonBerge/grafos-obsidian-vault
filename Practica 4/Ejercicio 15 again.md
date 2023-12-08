El algoritmo no repite aristas, debido a que se toman del grafo $F$ y se borran del mismo a medida que se agarran, por lo tanto en toda iteración $W$ es un recorrido euleriano.

Suponiendo que el algoritmo termina en un vértice $y$, esto indica que todas las aristas de $y$ fueron procesadas por el algoritmo a partir de aquí distingo las aristas en 2 categorías.
- La arista $e$ se uso para "entrar" al vértice $y$, es decir, el algoritmo estaba en un vértice $x\neq y$ al momento de procesar la arista.
- La arista $e$ se uso para "salir" al vértice $y$, es decir, el algoritmo estaba en el vértice $y$ al momento de procesar la arista.
El algoritmo siempre alterna entre aristas de "salida" y aristas de "entrada"(siempre que las mismas no son lazos), como hay una cantidad par de aristas unidas al vértice $y$. Notar que el vértice final del algoritmo($y$ en este caso) termino con una arista usada para "entrar", esto solo es posible si la primera arista de $y$ fue usada para "salir" del mismo, es decir, $y$ fue el primer vértice del algoritmo y también el ultimo.

Esto indica que el recorrido $W$ es en realidad un circuito del grafo.

Queda probar que dicho circuito es un circuito de Euler.

Para eso voy a probar por inducción lo siguiente:
**En cada paso del algoritmo de Fleury que no es de terminación, el grafo $F$ posee una componente no trivial y el resto de componentes conexas son triviales**

Esto lo pruebo por inducción en la cantidad de pasos $i$.

CB) $i=0$
El inicio del algoritmo, como $F$ es conexo tiene una única componente conexa si $G$ no es un conjunto estable entonces el paso no es de terminación y se cumple la hipótesis.

PI)
Suponiendo que se esta en un estado de no terminación con un vértice $x$ se toma una arista $e$.
- La arista $e$ no es de corte, las componentes conexas no cambian, la hipótesis vale. Notar que el algoritmo siempre priorizara estas aristas.
- La arista $e=xy$ es de corte, en este caso voy a probar que el vértice $d(x)=1$, es decir, $x$ es la única arista de corte posible.

Si se llega al paso del ultimo ítem entonces todas las aristas del grafo son de corte.
- Si $d(x)=1$, entonces se produce una componente no trivial y otra trivial como mucho, el algoritmo se cumple.
- Si $d(x) > 2$