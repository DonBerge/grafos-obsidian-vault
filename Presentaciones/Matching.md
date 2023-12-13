## Problema de introducción
---


## Que es un matching?
---
Dado un grafo $G=(V,E)$, un matching $M$ es un subconjunto de $E(G)$ tales que dos aristas cualesquiera de $M$ no comparten extremo. Un vértice que es extremo de una arista de $M$ se dice que es un vértice saturado por $M$ o $M$-saturado.

*Inserte dibujito de un matching*

Un subconjunto de un matching es también un matching, pero puede ocurrir que un matching $M$ no sea subconjunto de otro matching. Si esto ocurre, decimos que $M$ es un matching maximal.

Se dice que un matching $M$ es perfecto cuando todos los vértices de $G$ están saturados por $M$.

A partir de esta información se puede sacar el siguiente resultado:
<u>Teorema:</u> Sea $n = |V(G)|$, un matching $M$ tiene un tamaño de como maximo $\left\lfloor\frac n 2\right\rfloor$ aristas.
<u>Demostración:</u>
	Si hay un matching de tamaño mayor, entonces este matching tiene como subconjunto a otro matching de tamaño al menos $\left\lfloor\frac n 2\right\rfloor+1$ el cual satura exactamente $2\left\lfloor\frac n 2\right\rfloor + 2$ vértices.
	\ 
	Luego si $n$ es par $\left\lfloor\frac n 2\right\rfloor = \frac n 2$. Se saturan $n+2$ vértices, es decir, hay mas vértices saturados que vértices del grafo, absurdo.
	\ 
	Si $n$ es impar $\left\lfloor\frac n 2\right\rfloor = \frac{n-1} 2$ y se saturan en total $n+1$ vértices, nuevamente hay mas vértices saturados que vértices del grafo, absurdo.
	\ 
	El absurdo viene de suponer que hay un matching de tamaño mayor a $\left\lfloor\frac n 2\right\rfloor$, por lo tanto $|M| \leq \left\lfloor\frac n 2\right\rfloor$.

## Caminos M-aumentantes  y Teorema de Berge
Dado un matching $M$ se definen:

<u>Camino M-alternante:</u> Es un camino en $G$ que alterna aristas de $M$ y $E(G-M)$.
<u>Camino M-aumentante:</u> Un camino $M$-alternante cuyos extremos son distintos y no están $M$-saturados.

Observación: Si se tiene un camino $M$-aumentante, las aristas de $P-M$ forman un matching de tamaño mayor a $M$, mas específicamente, $|P-M| = |M|+1$.

**Explicar con dibujito**

