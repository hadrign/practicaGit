## Respuestas Ejercicio 1 Hadrian Grille

1. ¿Qué comando utilizaste en el paso 11? ¿Por qué?
	- Utilicé el comando _git reset —hard HEAD~1_ porque con este comando movemos el HEAD al commit anterior y añadiendo el HARD, descartamos los cambios del Working copy
2. ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
	- Primero utilicé el comando _git reflog_ para conocer los movimientos de nuestro repositorio y una vez localicé el identificador del commit a donde quería volver utilicé _git reset --hard bc44d51_ poniendo hard para recuperar los cambios que habíamos perdido y poniendo el identificador del commit al que queríamos volver.
	También se podia haber utilizado el _git reflog_ para identificar el commit al que queremos volver. Aplicar un _git reset_ a ese commit y finalmente descartar los cambios utilizando _git checkout -- documento.md_
3. El merge del paso 13, ¿Causó algún conflicto? ¿Por qué? 
	- Al intentar hacer un merge de la rama “styled” con “master” nos sale un mensaje de “Already up to date” esto es debido a que estamos intentando que la rama hijo absorba a su padre, pero este ya es así ya que styled tiene una referencia a su commit padre, con lo que git ya nos indica que no hay nada que hacer.
4. El merge del paso 19, ¿Causó algún conflicto? ¿Por qué? 
	- Si, ha habido conflictos porque el archivo a sido modificado en las mismas lineas en las dos ramas con lo que git nos advierte de ello y nos pide que elijamos con la que se debe quedar
5. El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
	- No se genero ningún conflicto porque el commit padre de Styled era master con lo que git sabe que styled ha sido realizado después y que los cambios son más recientes.
6. ¿Qué comando o comandos utilizaste en el paso 25?
	- Para dibujar el diagrama he utilizado el comando _git log --graph_
7. El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
	- No porque dejaríamos el segundo commit, cuando guardamos los cambios de la rama Style, inalcanzable.
8. ¿Qué comando o comandos utilizaste en el paso 27? 
	- Utilizamos _git reflog_ para conocer el SHA reducido del commit al que tenemos que mover y como no queremos perder los cambios en el working copy ejecutamos _git reset a760475_
9. ¿Qué comando o comandos utilizaste en el paso 28
	- Para descartar los cambio ejecutamos el comando _git checkout —- git-nuestro.md_
10. ¿Qué comando o comandos utilizaste en el paso 29? 
	- Para eliminar la rama title he utilizado el comando _git branch -D title_ , porque con -d no podríamos borrarla porque nos dice que dejamos commits inalcanzables.
11. ¿Qué comando o comandos utilizaste en el paso 30?
	- _git reflog para conocer el SHA reducido del merge (cfcf584) y después ejecutar _git reset —-hard cfcf584_ para recuperar el merge que habíamos deshecho y recuperar los cambios en el working copy
12. ¿Qué comando o comandos usaste en el paso 32? 
	- Ejecutamos primeramente _git reflog_ para conocer el identificador del commit al que queremos volver (149c7b9), después _git checkout 149c7b9_
13. ¿Qué comando o comandos usaste en el punto 33? 
	- Primeramente ejecutamos _git reflog_ para conocer el identificador del estado final (25bc3bb) y después ejecutamos _git checkout 25bc3bb_ para volver al estado final donde habíamos añadido el título.

