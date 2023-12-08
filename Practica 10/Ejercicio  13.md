$K_5$ es un grafo arista-transitivo:
Sean los vértices $x,y,z,u,v$ y dos aristas $xy$ e $uv$ la función definida como:
$\theta:= \begin{pmatrix}x & y & z & u & v \\ u & v & z & x & y\end{pmatrix}$
Es un automorfismo del grafo que manda a la arista $xy$ a la arista $uv$.

Se puede ver que $\theta$ es invertible ya que es inversible(es su propia inversa):
$\theta(\theta(x))=\theta(u)=x$
$\theta(\theta(y))=\theta(v)=y$
$\theta(\theta(z))=\theta(z)=z$
$\theta(\theta(u))=\theta(x)=u$
$\theta(\theta(v))=\theta(y)=v$

Dado que todos los vértices de un $K_5$ están conectados, la función no rompe adyacencias. Sigue que $\theta$ es un automorfismo y $K_5$ es arista transitivo.

Luego dado el siguiente dibujo del $K_5$

![[Drawing 2023-12-06 16.05.43.excalidraw]]

Se puede ver que con borrar una arista el grafo resulta planar. Como el grafo es arista transitivo, con borrar cualquier arista se puede conseguir una inmersión plana del grafo. Subgrafos con menos aristas también resultan planares ya que todo subgrafo de un grafo planar es planar.

Como todo subgrafo propio de $K_5$ tiene que borrar al menos una arista del grafo original, todo subgrafo propio de $K_5$ es planar.