De aquí se puede enunciar el Teorema de Berge
<u>Teorema de Berge:</u> Un matching $M$ de $G$ es maximo $\iff$ No hay caminos $M$-aumentantes en $G$
$\implies$) Observación anterior, si $M$ fuese un matching máximo y existiese un camino $M$-aumentante entonces existe un matching mas grande de $M$. Absurdo.
$\impliedby$)
	Primero pruebo dos lemas intermedios:
	Lema 1: Si $\Delta(G)\leq 2$ toda componente conexa de $G$ es un ciclo o un camino.
		Para cada componente conexa, sea $P = x_1 \to x_2 \to \dots \to x_k$ un camino maximal, todos los vértices internos ya tienen grado $2$ así que no salen mas aristas de dichos vértices, de $x_1$ y $x_k$ no pueden salir aristas a cualquier otro vértices puesto que sino $P$ no seria maximal, así que $\{x_1,x_2,\dots,x_k\}$ son todos los vértices de la componente. El grafo inducido por estos vértices puede tener como mucho una arista adicional, la correspondiente a $x_1x_k$, luego dicha componente es un camino o un ciclo.
	Lema 2: Sean $M'$ y $M$ dos matchings, se tiene que toda componente conexa de $M' \Delta M$ es un camino o un ciclo par.)
		Si existiese un vértice $v$ de grado mayor a $2$ entonces inciden al menos $3$ aristas en dicho vertice, es decir, hay al menos $2$ aristas de $M$ o $M'$ que tienen a $v$ como extremo, lo cual es absurdo ya que contradice la definición de matching. Esto implica que $\Delta(G) \leq 2$ y cada componente conexa es un camino o un ciclo. Por un argumento similar se puede llegar a que en cada vértice inciden como mucho $2$ aristas, una arista de $M$ y una $M'$. Luego se tiene lo siguiente:
		\ 
		Si la componente es un camino $u_1 \to u_2 \to \dots \to u_k$: Asumir S.P.D.G que $u_1u_2 \in M$, luego por lo visto anteriormente, $u_2u_3 \in M'$ y $u_3u_4 \in M$ y así sucesivamente.
		\ 	
		Si la componente es un ciclo $u_1 \to u_2 \to \dots \to u_k \to u_1$: Por la razón anterior dicho ciclo alterna entre aristas de $M$ y $M'$, Si $u_1u_2 \in M$ entonces la arista $u_ku_1$ no puede ser una arista de $M$($M$ no seria un matching). Luego se tiene que este ciclo es un ciclo par.
	\ 
	Suponiendo que $G$ no tiene un camino $M$-aumentante y existe un matching $M'$ donde $|M'| > |M|$, probemos que existe un camino $M$-aumentante.
	\ 
	Sea $F = M' \Delta M$, cada componente conexa es un ciclo par o un camino por el lema anterior. Como $|M'| > |M|$ una de estas componentes debe ser un camino que alterna aristas entre matchings. Los extremos de este camino estan saturados por $M'$ y por lo tanto existe un camino $M$-aumentante. Absurdo
	$\square$

El teorema de Berge provee una forma de encontrar un matching perfecto en el grafo a base de encontrar caminos aumentantes.

Estudiemos ahora el caso de los matchings para grafos bipartitos.


(en este teorema tengo dudas)
Teorema de Hall: Un grafo bipartito $G[X, Y]$ tiene un matching que satura $X$ $\iff$ $\forall S\subseteq X : |N(S)| \geq |S|$
$\implies$) Sea el matching $M$ que satura a $X$, cada vértice $x_i$ de $S$ se corresponde con una única arista $e_i$ de $M$ que lo tiene como extremo, esto implica que para cada arista $e_i$ el otro extremo $y_i$ pertenece a $N(S)$ se tiene que $|N(S)| \geq |S|$, el mayor viene que los vértices $x_i$ pueden conectarse con otros vértices de $Y$ que no son alcanzados por las aristas $e_i$.
$\impliedby$) Consideremos la contrarrecíproca, $\text{no hay un matching que sature a } X \implies \exists S \subseteq X : |N(S)| < |S|$
Sea $M$ un matching máximo y $u \in X$ no saturado, considerando todos los caminos $M$-alternantes(no $M$-aumentantes porque no existen puesto que $M$ es máximo). Sea $S \subseteq X$ los vértices de $X$ que aparecen en alguno de estos caminos y $T \subseteq Y$ los vértices de $Y$ que aparecen en algunos de estos caminos.

Se tiene que $T \subseteq N(S)$

Veamos que $T=N(S)$

Todos los vecinos de $u$ están saturados(sino el matching podría extenderse y este no seria máximo). Por lo tanto $N(u) \subseteq T$. Luego sea $y \in N(S)-T$, se tiene que $y$ no esta saturado(sino $y \in T$) y por un argumento igual al anterior se tiene que $y$ es vecino de algun vertice saturado $s\in S-\{u\}$ y por lo tanto $sy$ es una arista de $G$ y $sy \notin M$.

Por ende existe un camino $M$-alternante de $u$ a $s$, sumado a la arista $sy$, se tiene un camino $M$-aumentante, $M$ no es máximo. El supuesto vértice $y$ no existe y resulta $T=N(S)$.
Se tiene que: $|T|=|S-\{u\}|$
$|N(S)| = T = |S-\{u\}| = |S|-1 < |S|$

