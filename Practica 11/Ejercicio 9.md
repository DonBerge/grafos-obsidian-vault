Dada una red $G$ donde el vértice $a$ es la fuente y el vértice $z$ el sumidero.
Sean $S$ y $T$ dos conjuntos que definen un corte, se tiene que $a \in S$, $a \in T$, $z \in \overline S$, $z \in \overline T$.

Por lo tanto:
- $a \in S \cap T$ y $a \in S \cup T$.
- $z \in \overline S \cup \overline T$ y $z \in \overline S \cap \overline T$, por leyes de De Morgan $z \in \overline{S \cap T}$ y $z \in \overline{S \cup T}$.

Como $S \cap T$ y su complemento forman una partición, $S \cap T$ define un corte. Lo mismo se puede decir para $S \cup T$ y su complemento.

Luego se tiene que:
$cap(S \cup T, \overline{S \cup T}) = sum\{uv \in E: u \in S \cup T \land v \notin S \cup T\}$
$= sum\{uv \in E: u \in S \lor u \in T \land v \notin S \land v \notin T\}$

Para el caso del otro corte se tiene análogamente que:
$cap(S \cap T, \overline{S \cap T})=sum\{uv \in E: u \in S \land u \in T \land v \notin S \lor v \notin T\}$

La unión de estos dos conjuntos son las aristas $uv$ que cumplen:
$u \in S \lor u \in T \land v \notin S \land v \notin T$
$\lor$
$u \in S \land u \in T \land v \notin S \lor v \notin T$
Esta será la proposición (1).


La unión de las aristas de los cortes definidos por $S$ y $T$ son aquellas que cumplen:
$u \in S$ $\land$ $v \notin S$
$\lor$
$v \in S$ $\land$ $v \notin T$
Esta es la proposición (2).

Notar que (1) $\implies$ (2).

Suponiendo (1) verdadero:
Si $u \in S \lor u \in T \land v \notin S \land v\notin V$:
- Si $u \in S$ se tiene que $v \notin S$ por lo tanto (2).
- Si $u \in T$ se tiene que $v \notin T$ por lo tanto (2).
Si $u \in S \land u \in T \land v \notin S \lor v \notin T$:
- Si $v \notin S$ se tiene que $u \in S$ y por lo tanto (2).
- Si $v \notin T$ se tiene que $v \in T$ y por lo tanto (2).

Por ende (2) es valido cuando (1) es valido.

Si (1) es falso la implicancia también es valida.

Por lo tanto (1) $\implies$ (2).

Como toda arista que cumple (1) también cumple (2), toda arista que pertenezca a los cortes definidos por $S \cup T$ y $S \cap T$ pertenece también a los cortes definidos por $S$ y $T$.

Tomando las capacidades de ambos cortes, se tiene lo que se quería probar.

---
Puesto que $S$ y $T$ definen cortes minimos, se tiene que:
1. $cap(S,\overline S) = cap(T, \overline T)$
2. $cap(S \cup T, \overline{S \cup T}) \geq cap(S,\overline S)$
3. $cap(S \cup T, \overline{S \cup T}) \geq cap(S,\overline S)$

Por ende combinando (2) y (3) :
$cap(S \cup T, \overline{S \cup T}) + cap(S \cup T, \overline{S \cup T}) \geq cap(S,\overline S) + cap(S,\overline S)$
$\implies$ por (1)
$cap(S \cup T, \overline{S \cup T}) + cap(S \cup T, \overline{S \cup T}) \geq cap(S,\overline S) + cap(T,\overline T)$

Pero por el ejercicio anterior:
$cap(S \cup T, \overline{S \cup T}) + cap(S \cup T, \overline{S \cup T}) \leq cap(S,\overline S) + cap(T,\overline T)$

Por ende ambos términos son iguales.
$cap(S \cup T, \overline{S \cup T}) + cap(S \cup T, \overline{S \cup T}) = cap(S,\overline S) + cap(T,\overline T)$ (4)

Por (2) y (3) pueden ocurrir 3 cosas con los términos de la izquierda:
- Ambos tienen capacidades estrictamente mayores que el corte definido por $S$, esto es una contradicción con (4).
- Uno tiene una capacidad igual a la del corte de $S$ y el otro es estrictamente mayor, nuevamente esto seria una contradicción con (4).
- Los dos tienen capacidades iguales a la del corte de $S$. Esta es la única posibilidad que no invalida (4).

Por lo tanto, los cortes definidos por $S \cup T$ y $S \cap T$ son cortes mínimos.