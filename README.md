# Ejercicio 1 de la práctica de GIT
### autor: Fiorella Ruiz

- ¿Qué comando utilizaste en el paso 11? ¿Por qué?
`$ git log`  para comprobar los commits en la rama styled
`$ git reset --hard HEAD~1` así deshago el último paso
y vuelvo al git-nuestro.md anterior. El archivo en el Working copy también cambia.

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
`$ git reflog`
`$ git reset --hard 246f6ad`
`$ nano git-nuestro.md`
Primero reviso los registros para ver a qué referencia tengo que retroceder.
Luego con "reset hard" retrocedo y deshago el cambio del paso 11. El cambio afecta al Working copy.
Finalmente confirmo que el archivo es el anterior

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
No. Por que no había ningún commit en master no incluido en styled, por lo tanto no se generaron conflictos.

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
Sí, porque en la rama htmlify hicimos un commit (modificar archivo git-nuestro.md) que en Styled no está y que afecta al mismo archivo. 

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No. Sólo se indicó que se "actualizó" el archivo git-nuestro.md al de la rama styled.
Esto se debe a que la rama styled contenía el commit de master. Lo único que pasó es que ahora master apunta al último commit de styled.

- ¿Qué comando o comandos utilizaste en el paso 25?
Primero usé: `$ git log --graph` pero luego, para hacerlo más simple:
`$ git log --pretty=oneline --graph`

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
Sí puede ser fast forward. La rama title nació del último commit de la rama master, por lo tanto el puntero de master puede ir directo hasta title sin que se tenga que hacer un commit extra.

- ¿Qué comando o comandos utilizaste en el paso 27?
`$ git reset HEAD~1`
La idea es retoceder sin hacer cambios en el Working Copy.

- ¿Qué comando o comandos utilizaste en el paso 28?
$ nano git-nuestro.md

- ¿Qué comando o comandos utilizaste en el paso 29?
`$ git branch -D title`

- ¿Qué comando o comandos utilizaste en el paso 30?
Primero `$ git reflog` para buscar la referencia donde está el merge que me interesa.
Luego `$ git reset --hard 74a1aa8` para hacer el cambio y cambiar también el Working Copy y tener nuevamente el título en el archivo.

- ¿Qué comando o comandos usaste en el paso 32?
`$ git reflog` para buscar la referencia del commit inicial y luego:
`$ git reset 0c2b3ec` para ir a ese commit sin cambiar el Working Copy.

- ¿Qué comando o comandos usaste en el punto 33?
`$ git reflog` para buscar la referencia del commit final y luego:
`$ git reset 74a1aa8` para ir a ese commit sin cambiar el Working Copy.