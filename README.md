# 10 comandos Linux que debes conocer

## 1. pwd
Significa Personal Working Directory te muestra la ruta del directorio en que estás ubicado actualmente.

~~~
$ pwd
/home/alejandro/EDteam
~~~

## 2. mkdir
Significa Make Directory y con él puedes crear una nueva carpeta con el nombre que indiques.

~~~
mkdir {nombre_de_la_carpeta}
$ mkdir mi_carpeta
~~~

## 3. touch
Con este comando puedes crear nuevos archivos en el directorio actual.

~~~
$ touch mi_archivo.txt
$ ls
mi_archivo.txt
~~~

## 4. ls
Este comando lista los archivos y directorios de la carpeta actual.

~~~
$ ls
mi_archivo.txt
mi_carpeta
~~~

Si quieres mostrar elementos ocultos, usa el flag -a.

~~~
$ ls -a
.soy_un_archivo_oculto
mi_archivo.txt
mi_carpeta
~~~

Para listar el contenido detallado usa el flag -l

~~~
$ ls -l
-rw-rw-r-- 1 alejandro alejandro    0 oct 22 16:46 mi_archivo.txt
drwxrwxr-x 2 alejandro alejandro 4096 oct 22 16:42 mi_carpeta
~~~

## 5. cd
El comando cd (change directory) permite moverse entre directorios del sistema.

~~~
cd {ruta\_absoluta\_o\_relativa}
~~~

Puedes cambiar de directorio especificando la ruta absoluta desde el directorio raíz o relativa desde tu ubicación actual, en Linux el directorio actual se indica con el signo .

Los siguientes tres comandos realizan la misma acción para moverte al directorio mi\_carpeta

~~~
$ pwd
/home/alejandro/EDteam

$ cd /home/alejandro/EDteam/mi_carpeta
$ cd ./mi_carpeta
$ cd mi_carpeta
~~~

Para regresar al directorio anterior usa el comando cd -

~~~
$ pwd
/home/alejandro/EDteam/mi_carpeta

$ cd -

$ pwd
/home/alejandro/EDteam
~~~

Para moverte un directorio por encima de tu posición actual puedes usar el comando cd .., o una secuencia de .. para ir subiendo por la estructura de directorios. Por ejemplo para ir a la carpeta home desde nuestra ubicación actual EDteam usaremos:

~~~
$ pwd
/home/alejandro/EDteam
$ cd ../..
$ pwd
/home 
~~~

## 6. mv
El comando mv (Move) mueve directorios o archivos de una ubicación a otra. Su sintaxis es: mv {ubicación\_actual} {nueva\_ubicación}

~~~
$ mv mi_archivo.txt ./mi_carpeta/mi_archivo.txt
~~~

También puedes renombrar archivos y carpetas con este mismo comando: mv {nombre\_actual} {nombre\_nuevo}

~~~
$ mv mi_archivo.txt usuarios.txt
$ mv mi_carpeta cursos
~~~

## 7. cp
El comando cp (Copy) copia archivos o directorios. Su sintaxis es cp {origen} {destino}

~~~
$ cp usuarios.txt usuarios_copia.txt
~~~

Para copiar directorios agrega la opción -r.

~~~
$ cp -r cursos/ cursos_copia/
~~~

## 8. rm y rmdir
El comando rm (Remove) elimina archivos. Su sintaxis es rm {nombre\_del\_archivo}
El comando rmdir (Remove directory) elimina carpetas vacías. Su sintaxis es: rmdir {nombre\_carpeta}

~~~
$ rmdir carpeta_vacia/
~~~

Para eliminar directorios no vacíos usa el comando rm con la opción -r

~~~
$ rm -r cursos_copia/ 
~~~

## 9. cat
El comando cat te permite leer el contenido de archivos.

~~~
$ cat notas.txt
~~~

Estas son las notas de mi curso
Fin de las notas de mi curso
Puedes mostrar las lineas del archivo con la opción -n.

~~~
$ cat -n notas.txt
~~~

1 Estas son las notas de mi curso
2 Fin de las notas de mi curso

## 10. find
Con el comando find y la opción -iname puedes encontrar archivos. La sintaxis es: find {donde\_buscar} -iname {archivo\_a\_buscar}

~~~
$ find . -iname "usuarios.txt"
./cursos/usuarios.txt
~~~