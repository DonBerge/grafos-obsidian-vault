Teorema: $G$ es perfecto $\iff$ $\forall H \text{ subgrafo inducido de } G : |V(H)| \leq \alpha(H) \cdot \omega(H)$
Demostración:
Para cualquier subgrafo inducido $H$ de $G$ sus vértices pueden particionarse en $\chi(H)$ clases de color con colores $1,2,\dots,\chi(H)$.
Luego se tiene que $|V(H)| = \sum_{i=1}^{\chi(H)}|[i]| \overset{\text{los vertices de la clase de color forman un estable}}{\leq} \sum_{i=1}^{\chi(H)} \alpha(H) \leq \chi(H) \cdot \alpha(H)$
Luego si $G$ es perfecto se tiene que $\chi(H) = \omega(H)$ y la desigualdad se cumple, esto prueba la ida
$\impliedby$) 
Si la vuelta fuese falsa entonces debería existir un contraejemplo de dicha proposición.

Suponiendo que existe dicho contraejemplo $G$, $G$ es un grafo que cumple:
- La proposición $\forall H \text{ subgrafo inducido de } G : |V(H)| \leq \alpha(H) \cdot \omega(H)$, es verdadera.
- $G$ no es perfecto.

S.P.D.G, voy a asumir además que $G$ es el contraejemplo con la menor cantidad de vértices.

Esto implica que cualquier grafo con menos vértices que $G$ cumple con el teorema.

Sea $n:=|V(G)|$,
Defino los siguientes términos por simplicidad, $\omega:=\omega(G)$, $\alpha(G):=\alpha$, $V:=V(G)=\{v_1,\dots,v_n\}$

Voy a probar 3 lemas:

**Lema 1:** $\forall U \subset V(G) : \chi(G-U) = \omega(G-U)$ y $\chi(G) > \omega(G)$
**Demostración**:
Cualquier subgrafo inducido propio de $G$ tiene menos de $n$ vértices, por lo que todo subgrafo inducido propio de $G$ es perfecto. Esto prueba la primera proposición.
Si no se cumpliese que $\chi(G) > \omega(G)$ entonces $\chi(G) \leq \omega(G)$ y sigue que $\chi(G) = \omega(G)$ y $G$ es perfecto. ABS!. La segunda proposición también es valida.

**Lema 2:** Existen $S_0,S_2,\dots,S_{\alpha\omega}$ conjuntos estables en $G$ tal que todo vértice $v \in V$ esta contenido en exactamente $\alpha$ de estos conjuntos.
**Demostración**:
Defino al conjunto $S_0:=\{u_1,u_2,\dots,u_\alpha\}$ como un estable máximo del grafo $G$.
Luego para cada vértice $u_i \in S_0$, sabemos por lema 1 que $\chi(G-\{u_i\})=\omega(G-\{u_i\})$, además $\omega(G-\{u_i\}) \leq \omega$, por lo que existe un $f$ $\omega$-coloreo del grafo $G-\{u_i\}$, defino los siguientes $S_i,\dots,S_{i+\omega}$ conjuntos como las clases de color de $f$, cada vértice de $G-\{u_i\}$ va a pertenecer a exactamente $1$ de estos conjuntos. Luego como puedo construir $\alpha$ de estos conjuntos, el lema 2 es valido.

**Lema 3**: Para cada $1 \leq i \leq \alpha\omega+1$, existe una clique $C_i$ de tamaño $\omega$ tal que:
	- $|V(C_i) \cap S_i| = 0$
	- $|V(C_i) \cap S_j|=1$ para cada $1\leq j \leq \alpha\omega + 1$ donde $i\neq j$
