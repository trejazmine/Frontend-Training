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

# 3. Working wit Git
# 4. Graded Assessment
