- ¿Qué comando utilizaste en el paso 11? ¿Por qué? 
   Usé el comando git reset --hard HEAD~1 ya que se indica que hay que perder los cambios de working copy,
   si no pusiera el --hard los cambios de worling copy seguirían estando.
- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué? 
	Primero git reflog para localizar el identificador hash del commit que quiero rehacer, y luego
	git reset --hard <id del commit que quiero rehacer>, usando --hard para que working copy tenga los cambios de ese commit
- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué? 
	No causó ningún conflicto, ya que la rama styled ya tenía los cambios de master, antes de hacer la modificación
	de la rama styled, si se hubiera cambiado alguna línea del archivo en master tras los cambios en styled, si hubiera dado conflicto
- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué? 
	Si causó conflicto, porque en htmlify, se hicieron cambios en el archivo de texto, en las mismas líneas que también
	se modificaron en la rama styled.
- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué? 
	No causó ningún conflicto, ya que la rama styled ya que se hizo con fast-forward, esto fue posible porque styled
	nació de un commit de master en el que ambas ramas tenían el mismo contenido en el archivo de texto, y este archivo de texto
	nunca se modificó en master
- ¿Qué comando o comandos utilizaste en el paso 25? 
	git log --graph --pretty=oneline primero este comando, pero también creo otro alias global usando
	git config --global alias.graph2 "log --graph --pretty=oneline" para luego usar git graph2
- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué? 
	No, porque master ya hizo un merge fast forward con styled y se situó en el commit de la rama styled con sus cambios,
	no se puede hacer merge con ff con title porque entonces se perdería el commit de styled.
- ¿Qué comando o comandos utilizaste en el paso 27? 
	git reset HEAD~1 ya que indica que no hay que perder los cambios del working copy
- ¿Qué comando o comandos utilizaste en el paso 28? 
	git restore git-nuestro.md
- ¿Qué comando o comandos utilizaste en el paso 29? 
	git branch -D title
- ¿Qué comando o comandos utilizaste en el paso 30? 
	git reflog para sacar el id del commit antes del merge y a continuación 
	git reset --hard <id-del-commit-antes-del-merge>
- ¿Qué comando o comandos usaste en el paso 32? 
	git reflog para sacar el id del primer commit y a continuación git reset --hard  <id-del-primer-commit>
- ¿Qué comando o comandos usaste en el punto 33?
	git reflog para sacar el id del commit final (cuando se puso titulo al poema) 
	y a continuación git reset --hard  <id-del-commit-cuando-se-puso-titulo-al-poema>
