# Sesion 0. Terminal de Ubuntu para Verilog

Esta sesion sirve para perder el miedo a la terminal. Antes de escribir circuitos en Verilog conviene saber moverse por carpetas, localizar archivos y ejecutar las herramientas que compilan y simulan nuestros disenos.

```{admonition} Objetivos de aprendizaje
:class: tip

- Abrir una terminal de Ubuntu y saber en que carpeta estamos.
- Movernos por el sistema de archivos con `pwd`, `ls` y `cd`.
- Crear una carpeta de trabajo y organizar ficheros Verilog.
- Crear un archivo sencillo con `gedit` y mostrarlo desde la terminal.
- Preparar el primer comando de compilacion con `iverilog`.
```

## La terminal como mesa de trabajo

Una terminal es una ventana donde escribimos ordenes de texto. Para este curso la usaremos como una mesa de trabajo: entramos en una carpeta, miramos que archivos hay, abrimos un editor y ejecutamos comandos sencillos.

En Ubuntu puedes abrirla con `Ctrl` + `Alt` + `T`, o buscandola como **Terminal** en el menu de aplicaciones.

## Donde estoy: `pwd`

El comando `pwd` muestra la ruta de la carpeta actual.

```bash
pwd
```

Una salida posible es:

```text
/home/usuario
```

Esta ruta significa: estamos dentro de la carpeta personal del usuario. Si la terminal fuera un navegador de archivos, `pwd` seria mirar la barra de direccion.

## Que hay aqui: `ls`

El comando `ls` lista el contenido de la carpeta actual.

```bash
ls
```

Variantes utiles:

```bash
ls -l
ls -a
ls -lh
```

| Comando | Para que sirve |
|---|---|
| `ls` | Lista archivos y carpetas visibles. |
| `ls -l` | Muestra mas detalles: permisos, tamano y fecha. |
| `ls -a` | Incluye archivos ocultos, los que empiezan por punto. |
| `ls -lh` | Muestra tamanos mas legibles, por ejemplo `4K` o `2M`. |

## Cambiar de carpeta: `cd`

El comando `cd` cambia la carpeta actual.

```bash
cd Documentos
pwd
```

Para volver una carpeta hacia atras:

```bash
cd ..
```

Para ir directamente a tu carpeta personal:

```bash
cd
```

Para entrar en una ruta concreta:

```bash
cd ~/verilog/sesion_00
```

El simbolo `~` representa tu carpeta personal. En muchas instalaciones equivale a algo como `/home/usuario`.

## Crear y preparar una carpeta de practicas

Vamos a crear una carpeta para el curso y otra para esta sesion.

```bash
mkdir -p ~/verilog/sesion_00
cd ~/verilog/sesion_00
pwd
```

El comando `mkdir` crea carpetas. La opcion `-p` permite crear varias carpetas encadenadas si todavia no existen.

## Comprobar herramientas instaladas

Para compilar Verilog en Ubuntu usaremos principalmente:

- `iverilog`: compila el diseno y el banco de pruebas.

Comprueba si estan disponibles:

```bash
iverilog -V
```

Si Ubuntu responde con un mensaje de version, la herramienta esta instalada. Si responde `command not found`, falta instalarla.

````{admonition} Instalacion en Ubuntu
:class: note

Si trabajas en una maquina donde tienes permiso para instalar paquetes, puedes preparar las herramientas con:

```bash
sudo apt update
sudo apt install iverilog
```
````

## Crear un primer archivo de texto

Crea el archivo `hola.txt` con `gedit`:

```bash
gedit hola.txt
```

```{admonition} Otros editores en la terminal
:class: note

Ademas de `gedit`, existen editores que se abren dentro de la propia terminal, como `nano`, `pico` o `vim`. En esta sesion usaremos `gedit` porque permite empezar de forma visual y sencilla.
```

Escribe una sola palabra:

```text
hola
```

Guarda el archivo y cierra `gedit`.

Comprueba que el archivo existe:

```bash
ls -l
```

Muestra su contenido desde la terminal:

```bash
cat hola.txt
```

La salida esperada es:

```text
hola
```

## Compilar y ejecutar

Mas adelante escribiremos archivos Verilog. El ciclo sera muy parecido: estar en la carpeta correcta, listar los archivos, compilar y ejecutar el resultado.

Crea este archivo `saludo.v`:

```bash
gedit saludo.v
```

Contenido:

```verilog
module saludo;
  initial begin
    $display("Hola desde Verilog");
    $finish;
  end
endmodule
```

Compila el archivo con `iverilog`:

```bash
iverilog -o saludo saludo.v
```

Este comando lee `saludo.v` y crea un archivo ejecutable llamado `saludo`.

Ejecutalo con:

```bash
./saludo
```

La salida esperada es:

```text
Hola desde Verilog
```

## Patron de trabajo para las sesiones

En este curso repetiremos muchas veces la misma secuencia:

```bash
cd ~/verilog/sesion_00
ls
iverilog -o simulacion archivo.v
./simulacion
```

Cuando el ejemplo tenga un banco de pruebas, normalmente compilaremos dos archivos:

```bash
iverilog -o simulacion diseno.v testbench.v
./simulacion
```

## Comandos basicos de ayuda

| Comando | Uso habitual |
|---|---|
| `clear` | Limpia la pantalla de la terminal. |
| `history` | Muestra comandos usados anteriormente. |
| `man ls` | Abre el manual de `ls`. Se sale con `q`. |
| `cat archivo.txt` | Muestra el contenido de un archivo corto. |
| `cp origen.v copia.v` | Copia un archivo. |
| `mv viejo.v nuevo.v` | Renombra o mueve un archivo. |
| `rm archivo.txt` | Borra un archivo. Usalo con cuidado. |

## Errores frecuentes

| Mensaje o situacion | Que revisar |
|---|---|
| `command not found` | La herramienta no esta instalada o el nombre esta mal escrito. |
| `No such file or directory` | No estas en la carpeta correcta o el archivo no se llama asi. Usa `pwd` y `ls`. |
| `cat hola.txt` no muestra nada | El archivo esta vacio o no se guardo en `gedit`. |
| `./saludo` no funciona | Revisa que primero hayas compilado con `iverilog -o saludo saludo.v`. |

## Practica guiada

1. Abre una terminal de Ubuntu.
2. Crea la carpeta `~/verilog/sesion_00`.
3. Entra en esa carpeta y confirma la ruta con `pwd`.
4. Abre `gedit` desde la terminal con `gedit hola.txt`.
5. Escribe `hola`, guarda el archivo y cierra `gedit`.
6. Usa `ls` para comprobar que `hola.txt` aparece en la carpeta.
7. Usa `cat hola.txt` para mostrar su contenido.
8. Cambia el texto por `hola mundo`, guarda de nuevo y vuelve a mostrarlo con `cat hola.txt`.

## Cierre

Antes de pasar a la sesion 1, debes poder responder sin mirar apuntes: donde estoy (`pwd`), que archivos tengo (`ls`), como entro en una carpeta (`cd`), como abro un archivo con `gedit` y como muestro un archivo corto con `cat`.
