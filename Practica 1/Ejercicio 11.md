a) Muestre que, en todo grupo de dos o más personas, existen siempre dos personas que tienen exactamente el mismo número de conocidos en el grupo.
	Sea el grafo donde los vértices representan a personas y las aristas unen a dos personas distintas que se conocen.
	Bajo esta suposición una persona no se puede conocer a si misma, así que no hay lazos.
	Como el grafo representa un grupo de personas, no hay vértices aislados.
	Los grados de un vértice $v$ representa para una personas del grupo a cuantas personas distintas del grupo conoce.
	Como hay $n$ personas y $n-1$ posibles grados($1,2,\dots,n-1$). Por principio del palomar va a haber 2 grados que van a repetir y por lo tanto el enunciado se cumple.
b) Describa un grupo de cinco personas en el que dos personas cualesquiera tienen exactamente un conocido en común. ¿Existe un grupo de cuatro personas con esta misma propiedad?
	Voy a probar que no existe un grupo de 4 personas con esta propiedad
	Sean los vértices $x,y,z,w$ de un grafo que cumple esta propiedad
	Tiene que haber si o si aristas entre los vértices
	Suponiendo sin perder generalidad que $x$ e $y$ están conectados, estos vértices tienen un vértice en común, suponiendo que $z$ es este vértice
	Hasta ahora las aristas son $(x,y)$ $(x,z)$ $(y,z)$, entonces el grafo inducido por los vértices $\{x,y,z\}$ es un $K_3$
	$w$ tiene que conectarse a algún vértice, si se conecta a $v \in \{x,y,z\}$ después tiene que conectarse a otro vértice $u\neq v \in \{x,y,z\}$ ósea que a su vez $\{w,v,u\}$ es un $K_3$
	Ahora si se miran los vértices $q \in \{x,y,z\}, q \neq u \land q \neq v$ y $w$ se tiene lo siguiente:
	$w$ no esta conectado a $q$(sino $u,v$ tiene en común a $w$ y $q$)
	$w$ esta conectado a $u,v$
	$q$ esta conectado a $u,v$
	$w$ y $q$ tienen $2$ vértices en común, absurdo.
