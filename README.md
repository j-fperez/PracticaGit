En el paso 11 utilizo el comando git reset --hard HEAD~1 porque es la forma de que pierda los datos realizados en el working copy.

En el paso 12 ejecuto primero el comando git reflog paver la lista de todas las acciones que hemos realizado.
Localizo el identificador 8f1d673 que corresponde al commit que acabamos de deshacer.
Entonces ejecuto el comando git reset --hard 8f1d673 para volver al último commit

En el paso 13 el merge no causa ningún conflicto porque no hemos modificado el archivo git-nuestro.md en ambas ramas en las mismas lineas.
En la rama styled eliminamos la primera línea, así que no coincide ninguna línea en las dos ramas.

El merge del paso 19 no crea conflictos porque se modifica el archivo git-nuestro.md en ambas ramas en las mismas líneas.

El merge del paso 21 no crea conflictos porque el archivo git-nuestro.md es el mismo en las dos ramas.

En el paso 25 utilizo git log --graph
                      git log --decorate
                      git log --pretty=oneline
También puede utilizarse una combinación de varias opciones como git log --graph --decorate --pretty=oneline
También puede utilizarse un alias (ejemplo, git graph)

El merge del paso 26 no podría ser fast forward, ya que el puntero HEAD apunta a aster pero no a title.

En el paso 27 utilizo el comando git reset HEAD~1

En el paso 28 utilizo el comando git checkout -- git-nuestro.md

En el paso 29 utilizo  el comando git branch -D title

En el paso 30 utilizo el comando git reflog para ver el hash del merge (creo que era 99ba391).
Utilizo el comando git reset --hard 99ba391 para rehacer el merge.

En el paso 32 utilizo git log para ver el hash del commmit inicial(no lo tengo apuntado).
Utilizo el comando git checkout <hash_commit_inicial> para volver al commit inicial.

En el paso 33 hago lo mismo que en el paso 32. Primero utilizo git lo para ver el hash del commit final (creo que es 99ba391).
Luego utilizo el comando git checkout 99ba391 para volver al estado final, cuando pusimos el título del poema.

NOTA:
Cuand iba a subir los cambios al repositorio remoto me desapareció el fichero README.md, por lo que algunos hashes no los he apuntado
o puede que estén mal escritos.

Gracias.