Primero pruebo el primer ítem, si dicha clique no existiese entonces todas las cliques de tamaño $\omega$ intersecan al conjunto $S_i$, esto hace que el subgrafo inducido $G-S_i$ tenga un numero de clique de como mucho $\omega-1$, como por lema 1 existe un $\omega-1$-coloreo de $G-S_i$, luego dicho coloreo puede extenderse a un coloreo de $G$ asignándole a cada vértice de $S_i$ un nuevo color, esto implica que $\chi(G)\leq \omega(G)$ lo que contradice la segunda proposición del lema 1. Por lo que existe una clique $C_i$ que es disjunta del estable $S_i$.
Para probar el segundo ítem, no puede ocurrir que $|V(C_i) \cap S_j| \geq 2$ ya que esto implicaría que $S_j$ no es un estable, así que se tiene que $|V(C_i) \cap S_j| \leq 1$, ya sabemos que $|V(C_i) \cap S_i| = 0$, por lo tanto:
$$\sum_{j=1}^{\alpha\omega+1} |V(C_i) \cap S_j| \leq \alpha\omega$$
Por el lema 2, cada vértice de $C_i$ aparece en al menos $\alpha$ de estos conjuntos, como hay $\omega$ vértices en $C_i$ se tiene que:
$$\alpha\omega \leq \sum_{j=1}^{\alpha\omega+1} |V(C_i) \cap S_j|$$
Y por lo tanto vale la igualdad, dado que $|V(C_i) \cap S_j| \leq 1$, el segundo ítem es valido y por lo tanto el lema 2 también lo es.

Finalmente, defino dos matrices $A$ y $B$ de tamaño $(\alpha\omega +1) \times n$, donde:
- $a_{ij}=1$ si $v_j \in S_i$ y $a_{ij}= 0$ si no.
- $b_{ij}=1$ si $v_j \in C_i$ y $b_{ij}=0$ si no.
Ahora las entradas del producto $AB^t$ son:
$(AB^t)_{ij} = \sum_{k=1}^n A_{ik} \cdot B_{jk}$
$A_{ik}\cdot B_{jk} = 1$ $\iff A_{ik} = 1 \land B_{ik} = 1 \iff v_k \in S_i \land v_k \in C_j \iff v_k \in S_{i} \cap C_j$
Por lo tanto:
$(AB^t)_{ij} = \sum_{k=1}^n A_{ik} \cdot B_{jk} = |S_i \cap C_j|$.

Que por el lema 3 sabemos que tiene la siguiente pinta:
$$AB^t = 
\begin{pmatrix}
0 & 1 & 1 & \dots & 1 & 1 & 1 \\
1 & 0 & 1 & \dots & 1 & 1 & 1 \\
1 & 1 & 0 & \dots & 1 & 1 & 1 \\
\vdots & \vdots & \vdots & \ddots & \vdots & \vdots & \vdots \\
1 & 1 & 1 & \dots & 0 & 1 & 1 \\
1 & 1 & 1 & \dots & 1 & 0 & 1 \\
1 & 1 & 1 & \dots & 1 & 1 & 0 \\
\end{pmatrix}
$$
La cual es invertible ya que sus columnas son linealmente independientes.

Utilizando las propiedades del rango de una matriz:
$\operatorname{rank}(AB) \leq \min\{\operatorname{rank} A, \operatorname{rank} B\}$
$\operatorname{rank} A \leq m$. $m=$ cantidad de columnas de $A$.

Se tiene que:
$\alpha\omega+1 = \operatorname{rank}(AB^t) \leq \min\{\operatorname{rank} A, \operatorname{rank} B^t\} \leq n$

$G$ es un grafo que cumple que $n \geq \alpha\omega + 1$, pero estábamos bajo la suposición de que $G$ era un grafo que cumplía $n \leq \alpha\omega$,  ABS!.

Este absurdo proviene de suponer que existe un contraejemplo de la vuelta, por lo que la propiedad es cierta.

El teorema es cierto y este teorema deriva en el teorema del grafo perfecto:
$G$ es perfecto $\iff$ 
$\forall H \text{ subgrafo inducido de G}: |V(H)| \leq \alpha(H)\cdot\omega(H) \iff$
$\forall H \text{ subgrafo inducido de G}: |V(H)| \leq \alpha(H)\cdot\alpha(\overline{H}) \iff$
$\forall H \text{ subgrafo inducido de }\overline G: |V(H)| \leq \alpha(\overline H)\cdot\alpha(H) \iff$
$\forall H \text{ subgrafo inducido de }\overline G: |V(H)| \leq \alpha(H) \cdot \omega(H) \iff$
$\overline{G}$ es perfecto