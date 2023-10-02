En un grafo simple $G[X,Y]$ bipartito con $n$ vértices y $m$ aristas donde $|X|=r$ y $|Y| = s$

a) $m \leq rs$
	Para cada vértice $x \in X$, su máximo grado posible es $s$
	Para cada vértice $y \in Y$, su máximo grado posible es $r$
	$2m = \sum_{x \in X} g(x) + \sum_{y \in Y} g(y) \leq rs + rs = 2rs$
	$m \leq rs$
b) $m \leq \frac {n^2} 2$
	$s = (n-r)$
	$rs = r(n-r) = -r^2+rn$
	¿Cuál es el valor de $r$ que maximiza $-r^2+rn$?
	Sea $f(x)=-x^2+nx$, $f$ es una función cuadrática con el termino cuadrado negativo. Alcanza su valor máximo en su vértice, es decir, el valor máximo es $r= \frac n 2$
	$m \leq rs = r(n-r) = \frac n 2 \cdot \frac n 2 = \frac {n^2} 4$
c) Describir los grafos donde $m = \frac{n^2} 2$
	Tiene que ocurrir que $\forall x \in X : g(x)=s$ y $\forall y \in Y : g(y) = r$
	Y además $|X|=\frac n 2$ y por consiguiente $|Y| = \frac n 2$
	Los grafos que cumplen la propiedad son por consiguiente los grafos bipartitos completos $K_{\frac n 2,\frac n 2}$
	El $n$ tiene que ser un numero par(sino $\frac {n^2} 4$ no es un numero entero)