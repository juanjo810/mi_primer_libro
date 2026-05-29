# Sesion 7. Registros

La sesion construye registros a partir de biestables y presenta una herramienta esencial de depuracion: los cronogramas con GTKWave.

```{admonition} Objetivos de aprendizaje
:class: tip

- Un registro almacena varios bits distribuidos en biestables.
- Los registros SISO desplazan informacion serie a serie.
- Los registros SIPO reciben en serie y entregan en paralelo.
```

## Conceptos clave

- Un registro almacena varios bits distribuidos en biestables.
- Los registros SISO desplazan informacion serie a serie.
- Los registros SIPO reciben en serie y entregan en paralelo.
- `$dumpfile` y `$dumpvars` generan ficheros de ondas para inspeccionar senales.
- Los retardos reales o simulados pueden explicar comportamientos inesperados.

## Practica guiada

1. Construye un biestable D a partir de los bloques ya conocidos; usa la {numref}`fig-verilog-07-d` para verificar entradas y salida.
2. Usa varios biestables para formar un registro SISO; sigue la conexion de la {numref}`fig-verilog-07-siso`.
3. Genera un fichero de ondas y abrelo con GTKWave; compara la ventana esperada con la {numref}`fig-verilog-07-gtkwave`.
4. Modifica el registro para obtener una salida paralela SIPO; usa la {numref}`fig-verilog-07-sipo` y, para la ampliacion, la {numref}`fig-verilog-07-pisiso`.

## Indice teoria-practica-figuras

Usa esta tabla como mapa rapido: cuando un ejercicio mencione una figura, esa figura forma parte del enunciado y debe consultarse antes de escribir el codigo.

| Bloque de teoria | Ejercicios relacionados | Figuras que se deben consultar |
|---|---|---|
| Biestable D | Ejercicio 1 | {numref}`fig-verilog-07-d` |
| Registro SISO | Ejercicio 2 | {numref}`fig-verilog-07-siso` |
| Cronogramas | Ejercicio 3 | {numref}`fig-verilog-07-gtkwave` |
| Registros SIPO y carga paralela | Ejercicio 4 | {numref}`fig-verilog-07-sipo`, {numref}`fig-verilog-07-pisiso` |

## Figuras de referencia
Las figuras siguientes recogen los esquemas y tablas que conviene tener a mano mientras se resuelven los ejercicios de la sesion.

La {numref}`fig-verilog-07-d` sirve como referencia para: biestable D.

```{figure} ../../_static/verilog/sesion_07/d.png
---
name: fig-verilog-07-d
alt: Biestable D.
width: 85%
align: center
---
Biestable D.
```

La {numref}`fig-verilog-07-siso` sirve como referencia para: registro SISO.

```{figure} ../../_static/verilog/sesion_07/siso.png
---
name: fig-verilog-07-siso
alt: Registro SISO.
width: 85%
align: center
---
Registro SISO.
```

La {numref}`fig-verilog-07-gtkwave` sirve como referencia para: visualizacion de senales con GTKWave.

```{figure} ../../_static/verilog/sesion_07/gtkwave.png
---
name: fig-verilog-07-gtkwave
alt: Visualizacion de senales con GTKWave.
width: 85%
align: center
---
Visualizacion de senales con GTKWave.
```

La {numref}`fig-verilog-07-sipo` sirve como referencia para: registro SIPO.

```{figure} ../../_static/verilog/sesion_07/sipo.png
---
name: fig-verilog-07-sipo
alt: Registro SIPO.
width: 85%
align: center
---
Registro SIPO.
```

La {numref}`fig-verilog-07-pisiso` sirve como referencia para: registro con carga paralela y desplazamiento serie.

```{figure} ../../_static/verilog/sesion_07/pisiso.png
---
name: fig-verilog-07-pisiso
alt: Registro con carga paralela y desplazamiento serie.
width: 85%
align: center
---
Registro con carga paralela y desplazamiento serie.
```

## Cierre

Antes de pasar a la sesion siguiente, guarda el fichero Verilog de cada ejercicio y anota dos cosas: que esperabas obtener y que imprimio realmente la simulacion. Esa comparacion es la forma mas rapida de localizar errores.

## Fuente original

Contenido redactado y ampliado a partir de la presentacion de clase y de la pagina de referencia: <http://avellano.fis.usal.es/~compi/sesion7.htm>.
