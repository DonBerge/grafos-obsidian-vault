Sea $G$ un grafo con $n:=|V(G)|$, $m:=|E(G)|$ 
1. $\omega(G) \leq \chi(G) \leq n$
	Como las cliques están totalmente conectadas, necesitan tantos colores como vértices tienen para poder colorearse. Luego resulta $\chi(G) \geq \omega(G)$. Además se puede colorear el grafo asignando un vértice a cada color, por lo que $n \geq \chi(G)$ y por transitividad resulta la cota.
2. $\chi(G)\alpha(G) \geq n$
	$n = \sum_{\text{clases de color }C_i} |C_i| \leq \sum_{\text{clases de color }C_i} \alpha(G) = \chi(G)\alpha(G)$
	La desigualdad surge de que todas las clases de color son conjuntos estables de cardinal menor o igual al máximo conjunto estable del grafo.
3. $\chi(G)\chi(\overline G) \geq n$
	Esta es una combinación de las cotas $1$ y $2$
	$n \leq \chi(G)\alpha(G) = \chi(G)\omega(\overline G) \leq \chi(G) \chi(\overline G)$.
4. $\chi(G)(n-\delta(G)) \geq n$
	Sea  $I$ un estable máximo y $v \in I$, $I \subseteq V - N(v)$(los vecinos de $v$ no pueden pertenecer al estable), en consecuencia, $\alpha(G) \leq |I| \leq |V-N(v)| = n - d(v) \leq n - \delta(G)$.
5. $\chi(G) \leq n+1 - \alpha(G)$
	Sea $I$ un estable máximo del grafo, es posible crear un coloreo de $G$ asignándole un color a cada vértice de $I$ y colores distintos a todos los demás vértices que no están en $I$, este es un coloreo que usa $n-\alpha(G) + 1$ colores y en consecuencia $\chi(G) \leq n + 1 - \alpha(G)$.
6. $\chi(G) \leq 1/2 + \sqrt{2m + 1/4}$
	Para cada vértice de cada color en un $\chi(G)$-coloreo tiene que haber una arista que conecte dicho vértice con al menos un vértice de otro color, si esto no es así entonces existiría un $(\chi(G)-1)$-coloreo lo cual es imposible. Puede haber mas de una arista que conecte vértices de distinto color, por lo tanto $m \geq \binom{\chi(G)} 2$.
	
	Luego:
	$m \geq \binom{\chi(G)} 2 = \chi(G)(\chi(G)-1)/2$
	$2m \geq \chi(G)^2 - \chi(G)$
	$2m + 1/4 \geq \chi(G)^2 - \chi(G) + 1/4$
	$2m + 1/4 \geq (\chi(G) - 1/2)^2$
	$\sqrt{2m + 1/4} + 1/2 \geq \chi(G)$
7. 