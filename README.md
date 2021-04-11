# Comandos Básicos de Git



## Tabla de Contenido

- [Configuración inicial](##Configuracion%20inicial )
- [Llevar los Archivos al Stage](##Llevar%20los%20Archivos%20al%20Stage)
- [Llevar los Archivos al Stage](##Llevar%20los%20Archivos%20al%20Stage)
- [Comentar los archivos para mandar a repositorio](##Comentar%20los%20archivos%20para%20mandar%20a%20repositorio)
- [Deshaciendo Cambios en el repositorio](##Deshaciendo%20Cambios%20en%20el%20repositorio)
- [Historial de Cambios](##Historial%20de%20Cambios)
- [Ramas](##Ramas)
- [Unir Ramas](##Unir%20Ramas)
- [Enviar archivos a Repositorio remoto](##Enviar%20archivos%20a%20Repositorio%20remoto)

<br>

## Configuración inicial
---

###### git config --global init.defaultbranch "master"
- Determina la rama "master" como la principal.

###### git config --global user.name "username"
- Determina el nombre de usurario principal.

###### git config --global user.email "email"
- Determina el correo de usurario principal.

###### git init
- Sirve para iniciar un repositorio local.

[Documentación completa del comando 'git init'](https://git-scm.com/docs/git-init)
[Documentación completa del comando 'git config'](https://git-scm.com/docs/git-config)


## Llevar los Archivos al Stage
---

###### git add .
- Agrega todos los archivos al Stage.

###### git add \'archivo'
- Sirve para añadir un archivo especifico al Stage.

###### git rm --cached \'archivo'
- Para remover un archivo especifico del Stage.

###### git restore \'archivo'
- Para descartar los cambios del archivo en el directorio.

[Documentación completa del comando 'git add'](https://git-scm.com/docs/git-add)
[Documentación completa del comando 'git rm'](https://git-scm.com/docs/git-rm)
[Documentación completa del comando 'git restore'](https://git-scm.com/docs/git-restore)




## Comentar los archivos para mandar a repositorio
---

###### git commit
- Se abre el editor de texto VIM para poder hacer el comentario.
	- *comentarios para el editor VIM*.
	- **i** para editar.
	- **esc** para salir de edición.
	- **usar** :wq para guarda y salir.
	- **q** para salir sin guardar.
	- **w** para guardar.

###### git commit -m "mensaje"
- Escribir directamente el mensaje sin pasar por el editor de texto.

###### git commit -am "mensaje"
- Añade todos los archivos al repositorio y agrega comentario.
	-No funciona si los archivos son nuevos, en ese caso tiene que uar "git add ." desde la raiz.

[Documentación completa del comando 'git commit'](https://git-scm.com/docs/git-commit)



## Deshaciendo Cambios en el repositorio
---

###### git checkout \'archivo'
- Regresa al estado anterior al archivo.

###### git checkout -f
- Fuerza el regreso al estado anterior del archivo.

###### git restore --staged \'archivo'
- Quita el archivo del stage y lo regresa al área de trabajo.

###### git checkout \'hash'
- regresa el espacio de trabajo al hash seleccionado.
	-para ver el hash usar `git log`.

###### git checkout master
- regresa el espacio de trabajo al al ultimo hash creado (mas reciente).


[Documentación completa del comando 'git checkout'](https://git-scm.com/docs/git-checkout)



## Historial de Cambios
---

###### git logs
- Muestra el historial de cambios del repositorio.

###### git diff \'archivo'
- Muestra la diferencia de cambios entre el espacio de trabajo y el Stage.

###### git diff --stat \'archivo'
- Muestra información simple del del archivo.

###### git diff --numstat \'archivo'
- Muestra información simple en números del del archivo.

###### git log --oneline --all --graph --decorate
- Muestra una linea de tiempo gráfica del historial de cambios.



[Documentación completa del comando 'git log'](https://git-scm.com/docs/git-log)



## Ramas
---

###### git checkout -b "nombre de la rama"
- Crea una nueva Rama y te cambia a esa rama.

###### git branch
- Muestra todas las ramas del repositorio.
	- La rama que comiencecon `*` es la rama que esta seleccionada

###### git branch -d \'nombre de la rama'
- Elimina la rama que hayas elegido

###### git switch \'nombre de la rama'
- Te cambia a la rama que hayas elegido

[Documentación completa del comando 'git branch'](https://git-scm.com/docs/git-branch)



## Unir Ramas
---

###### git merge \'nombre de la rama'
- Une la rama que hayas seleccionado a la rama donde te encuentres


[Documentación completa del comando 'git branch'](https://git-scm.com/docs/git-merge)




##Enviar archivos a Repositorio remoto
---

###### git push origin master
- Envia los archivos a la rama master del repositorio remoto<

###### git push origin 'branch'
- Envía los archivos a la rama que elijas del repositorio remoto


[Toda la documentación GIT](https://git-scm.com/docs)