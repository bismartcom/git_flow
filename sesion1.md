# Sesion 1 Git Flow en Bismart

## Presentación de la formación (0 - 10)

El objetivo de la formación es integrar en los proyectos de Bismart, una manera de trabajar sobre el código, sea SQL, Databricks, Datafactory o programas en Python. Queda fuera de la formación los proyectos centrados en Power BI, ya que al ser ficheros binarios grandes (un .pbix son distintos ficheros compromidos y empaquetados bajo un solo fichero) no hemos definido en Bismart aún una manera práctica de trabajar. 

Con esto, pretendemos que todos los proyectos de bismart adapten esta forma de trabajar o variaciones más senzillas sobre ellas. 

## Objetivos de la sesion 1

* Aprender los comandos básicos en git: pull, push, merge, status, branch, checkout
* Aprender como funciona git bajo Visual Studio Code

----
## Conceptos básicos (10-50)

>Notas privadas: Joan.. abre el link con tu cuenta y les compartes el kahoot: https://create.kahoot.it/details/c9318539-166c-4623-a3b0-23eed7339c08


Si haceis la formación a vuestro paso, provad esta URL para autoexaminaros:

(el link saldrá al acabar la formación no antes!)

----
## Introduccion a git (50 - 80)

Tenemos powerpoint con una presentación básica sobre git:

[Abrir powerpoint](https://bismartbiss.sharepoint.com/:p:/r/Formacion/Documentos%20Formacion/FORMACI%C3%93N%20INTERNA%202019/Operaciones/Formaci%C3%B3n%20Repositorio%20Git/Introduccion%20GIT.pptx?d=wd8c23ca46ff84b609f3e013c436870dd&csf=1&web=1&e=iOWpCp) (necesitas usuario de Bismart) 

----

## Ejercicio 1: creacion de un propio repositorio

Git es un repositorio de código distribuído. En tu máquina puede funcionar sin necesidad de conectarte a ningú lugar especial ni disponer de ninguna cuenta de ningún tipo. 

Para ello vamos a hacer algunos ejercicios básicos:

1. Crear una carpeta en tu directorio donde tengas los proyectos, que **no** sea bajo una carpeta controlada por **onedrive**.

2. Ves a esa carpeta desde la terminal: puedes hacer click sobre la carpeta con el boton derecho y hacer click en "abrir con la terminal". O bien abre la consola, copia la ruta entera de tu carpeta y ejecuta: 

![](images/20230424171552.png)
```powershell
cd C:\Users\joan.teixido\apps\myGit
````

3. En esta carpeta vacía, ejecutamos "git init". En ese momento esta carpeta tendrá una carpeta oculta llamada .git

A partir de aquí, por defecto, todos los ficheros y carpetas incluídos bajo esta carpeta estarán "tracked" por git. 

4. Abrir el visual Studio Code en esta carpeta "myGit", con boton derecho sobre carpeta, o con la terminal escribiendo: 

```
code . 
```

5. Crear un fichero cualquiera con algún texto. 
6. Ejecutar ``` git add .  ``` para añadir todos los ficheros para preparar el commit 

7. y luego un git commit -m "MENSAJE_DEL_COMMIT", para hacer un commit con ese fichero (o los que hayámos añadido)

```
git commit -m "Añadido mi primer fichero al commit"
```

Si ahora ejecutamos por ejemplo, ```git log``` tendremos la lista de commits ejecutados de más nuevo a más viejo. Cada commit tiene un ID que lo identifica y continene los datos del cambio. 


8. Vamos a crear una rama:

``` 
git checkout -b mi_nueva_rama
```

Con el -b creamos la rama y movemos el HEAD a esa nueva rama.

9. Creamos otro fichero distinto y lo añadimos a un nuevo commit. 
10. Finalmente cambiamos de rama y volvemos a main con ```git checkout main```
11. Ahora ya no tenemos el nuevo fichero, ya que solo existe en la rama "mi_nueva_rama"

Ahora se trata de juntar las dos ramas:

```
git merge mi_nueva_rama
```

Como estamos en la rama "main" eso nos trae los cambios en "mi_nueva_rama" a main. 










