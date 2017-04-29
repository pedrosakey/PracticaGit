## Preguntas


- ¿Qué comando utilizaste en el paso 11? ¿Por qué?
	 
	 *git reset --hard HEAD~1*

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

	*git reflog

	fd736d7 HEAD@{0}: reset: moving to HEAD~1
	3a43944 HEAD@{1}: commit: Añado segunda version de git nuestro
	fd736d7 HEAD@{2}: checkout: moving from master to styled
	fd736d7 HEAD@{3}: commit (initial): Primera version del git nuestro*

	*git reset --hard 3a43944*

	Usé reflog porque es lo primero que se me ocurrió pero hubiera sido mas eficiente utilizar la referencia directamente con:

	*git reset --hard HEAD@{1}*


- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
	
	Already up-to-date. Ya está incluido el commit de la rama master. Este merge no tiene sentido.

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
	
	NO, merge no fast forward crea un commit nuevo con dos padres y avanza la rama styled a ese commit

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

	NO, merge fast-forward master avanza al commit de styled


- ¿Qué comando o comandos utilizaste en el paso 25?

	*git log --graph*

	Listo con

	*git config --list*

	Veo que tenemos un alias para listar los alias
	Hacemos un git alias
	Para pintar el grafo bonito tenemos el alias llg
	llg	 => log --color --graph --pretty=format:'%C(bold white)%H %d%Creset%n%s%n%+b%C(bold blue)%an <%ae>%Creset %C(bold green)%cr (%ci)' --abbrev-commit

	*git llg*


- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

	SI, porque la rama master se encuentra en la lista de commits de la rama title, en concreto la rama title está un commit por encima.

			* 8e5fc7b8edaa8c4eed238037e90e797bfb3ee5fe  (HEAD -> title)
			| Añado titulo a git nuestro
			| Pedro Sánchez Castro <pedro@sanchez.com> 4 hours ago (2017-04-29 09:46:28 +0200)
			*   c97d03199ffb57599f1ed24a6d5ac364b1ee45b2  (styled, master)
			|\  Merge branch 'htmlify' into styled
			| | Pedro Sánchez Castro <pedro@sanchez.com> 4 hours ago (2017-04-29 09:29:15 +0200)

- ¿Qué comando o comandos utilizaste en el paso 27?
	
	*git reset HEAD~1*


- ¿Qué comando o comandos utilizaste en el paso 28?
 	
 	*git checkout git-nuestro.md*

- ¿Qué comando o comandos utilizaste en el paso 29?
	
	*git branch -D title*

- ¿Qué comando o comandos utilizaste en el paso 30?

	*git checkout 8e5fc7b* 

	(hash rama title). Puntero al commit
	You are in 'detached HEAD' state

	*git branch title* 
	Creo la rama que borre antes

	*git checkout master*
	Vuelvo a puntar a la rama master

	*git reset --hard b62094b*

	Busco en el reflog el merge y avanzo con master y head	



- ¿Qué comando o comandos usaste en el paso 32?

	git log , abajo del todo commit inicial

	commit fd736d75adba77bea6c21c01f2470a507f49eacd
	Author: Pedro Sánchez Castro <pedro@sanchez.com>
	Date:   Sat Apr 29 08:44:36 2017 +0200

    Primera version del git nuestro

    *git reset --hard fd736d75adba77bea6c21c01f24*


- ¿Qué comando o comandos usaste en el punto 33?

	Util usar aqui la referencia al reflog

	*git reset --hard HEAD@{1}*
