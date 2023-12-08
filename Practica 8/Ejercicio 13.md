a)
	Sea $S$ un cubrimiento por vértices, dos vértices $u,v \notin S$ forman un estable.
	Por el contrario si $u$ y $v$ estuviesen conectados entonces la arista $uv$ tiene extremos que no están en el cubrimiento y por ende $S$ no es un cubrimiento de vértices. Esto implica que $\overline{S}$ es un conjunto estable.
	De la misma manera, si $S$ es un estable, $\overline{S}$ es un cubrimiento por vértices ya que si existiese una arista $uv$ donde $u \notin \overline{S} \land v \notin \overline{S} \implies u \in S \land v \in S \implies$ no existe una arista que los conecta(ya que pertenecen al estable), lo cual es absurdo.
b)
	Sea $S$ un estable donde $|S| = \alpha(G)$, $\beta(G) = |\overline S|$
	$S \cup \overline{S} = V(G)$
	$|S| + |\overline S| = |V(G)|$
	$\alpha(G) + \beta(G) = |V(G)|$

