a)
Sea $v_1,v_2,v_3,\dots,v_n$ un camino de $v_1$ a $v_n$

Dicho camino repite vértices.

Es decir existe una o mas subsecuencias de vértices
$v_i,v_{i+1},v_{i+2},\dots,v_{j},v_{j+1},v_{j+2}$
Donde $v_i = v_j$

Sea el camino donde se eliminan todas estas subsecuencias salvo aquella(si existe) donde $v_i=v_1$ y $v_j = v_n$(si hay mas de una de este tipo, se deja solo una).

Dicho camino es el camino simple buscado.

b)
Un circuito es un camino cerrado que no repite aristas.

Si existe un circuito que contiene a $v$, entonces existe un camino cerrado que empieza y termina en $v$, por el ejercicio a), existe un ciclo que empieza y contiene a $v$.