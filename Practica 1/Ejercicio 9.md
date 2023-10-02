a) Todo camino es bipartito
	Los grafos caminos son los grafos $G(V,E)$ donde
	$V = \{v_1,\dots,v_n\}$
	$E=\{(v_i,v_{i+1}) : i \in [\![1,n-1]\!]\}$
	Tomando las particiones:
	$X = \{v_i : i \text{ impar}\}$
	$Y = \{v_i : i \text{ par}\}$
	Se tiene que los vértices impares solo están conectados con los vértices pares y viceversa
	El camino es bipartito
b) Un ciclo es bipartito $\iff$ Tiene longitud par
	Tiene longitud par $\implies$ El ciclo es bipartito)
		En el ciclos los conjuntos de vertices son de la forma
		$V = \{v_1,\dots,v_n\}$
		$E=\{(v_i,v_{i+1}) : i \in [\![1,n-1]\!]\} \cup \{(v_n,v_1)\}$
		Tomando las mismas particiones del ejercicio (a) se tiene que el grafo es bipartito
	El ciclo es bipartito $\implies$ Tiene longitud par
		Pruebo la contrarrecíproca, si tiene longitud impar entonces no es bipartito.
		Suponiendo que efectivamente el grafo es bipartito, entonces es posible particionarlo.
		Empezando por un vértice $v$ cualquiera que pertenece a la partición $X$.
		Este vértice esta conectado a otros 2 que tienen que pertenecer a la partición $Y$
		Luego cada uno de estos vértices esta conectado a otros dos que pertenecen a la partición $X$
		Repitiendo el proceso $k$ veces para armar las particiones se tiene que
		$|X|$ es impar e $Y$ par
		El ciclo eventualmente puede terminar de 2 formas:
		1) Termina con un único vértice, en este caso las particiones terminan siendo correctas pero el ciclo es par
		2) Terminan con dos vértices conectados entre si, el ciclo es par pero el grafo no es bipartito, absurdo
	Por lo tanto el grafo no puede ser bipartito sabiendo que el ciclo es impar.