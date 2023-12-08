Sea $G$ el grafo del enunciado
a)
Para cualquier numero natural $n$, $gcd(n,1) = 1$
Esto implica que $1$ es un vértice aislado en el grafo.
Para $1 <n \leq 7$ se tiene que $2n \in V(G)$, por lo que existe el camino $n \to 2n \to 2$
(ya que $\gcd(2n,2) = 2$ $\forall n \in \mathbb N$).
Para $n>7$:
- $n=8$, existe el camino $8 \to 2$
- $n=9$, existe el camino $9 \to 3 \to 6 \to 2$
- $n=10$, existe el camino $10 \to 2$
- $n=11$, $11$ es primo y $\gcd(11,n)=1$ $\forall n\leq 15$
- $n=12$, existe el camino $12 \to 2$
- $n=13$, $13$ es primo y $\gcd(13,n)=1$ $\forall n \leq 15$
- $n=14$, existe el camino $14 \to 2$
- $n=15$, existe el camino $15 \to 3 \to 6 \to 2$.

Hay $3$ componentes conexas

b)
Si $a = b \cdot p$ con $p$ un numero primo se tiene que 
$\gcd(a,b) = b$ ya que $b$ es el máximo numero que divide a $b$ y $a$ es divisible por $b$.

Entonces la distancia entre dos números $a$ y $b$ va a ser la cantidad de factores primos que tiene $a / \gcd(a,b)$

Si $a = p_1 \cdot p_2 \cdot \dots \cdot p_k$ con $p_i \geq 2$ entonces $a \geq 2^k$.
$\gcd(a, p_1)= p_1$

Entonces $dist(a,p_1) = k-1$

Si $a=8=2^3$, $dist(8,2)=2$
