Si $G$ tiene al menos un ciclo y todo ciclo tiene longitud al menos $k$ entonces para toda cara $f$ del grafo $G$ se tiene que $long(f)\geq k$

Por tanto $2a = \sum_{f \in F} long(f) \geq k\cdot c \implies c\leq \frac 2 k a$

Por la formula de Euler: $v-a+c = 2$
Reemplazando:
$2=v-a+c \leq v - a + \frac{2}{k} a = v +\left(-1+\frac 2 k\right)a = v - \left(\frac{k-2} k\right)a$
$a \leq \frac{k}{k-2}\left(v-2\right)$
$\blacksquare$