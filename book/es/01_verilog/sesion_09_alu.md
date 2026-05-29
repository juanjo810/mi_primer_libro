# Sesion 9. ALU

La ultima sesion aplica el trabajo modular a una ALU 74181. Se practica la inclusion de ficheros y la combinacion de operaciones aritmeticas y logicas.

```{admonition} Objetivos de aprendizaje
:class: tip

- `include` permite insertar el contenido de otro fichero Verilog en el punto indicado.
- La ALU 74181 recibe lineas de seleccion que determinan la operacion.
- Las lineas de acarreo negadas requieren atencion al interpretar entradas y salidas.
```

## Conceptos clave

- `include` permite insertar el contenido de otro fichero Verilog en el punto indicado.
- La ALU 74181 recibe lineas de seleccion que determinan la operacion.
- Las lineas de acarreo negadas requieren atencion al interpretar entradas y salidas.
- Las operaciones compuestas se resuelven almacenando resultados intermedios.
- El modulo de prueba debe dejar claras las entradas, la operacion seleccionada y la salida esperada.

## Practica guiada

1. Incluye el fichero `74181.v` desde un modulo de prueba; identifica los puertos en la {numref}`fig-verilog-09-74181`.
2. Comprueba operaciones como `7+4`, `2+6+1`, AND, XOR y OR combinado con NOT/XNOR; selecciona las lineas de control con la {numref}`fig-verilog-09-74181t`.
3. Implementa multiplicaciones pequenas como sumas repetidas; usa de nuevo la {numref}`fig-verilog-09-74181t` para justificar cada paso intermedio.
4. Documenta cada seleccion de lineas de control para poder depurar errores; tu tabla debe referirse explicitamente a la {numref}`fig-verilog-09-74181` y a la {numref}`fig-verilog-09-74181t`.

## Indice teoria-practica-figuras

Usa esta tabla como mapa rapido: cuando un ejercicio mencione una figura, esa figura forma parte del enunciado y debe consultarse antes de escribir el codigo.

| Bloque de teoria | Ejercicios relacionados | Figuras que se deben consultar |
|---|---|---|
| Interfaz de la ALU | Ejercicio 1 | {numref}`fig-verilog-09-74181` |
| Seleccion de operaciones | Ejercicios 2 a 4 | {numref}`fig-verilog-09-74181t` |

## Figuras de referencia
Las figuras siguientes recogen los esquemas y tablas que conviene tener a mano mientras se resuelven los ejercicios de la sesion.

La {numref}`fig-verilog-09-74181` sirve como referencia para: esquema funcional de la ALU 74181.

```{figure} ../../_static/verilog/sesion_09/74181.png
---
name: fig-verilog-09-74181
alt: Esquema funcional de la ALU 74181.
width: 85%
align: center
---
Esquema funcional de la ALU 74181.
```

La {numref}`fig-verilog-09-74181t` sirve como referencia para: tabla de operaciones de la ALU 74181.

```{figure} ../../_static/verilog/sesion_09/74181t.png
---
name: fig-verilog-09-74181t
alt: Tabla de operaciones de la ALU 74181.
width: 85%
align: center
---
Tabla de operaciones de la ALU 74181.
```

## Cierre

Antes de pasar a la sesion siguiente, guarda el fichero Verilog de cada ejercicio y anota dos cosas: que esperabas obtener y que imprimio realmente la simulacion. Esa comparacion es la forma mas rapida de localizar errores.

## Fuente original

Contenido redactado y ampliado a partir de la presentacion de clase y de la pagina de referencia: <http://avellano.fis.usal.es/~compi/sesion9.htm>.
