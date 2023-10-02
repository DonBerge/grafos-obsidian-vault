a)
Suponiendo que el grafo de Petersen efectivamente tiene un ciclo hamiltoniano. Esto quiere decir que tiene un $C_{10}$ como subgrafo

El grafo de Petersen tiene $15$ aristas. Si se quiere completar el ciclo $C_{10}$ para formar el grafo de Petersen es necesario añadir $5$ aristas adicionales.

Se tiene entonces el siguiente grafo

```math
```
Suponiendo s.p.d.g que primero se añade una arista en $1$

Los vértices $2$ y $10$ no pueden conectarse porque ya están conectados.
Los vértices $3$, $4$, $9$ y $8$ no pueden conectarse ya que hacerlo forma un ciclo de $3$ o un ciclo de $4$(lo cual es imposible ya que el grafo de Petersen no tiene ninguno).

Es decir que hay que conectar $1$ bien con el vértice $5$, $6$ o $7$. Suponiendo s.p.d.g que se conecta el vértice $1$ con el $6$.

```math
```

Dado que hay que seguir añadiendo aristas, se puede proseguir a añadir una arista al vértice $5$.

Conectar $5$ con $1$ genera un vértice de grado $4$.
Conectar $5$ con $3$, $7$ genera un ciclo de $3$.
Conectar $5$ con $4$ y $6$ es imposible porque ya están conectados.
Conectar $5$ con $2$, $8$ y $10$ genera un ciclo de $4$.

La única posibilidad es conectar los vértices $5$ y $9$.

```math
```

Conectar el vértice $10$ con cualquier otro vértice genera una contradicción.

Conectar $10$ con $1$, $9$, $5$ o $6$ genera un vértice de grado $4$.
Conectar $10$ con $8$, $2$ genera un ciclo de $3$.
Conectar $10$ con $3$, $7$ o $4$ genera un ciclo de $4$.

Por lo tanto el grado de Petersen no puede tener un ciclo hamiltoniano.

---

El grado de Petersen contiene un ciclo hamiltoniano que ignora un vértice.

```math
```

Eliminar dicho vértice $v$ genera un grafo con un ciclo hamiltoniano.

Dado que el grafo de Petersen es vértice transitivo, existe un automorfismo desde el vértice $v$ a cualquier otro vértice del grafo. Por lo que la propiedad se mantiene para cualquier otro vértice.