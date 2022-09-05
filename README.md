# Estados de Git
![](https://i.ibb.co/pP4Ccpk/2021-04-19-14-05-59-Git-Cheat-Sheet.png) 

## :red_square: CONFIGURACIÓN.
### :red_circle:  Antes de comenzar a crear commits

#### git version
~~~
git version (ver si esta instalado)
~~~
#### git help 
~~~
git help (Muestra comandos existentes)
git help NombreComando (Muestra descripción del comando)
~~~
#### git config 
Obtiene y configura el repositorio o las opciones globales.
~~~
git config global --user.name "Nombre del autor"
git config global --user.email "Correo del autor"
~~~
~~~
git config --list (muestra las configuraciones de git)
~~~
#### git config (Alias)
~~~
git config --global alias.ATAJO "COMANDO"
git config --global -e (registro editable)
git config --global -l (lista de alias)
~~~
##  :orange_square: WORKING DIRECTORY
### :orange_circle: Primeros pasos
#### git init
~~~
git init (Crea un repositorio local o reinicia uno)
git init [project name] (Crea un repositorio con nombre)
~~~
#### git add 
~~~
git add (Agrega el contenido del archivo al indice)
git add NombreArchivo (Agrega archivo)
~~~
~~~
git add . (Agrega todos los archivos)
git add -A (Agrega todos los archivos)
git add --all (Agrega todos los archivos)
~~~
~~~
git add "*.txt" (Agrega todos los txt de TODO el proyecto)
git add *.txt (Agrega todos los txt en el directorio actual)
git add <lista de archivos> (Agrega los archivos que listemos)
git add pdfs/*.pdf (Agrega todos los PDFs dentro de la carpeta PDFs)
git add pdfs/ (Agrega todos los archivos dentro de la carpeta PDFs)
~~~

## :yellow_square: STAGING AREA
### :yellow_circle: Iniciando proyecto
#### git reset
~~~
git reset (Restablece HEAD actual al estado especificado)
git reset NombreArchivo (excluye archivo)
git reset HEAD NombreArchivo (deshace cambios en el archivo)
git reset --soft NumeroCommit (deshace commit)
git reset --soft HEADˆ (deshace ultimo commit)
git reset --hard NumeroCommit (deshace el commit y borra lo ultimo)
~~~
#### git status
~~~
git status (Muestra el estado del árbol de trabajo)
git status -s ("s" de silent o silencioso)
git status -s -b ("silent" y "branch")
git status -sb (igual "-s -b")
~~~
#### git commit
~~~ 
git commit (Registra los cambios en el repositorio)
git commit -m "NombreCommit" (registra commit)
git commit -am "NombreCommit" (registra solo modificados)
git commit --amend (Registro de commit)
git commit --amend -m "NombreCommit" (Renombrar)
~~~
#### git log
~~~
git log (Muestran los registros de commits)
git log --oneline (muestra numero y commit)
git log --oneline -n 5 (muestra vista 5 ultimos)
git log --oneline --all (muestra todas las ramas)
git log --oneline --all --graph --decorate (muestra gráfica)
~~~
#### git rm
~~~
git rm --cached NombreArchivo (Elimina archivos del árbol de trabajo y del índice) 
~~~
### :yellow_circle: Trabajando con ramas
#### git branch
~~~
git branch (ver todas las ramas)
git branch NuevaRama (Crea rama)
git branch -D NombreRama (elimina rama)
git branch -d NombreRama (elimina rama)
~~~
#### git merge 
~~~
git merge (Une dos o más historias de desarrollo juntas)
git merge NombreRama (Une la rama master con otra rama)
~~~
###### Forward, Automática, Manual
![](https://i.ibb.co/RTbTmxH/merge.jpg)





## :blue_square: LOCAL REPOSITORY
### :large_blue_circle: Restaura o deshace cambios realizados
#### git checkout 
~~~
git checkout (Deshace cambios)
git checkout NombreArchivo (Deshace cambios del archivo)
git checkout carpeta/Archivo (Deshace cambios del archivo)
git checkout numeroCommit (Deshace cambios del commit)
git checkout --. (Restaura todos los archivos eliminados)
git checkout -f (restaura todos los cambios) 
git checkout master (restaura a ultimo commit)
~~~
### :large_blue_circle: Crea Rama
~~~
git branch NombreRama (crea rama)
git checkout -b  (crea rama y se traslada)
~~~
### :large_blue_circle: Subir cambios
~~~
git push (Sube cambios a repositorio remoto)
git push  origin <master> (Reemplaza "master" si es a otra rama)
~~~
### :large_blue_circle: Cambiar de Rama
~~~
git switch NombreRama (Cambia de rama)
git checkout NombreRama (Cambia de rama)
git checkout master (Cambia a rama master)
~~~




## :green_square: REMOTE DIRECTORY

### :green_circle: Crear un Repositorio
#### git clone
~~~
git clone my_url
~~~
### :green_circle: Sincronizar
#### git pull 
~~~
git pull (Obtenga cambios desde el origen (sin fusión))
git pull --rebase (Obtenga cambios de origin y rebase)
~~~
#### git fetch
~~~
git merge (Une dos o más historias de desarrollo juntas)
git merge NombreRama (Une la rama master con otra rama)
~~~


## :brown_square: OTROS COMANDOS
### :brown_circle: Más comandos

#### git reflog 
Mantiene un registro de todo lo que se hace. Te salva la vida.
~~~
git reflog (Mantiene un registro de todo)
~~~

#### git restore
___Restaura___ archivos de árbol de trabajo.

~~~
git restore --staget NombreArchivo
~~~

#### git diff
___Muestra los cambios entre confirmaciones___, confirmaciones y árbol de trabajo, etc.

~~~
git diff --stat NombreArchivo (muestra estadistica de cambios)
git diff --staged (verifica archivos en staged)
~~~



#### git tag
Crea, enumera, elimina o verifica un objeto de etiqueta firmado con GPG

~~~
git tag NombreTag (crea tag)
git tag -a VersionTag #commit -m "NombreTag" (crea tag desde commit) 
git tag (ver tags) 
git tag -d NombreTag (eliminar tag)
~~~

### :brown_circle: Ignorar archivos
#### .gitignore
Crear archivo ".gitignore" dentro colocar la rutas de los archivos a ignorar y se puedo comentar con "# comentario".

~~~
carpeta/ignorar.txt (ruta) 
ignorar_carpeta
~~~