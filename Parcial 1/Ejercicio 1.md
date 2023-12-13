Probar que $G_n$ es conexo pra $n \geq 5$

Por inducción:
$CB$) Isomorfo a Petersen, que es conexo

$PI$) $G_{n+1}$ tiene a $G_n$ como subgrafo inducido que por lo tanto es conexo.
$V(G_{n+1}) - V(G_n) = \{\{n,i\} : 1 \leq i \leq n-1\}$

Todo vértice de este conjunto esta conectado a un vértice de $V(G_n)$, efectivamente, $\{a,n\}$ esta conectado a $\{1,2\}$ si $a > 2$ o a $\{3,4\}$ si $a\leq 1$.

Resulta $G_n$ conexo.

$diam(G_n)=3$
Sean dos vértices $\{u,v\}$ y $\{x,y\}$ del grafo:
$|\{u,v\} \cap \{x,y\}| = 0 \implies dist(\{u,v\},\{x,y\})=1$
$\{u,v\} \cap \{x,y\} = v \implies$ asumiendo $x=v$, existe el camino $\{u,v\} \to \{w,w'\} \to \{x,y\}$ donde $w$ y $w'$ son dos números naturales distintos no pertenecientes a $\{u,v,y\}$(que existen, dado que $n\geq 5$). 
Si la intersección tiene cardinal $2$ entonces es el mismo vertice, que tiene distancia $0$.

Por lo tanto el diametro es $2$

Para que sea euleriano, tiene que pasar que $\binom {n-2} 2$ sea par. $\binom {n-2} 2 = \frac{(n-2)!}{2(n-4)!} = \frac{(n-2)(n-3)}{2}$. $n=4$ no cumple ya que no es conexo, $n=5$ no cumple la paridad. $n=6$ cumple ambas condiciones, el menor valor de $n$ es $6$.