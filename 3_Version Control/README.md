# 1. Software collaboration
a. [Version Control Git terminology](https://d3c33hcgiwev3.cloudfront.net/SspDywPOSySKQ8sDzrskYA_e4f25a0bc3f44a89a282db515ce821e1_github-git-cheat-sheet.pdf?Expires=1706313600&Signature=j1XGIHWH-TU-S4HdLKHa~ATlW9fwh-inLKlFo8QOj4YJeVzFF-PKUWdkiqIsMo3tleBkGlPhf7GiJg6-vJzD1YQ-vLq900Fjc3HzFo3gmLVBbllUFArJk9-gc011AIj8FvGp2hVHsRzMsXkQ9ybvTIlGfIf2Jkbv2AfIKB9KJt4_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

1. CVCS (Centralizado):

Contiene un servidor y un cliente.
El servidor almacena el repositorio principal con el historial completo del código base.
Desarrolladores extraen el código del servidor a sus máquinas locales.
Las operaciones requieren conexión con el servidor.
Los cambios deben enviarse al servidor central para compartir.
2. DVCS (Distribuido):

Similar al modelo centralizado, pero cada usuario es esencialmente un servidor.
Al extraer código, cada usuario tiene el historial completo de cambios localmente.
No es necesario estar conectado al servidor para realizar acciones locales.
Permite a los usuarios trabajar sin conexión y ofrece mejor velocidad y rendimiento.
Ventajas y Desventajas:

CVCS: Fácil aprendizaje, más control de acceso, pero puede ser más lento debido a la necesidad de conexión constante al servidor.
DVCS: Mayor velocidad y rendimiento, funciona localmente, permite trabajar sin conexión.

> Ambos tipos de SCV tienen sus propias ventajas y desventajas. CVCS es considerado más fácil de aprender, mientras que DVCS ofrece mejor rendimiento y operación sin conexión. La elección depende de las necesidades específicas del equipo y el proyecto.

# 2. Command Line
## Tuberias

1. **Listar y Cambiar de Directorio:**
   - Comando `ls` muestra carpetas: `archivo` y `proyectos`.
   - `cd` para cambiar a `archivo`.
   - `ls` dentro de `archivo` revela `envios`.

2. **Explorar Contenido de una Carpeta:**
   - `cd envios` para ingresar a la carpeta.
   - `ls` muestra `Archivo1.txt` y `archivo2.txt`.

3. **Ver Contenido de un Archivo:**
   - `cat Archivo1.txt` muestra el contenido.

4. **Contar Palabras en un Archivo:**
   - Comando `wc -w Archivo1.txt` devuelve 181 palabras.

5. **Uso de Tuberías (Pipes):**
   - `ls | wc -l` cuenta archivos en el directorio (resultado: 2).
   - `cat Archivo1.txt | wc -w` cuenta palabras en Archivo1.txt.
   
6. **Tuberías con Múltiples Archivos:**
   - `cat Archivo1.txt archivo2.txt | wc -w` cuenta palabras en ambos archivos (resultado: 362).

> ***Observaciones:***
> - La tubería (`|`) permite pasar la salida de un comando como entrada a otro.
> - El comando `wc` con la bandera `-w` cuenta palabras.
> - Se pueden combinar comandos para realizar operaciones más complejas.

## Redirección en la Línea de Comandos

1. **Flujo de Trabajo Básico:**
   - Comandos Linux: Toman entrada y generan salida.
   - Entrada Estándar (STDIN): Representada por 0.
   - Salida Estándar (STDOUT): Representada por 1.
   - Error Estándar (STDERR): Representada por 2.

2. **Redirección de Entrada Estándar:**
   - Uso de `cat` para capturar entrada del usuario y guardarla en un archivo (ejemplo: `cat > input.txt`).

3. **Redirección de Salida Estándar:**
   - Redirigir la salida de un comando a un archivo (ejemplo: `ls -l > output.txt`).

4. **Manejo de Errores con Redirección:**
   - Redirección de errores (STDERR) al archivo (ejemplo: `ls -l /bin/usr > error.txt 2>&1`).
   - Manejar errores y salida estándar por separado (ejemplo: `ls -l /bin/ > salida_error.txt 2>&1`).

5. **Ejemplos Prácticos:**
   - Demostración de redirección de salida y error en casos de éxito y fallo.
   - Utilización de `less` para visualizar el contenido de archivos.

6. **Uso de Números de Descriptores de Archivos:**
   - 0: Entrada Estándar (STDIN).
   - 1: Salida Estándar (STDOUT).
   - 2: Error Estándar (STDERR).

7. **Tuberías (Pipes):**
   - Enviar salida de un comando como entrada a otro (`ls | wc -l`).
   - Combinar salida y error usando tuberías (`ls /bin/usr > salida_error.txt 2>&1`).

> ***Conclusión:***
> - La redirección permite controlar la entrada, salida y errores de los comandos.
> - Números de descriptores de archivos: 0 (entrada), 1 (salida), 2 (error).
> - Tuberías facilitan el flujo de datos entre comandos.

## Grep

1. **Introducción a Grep:**
   - **Grep:** Impresión global de expresiones regulares.
   - Utilizado para buscar en archivos y carpetas, así como en el contenido de archivos.

2. **Ejemplo Práctico:**
   - Ejecución del comando `ls -l` para ver el archivo `nombres.txt`.
   - Contenido de `nombres.txt`: Lista de nombres no ordenados alfabéticamente.

3. **Búsqueda Estándar con Grep:**
   - Búsqueda de nombres que comienzan con "Sam" mediante el comando `grep Sam nombres.txt`.
   - Grep distingue entre mayúsculas y minúsculas.

4. **Ignorar Diferencia entre Mayúsculas y Minúsculas:**
   - Utilización de la bandera `-i` para ignorar distinción de mayúsculas/minúsculas (`grep -i Sam nombres.txt`).

5. **Búsqueda de Coincidencia Exacta:**
   - Uso de la bandera `-w` para buscar una coincidencia exacta (`grep -w Sam nombres.txt`).

6. **Combinación de Comandos con Pipe:**
   - Búsqueda de archivos ejecutables en el directorio `/bin` usando `ls /bin`.
   - Uso de pipe (`|`) para filtrar resultados con Grep (ejemplo: `ls /bin | grep zip`).

7. **Refinamiento de Búsquedas:**
   - Aplicación de diferentes banderas para refinar resultados según coincidencia exacta, parcial, o ignorar distinción de mayúsculas/minúsculas.

> ***Conclusión:***
> - Grep es una herramienta poderosa para buscar patrones en archivos y directorios.
> - Se pueden utilizar diferentes banderas para adaptar las búsquedas según las necesidades.
> - La combinación de comandos con pipes permite realizar búsquedas más específicas.

# 3. Working wit Git
### Git show [document name]
Esto muestra los últimos cambios hecho en los últimos commit para poder ver si se puede revertir algún causado.

Cuando no le agregas un comentario a un commit, la consola te lo pide, al agregarlo, sale de esa parte con: esc+shift+zz
Lo que me abre es un editor de código “VIN” en el mundo de la línea de comandos.

### git diff [llave commit 1] [llave commit 2] 
Esto nos muestra las diferencias entre 2 versiones de documentos que hemos hecho cambios.

Staging: la memoria RAM. estado temporal de archivos que voy agregando, ahí voy poniendo la modificaciones antes del commit. Va entre directorio y repositorio.
Untracked: no mapeado (sin el git add)
Tracked: mapeado (con git add)

### ¿Qué es branch y cómo funciona el Merge en Git?
Branch (rama): Son líneas que se usan para hacer experimentos, cambios, solucionar conflictos o arreglar bugs. 
En algún punto del branch, uno lo puede unir o fusionar (merch) para recuperar los mejor de ambas versiones.

> NOTA:
> Ramas experimentos: Branch Development
> Rama de arreglo de bug: Hotfix

- Git reset [codigo de commit]  --hard (para que se cambie definitivo)
- Git reset [codigo de commit]  --soft (aun sigue en staging el cambio)

- Git log --stat muestra estadísticas sobre los cambios en cada confirmación, incluyendo qué archivos fueron modificados y cuántas líneas fueron agregadas o eliminadas en cada uno. (Muy específico)

- **Git checkout  [codigo de commit] [nombre de archivo]**: solo para chequear cómo era mi documento antes, pero si le hago un commit puede quedarse ahí como está [cuidado] (puedo aplicarlo para cuando hago cambios y no los he agregado al add y commit # GIT CHECKOUT [FILE NAME])

- git checkout master [file name]: esto es para regresar a su estado original luego de hacerle el checkout de tipo anterior.

"This is to revert to the original state after performing a 'checkout' of the same type as the previous one."

- **git reset HEAD:** El comando git reset saca archivos del área de staging sin borrarlos ni realizar otras acciones. Esto impide que los últimos cambios en estos archivos se envíen al último commit. Podemos incluirlos de nuevo en staging con git add si cambiamos de opinión.

Con este comando puedes cancelar los cambios que ya habías agregado, para que puedas revisarlos, modificarlos o deshacerlos antes de confirmarlos con un commit.

- git rm --cached: esto para eliminar un archivo del área de staging, solo se queda en el directorio del disco duro.

This is to remove a file from the staging area, leaving only the file in the hard disk directory.

- Git commit --amend -m "Name of the new commit name" Esto es para cambiar el nombre del último commit hecho por si nos equivocamos

- Git mv [file name] [new file name] esto es para cambiar de nombre algún archivo que tenga en mi directorio.

This is to change the file name that I had in my directory.

>NOTE:
> “-” in english is “hyphen”
> git commit --amend -m "Name of the new commit name"

- git reflog: muestra un registro detallado de las referencias de Git en tu repositorio local, incluyendo información sobre las ramas, las cabezas (HEAD), y otros puntos de referencia importantes. La palabra "reflog" proviene de "registro de referencia".

Show a detailist register of the git references in your local repository, including information from the branches, the heads and others points of main references.

- git shortlog : Indica que commits ha realizado un usuario, mostrando el usuario y el titulo de sus commits.

Indicates which commits it realized a user, showing the user and the title of the commit.

- git log --after=“2018-1-2” ,
- git log --after=“today” y
- git log --after=“2018-1-2” --before=“today” Commits para localizar por fechas.

- git log --author=“Name Author”
Commits realizados por autor que cumplan exactamente con el nombre.

- git branch [file new branch] esto se usa para crear una nueva rama, aquí solo hace copia del último commit que haya en la rama master.

this is used to create a new branch, here it only makes a copy of the last commit in the master branch.

- git checkout [branch name] esto sirve para moverse a la rama que estamos nombrando.

this is used to move to the named branch.

> NOTA:
> Siempre debo crear una llave pública y privada por cada computadora que use para mis repositorios remotos.


Para conectar mi repositorio local con un repositorio remoto, debo copiar este link:
***Ejemplo:*** [https://github.com/trejazmine/Frontend-Training.git](https://github.com/trejazmine/Frontend-Training.git)
para luego colocar este link en mi git con el siguiente código:
git remote add origin [link de repositorio]

Debido a la actualización, ahora la rama master es rama main. Para trabajar con ese nombre debo colocarse antes:

- git pull origin main: trae una copia del main remoto hacia el local.
- git push origin main: lleva una copia del main local para que se fusione con el remoto.


>NOTA:
>por si aparece esto:
>fatal: refusing to merge unrelated histories
>***¿QUÉ SIGNIFICA?*** Git indica que estás intentando fusionar dos historias (o líneas de tiempo) que Git considera no relacionadas. Este problema suele ocurrir cuando intentas realizar un git merge entre dos ramas que no comparten un ancestro común. Es decir, Git no puede automáticamente determinar cómo combinar las historias divergentes.

poner esto:
git pull origin main --allow-unrelated-histories
(Si te abre un ventana de git, para salir poner:
Esc + :q! + enter

>NOTA: 
>Siempre hacer primero un git pull y luego el git push, como buena práctica.

Buen flujo de trabajo de git:
Git pull →  add, commits → Git pull → git push

- git log --all: to show all commits at the time.
- git log --all --graph: te muestra de una manera visual las ramas o commits
- git log --all --graph --decorate --oneline: te muestra todo más comprimido

alias arbolito="git log --all --graph --decorate --oneline" ESTO ES PARA COLOCAR UN NOMBRE QUE YO QUIERO A CUALQUIER COMANDO DE GIT

### Tags
Este para añadir versiones de mi proyecto relacionadas a los commits que he hecho.
git tag -a [nombre de tag (v0.1)] -m “mensaje de tag” [código de tag] 

- Para mostrar todos mis tags: git tag
- Para mostrar más detalles: git show-ref –tags
- Para mandar mis tags para mi github: git push origin --tags

Ahora, con esto no se borra de github, lo vamos a borrar de manera especial.

git push origin :refs/tags/[nombre de tag]

### Manejo de ramas en github:

- git show-branch: esto para mostrar el historial de ramas.
- git show-branch --all: da más detalles de las historias de las ramas.

- gitk: un apoyo visual de las ramas y cambios.