<u>Corolario:</u> Todo grafo $k$-regular tiene un matching perfecto:
	$|E| = \sum_{v \in X} d(v) = \sum_{v \in Y} d(v)$
	$|E| = k|X| = k |Y|$
	$|X| = |Y|$
	En consecuencia un matching que satura $X$ es un matching perfecto.
	\ 
	Sea $S \subseteq X$, las aristas incidentes en $S$ son $E(S) = k|S|$ y la cantidad de aristas incidentes en $N(S)$ son al menos las aristas incidentes en $S$, es decirs $|E(N(S))| = k|N(S)| \geq k|S|$ y en consecuencia $|N(S)|\geq |S|$. Como se verifica la condición de Hall, existe un matching que satura $X$ y en particular un matching perfecto.

## Cubrimientos de vértices
Definición: Un cubrimiento de aristas por vértices es un un conjunto $F \subseteq V(G)$ tal que toda arista de $G$ tiene como extremo a al menos un vértice de $F$. El tamaño mínimo de un cubrimiento de $G$ se denota como $\beta(G)$.

Sea $\alpha'(G)$ el tamaño máximo de un matching de $G$ notar que por cada arista del matching tiene que haber un vértice en un cubrimiento mínimo de $G$. De aquí sale que $\alpha'(G) \leq \beta(G)$.

<u>Teorema de Konig</u>: Si un grafo es bipartito entonces $\alpha'(G)=\beta(G)$
	Sea $F$ un cubrimiento por vértices mínimo de $G[X,Y]$ construyo un matching tal que $|F|=|M|$ lo que implica la tesis.
	\ 
	Sea $R=F \cap X$ y $T = F \cap Y$, sea $H \ sgi \ R \cup (Y-T)$ y $H'\ sgi \ T \cup (X-R)$(es decir, $H$ esta formado por los vértices de $X$ que están en el cubrimiento y los vértices de $Y$ que no están en el cubrimiento. $H'$ se construye igual solo que cambian los roles de $X$ e $Y$). No hay aristas entre $Y-T$ y $X-R$(sino $F$ no seria cubrimiento). Sea $S \subseteq R$, si $|N_H(S)| < |S|$, $T \cup N_H(S)$ (???) es un cubrimiento de $G$, esto pasa porque las aristas cubiertas por $S$ son cubiertas por $N_H(S)$ y las demás aristas son cubiertas por $T$, pero $|T \cup N_H(S)| = |T| + |N_H(S)| < |T| + |S| <= |T| + |R| = \beta(G)$
	Lo que es absurdo, luego se verifica la condición de Hall para $R$ en $H$.
	\ 
	Se tiene entonces que existe un matching $M_H$ de tamaño $|R|$. Análogamente se puede conseguir un matching $M_{H'}$ de tamaño $|T|$. Ambos grafos son disjuntos por lo que $M=M_H \cup M_{H'}$ es un matching de $G$ de tamaño exactamente $\beta(G)$.

## Relación de los cubrimientos con los conjuntos estables
El complemento de un estable es un cubrimiento y viceversa.
$S$ estable y $F$ cubrimiento
$\overline S$ es un cubrimiento)
	Por el contrario, si $\overline S$ no fuese un cubrimiento existe una arista $uv$ donde $u \notin \overline S \land v \notin \overline S \implies u \in S \land v \in S$ y como $S$ es un estable no existe una arista $uv$ que los conecte, lo que se contradice con la oración anterior.
$\overline F$ es un estable)
	Por el contrario, si $\overline F$ no fuese un estable existe una arista $uv$ donde
	$u \in \overline F \land v \in \overline F \implies u \notin F \land v \notin F$
	Y entonces hay una arista $uv$ que no es cubierta por $F$. Absurdo.

Corolario: $\alpha(G)+\beta(G)=|V(G)|$