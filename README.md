# Comandos-Git

![image](https://user-images.githubusercontent.com/78452543/226786216-e9aff967-dc1e-4308-b629-c4875babf707.png)

## Git:
Es un software de "Control de Versiones" que fue diseñada por Linus Torvalds, es Open Source y muy potente, permite registrar el historial de cambios de un proyecto y facilita a los usuarios a llevar el seguimiento de los cambios de un archivo.

## Comandos importantes de Git:

### Establecemos los valores de configuración.

Ahora debemos establecer las variables de configuración global, que son muy importantes, especialmente si estás trabajando con otros desarrolladores. La principal ventaja de esto es que es más fácil averiguar quién ha hecho un commit de determinado bloque de código.

- git config puede ser usado para establecer una configuración específica de usuario, como el nombre de usuario ,y el email, etc.
        
        git config --global user.name "nombre"
        git config --global user.email "correo@correo.com"
   
- Habilitar la útil colorización del producto de la línea de comando.

        git config --global color.ui auto

- Ver la configuracion.

        git config --list
       
- Puedes establecer fácilmente un alias para cada comando mediante git config.

        git config --global alias.ci 'commit'

- Con este comando haremos que git detecte automaticamente lo que queremos escribir

        git config --global help.autocorrect 1
        
### Crear repositorios

- Iniciar un nuevo repositorio

        git init
- Clonar un repositorio existente, descarga un proyecto y toda su historia de versión
       
       git clone <https://link-con-nombre-del-repositorio>

- Agregar archivos a la área de preparación
       
       git add <nombre-del-archivo>   // Agregar un archivo especifico.
       git add .                 // Agregar todos los archivos.

- Deshacer los git add

        git reset .
- Hacer commit de los cambios con un mensaje que explique los cambios
        
        git commit -m "mensaje de confirmación"
        git commit -a -m "saltar el git add" // Con este comando nos saltamos de hacer el git add 

- Enumera todos los archivos nuevos o modificados que se deben confirmar
        
        git status -s
- Muestra las diferencias de archivos que no se han enviado aún al área de espera

        git diff

- Modificar los git commit

        git commit --amend

- Deshacer los commit

        git reset --soft HEAD~1   // Borra el ultimo commit y no borra los cambios
        git reset --hard HEAD~1   // Borra el ultimo commit y si borra los cambios

- Subir los archivos a un repositorio remoto
        
        git push origin <nombre-de-la-rama>
        
### Ramas

- Crear una nueva rama

        git branch <nombre-de-la-rama>
- Crear una rama rama (Segunda opción)
        
        git checkout -b <nombre-de-la-rama> // Creará la nueva rama y cambiará a ella al instante

- Visualiza todas las ramas en el repositorio actual

        git branch
        git branch --list

- Cambiar a la rama especificada y actualiza el directorio activo
        
        git checkout <nombre-de-la-rama>

- Volver a la rama anterior sin necesidad de escribir el nombre
        
        git switch -

- Borrar una Rama
        
        git branch -D <nombre-de-la-rama>

- Lista los branches con mas información

        git show-branch

- Combina el historial de la rama especificada con la rama actual

        git merge <nombre-de-la-rama>

### Rebase
- Se usa para aplicar ciertos cambios de una rama en otra, Une el branch actual con la main

        git rebase

- Cuando resolvemos los conflictos --continue continua la secuencia del rebase donde se pauso

        git rebase --continue

- Omite el conflicto y sigue su camino
        
        git rebase --skip
- Devuelve todo al principio del rebase

        git rebase --abort

- Se usa para aplicar ciertos cambios de una rama en otra

        git rebase <nombre-de-la-rama>

### Remote

- Permite ver todos los repositorios remotos asigandos o a los que apunta tu repositorio local
        
        git remote -v

- Crear un repositorio remoto y lo enlaza con tu repositorio local
        
        git remote add <nombre/origin> <url>

- Remover el enlace al repositorio remoto
         
        git remote rm <nombre/origin>

- Permite cambiar la URL del repositorio remoto

        git remote set-url origin <url>

### Tag

- Crea un nuevo tags
        
        git tag v0.0.1 -m "primera versión"

- Muestra una lista de todos los tags
        
        git tag

- Te permite ver cómo estaba el repositorio en cada estado
        
        git show v0.0.1

- Enviar al repositorio en GitHub

        git push --tags

### OTROS COMANDOS
- Busca los cambios nuevos y actualiza el repositorio
        
        git pull origin <nombre-de-la-rama>

- Verifica cambios en el repositorio online con el local
        
        git fetch

- Almacena temporalmente el trabajo sin comentar.
        
        git stash

- Para recuperar los últimos cambios desde el stash a tu staging.
        
        git stash pop

- Listar el historial de versiones de la rama actual.
         
        git log
        git log --oneline --graph // Con este comando se lo puede ver mucho mejor 
        git log --pretty=oneline --graph --decorate --all // Otra forma mas completa

- Deshacer el commit si ya se hizo push
        
        git revert 3a67899

- Para recuperar archivos que borre
        
        git checkout -- . 

- Borrar un archivo

        git rm <nombre-del-archivo> 

- Para recuperar archivos que borre después del git rm

        git checkout HEAD -- .

- Eliminar un repositorio de Git creado con ‘git init’ en un directorio
        
        cd carpeta/
        rm -rf .git

- Cambia el nombre del archivo y lo prepara para commit
        
        git mv [archivo-original] [archivo-renombrado]
