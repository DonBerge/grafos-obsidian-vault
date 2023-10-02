a) El diámetro del grafo es $3$(se prueba buscando todas las distancias posibles y eligiendo la máxima)

b) El diámetro del grafo de Petersen es 2
Como el grafo de Petersen es vértice transitivo, basta con calcular todas las distancias desde un vértice particular y elegir la distancia máxima.

En este caso, la distancia máxima es $2$.

c) En el caso del grafo $Q_n$, el diámetro es $n$

Dados dos vértices del hipercubo, la distancia entre ellos es la cantidad de bits en la que difieren.

Si dos vértices $x,y$ de un hipercubo $Q_n$ difieren en exactamente $k$ bits, entonces $d(x,y)=k$

Si partiendo de $x$ se decide tomar una arista entonces un bit de $x$ va a cambiar.

Es posible tomar $k$ aristas para llegar de $x$ a $y$(una por cada bit en el que difieren) por lo que $d(x,y) \leq k$

Luego la distancia no puede ser menor estricta que $k$ ya que si se toman menos aristas alguno de los $k$ bits distintos va a permanecer inalterado.

Entonces la máxima distancia entre dos vértices del grafo va a hacer igual al máximo numero de componentes en las que pueden diferir, en este caso $n$.

d)
En el caso de $K_n$ el diámetro es $1$.

Para $u,v$ vértices distintos del grafo, por definición hay una arista que los conecta así que $d(u,v) = 1$.

Resulta entonces que la máxima distancia entre dos vértices cualesquiera solo puede ser $1$.