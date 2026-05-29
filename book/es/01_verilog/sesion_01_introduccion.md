# Sesion 1. Introduccion a Verilog

Esta sesion presenta Verilog como lenguaje de descripcion de hardware y prepara el entorno minimo para compilar y simular ejemplos sencillos. El objetivo no es escribir software convencional, sino describir circuitos y observar su comportamiento.

```{admonition} Objetivos de aprendizaje
:class: tip

- Verilog es un HDL: describe hardware, no solo una secuencia de instrucciones.
- El flujo basico de trabajo es escribir un fichero `.v`, compilarlo y ejecutar la simulacion.
- Los modulos delimitan el diseno; `initial` permite definir una secuencia de pruebas.
```

## Conceptos clave

- Verilog es un HDL: describe hardware, no solo una secuencia de instrucciones.
- El flujo basico de trabajo es escribir un fichero `.v`, compilarlo y ejecutar la simulacion.
- Los modulos delimitan el diseno; `initial` permite definir una secuencia de pruebas.
- Los registros (`reg`) almacenan valores en la simulacion y los cables (`wire`) conectan senales.
- Los formatos de `$display` ayudan a comprobar valores en binario, octal, decimal o hexadecimal.

## Practica guiada

1. Crea un directorio de trabajo y guarda en el un fichero `hello.v`.
2. Compila el fichero con `iverilog` y ejecuta la salida generada.
3. Modifica el ejemplo para imprimir un entero en decimal, binario y hexadecimal; compara tu salida con la {numref}`fig-verilog-01-ej-1-9`.
4. Declara un registro de 16 bits y observa que ocurre al asignar valores mayores que su capacidad; usa la {numref}`fig-verilog-01-ej-1-9-comentado` para localizar que parte del codigo produce cada salida.

## Indice teoria-practica-figuras

Usa esta tabla como mapa rapido: cuando un ejercicio mencione una figura, esa figura forma parte del enunciado y debe consultarse antes de escribir el codigo.

| Bloque de teoria | Ejercicios relacionados | Figuras que se deben consultar |
|---|---|---|
| Formato de salida y conversion de bases | Ejercicios 3 y 4 | {numref}`fig-verilog-01-ej-1-9`, {numref}`fig-verilog-01-ej-1-9-comentado` |

## Figuras de referencia
Las figuras siguientes recogen los esquemas y tablas que conviene tener a mano mientras se resuelven los ejercicios de la sesion.

La {numref}`fig-verilog-01-ej-1-9` sirve como referencia para: ejemplo de salida esperada para una practica inicial de conversion y visualizacion de datos.

```{figure} ../../_static/verilog/sesion_01/ej_1_9.png
---
name: fig-verilog-01-ej-1-9
alt: Ejemplo de salida esperada para una practica inicial de conversion y visualizacion de datos.
width: 85%
align: center
---
Ejemplo de salida esperada para una practica inicial de conversion y visualizacion de datos.
```

La {numref}`fig-verilog-01-ej-1-9-comentado` sirve como referencia para: version comentada del mismo ejemplo, util para localizar cada instruccion en el codigo.

```{figure} ../../_static/verilog/sesion_01/ej_1_9_comentado.png
---
name: fig-verilog-01-ej-1-9-comentado
alt: Version comentada del mismo ejemplo, util para localizar cada instruccion en el codigo.
width: 85%
align: center
---
Version comentada del mismo ejemplo, util para localizar cada instruccion en el codigo.
```

## Cierre

Antes de pasar a la sesion siguiente, guarda el fichero Verilog de cada ejercicio y anota dos cosas: que esperabas obtener y que imprimio realmente la simulacion. Esa comparacion es la forma mas rapida de localizar errores.

## Fuente original

Contenido redactado y ampliado a partir de la presentacion de clase y de la pagina de referencia: <http://avellano.fis.usal.es/~compi/sesion1.htm>.
