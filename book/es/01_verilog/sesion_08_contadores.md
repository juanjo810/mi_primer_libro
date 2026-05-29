# Sesion 8. Contadores

Esta sesion usa biestables para construir contadores y analizar transiciones de estado. El punto importante es distinguir entre comportamiento ideal, retardos y estados transitorios.

```{admonition} Objetivos de aprendizaje
:class: tip

- Un contador cambia de estado al ritmo de una senal de reloj.
- La cuenta puede ser ascendente o descendente mediante una linea de modo.
- HOLD permite congelar el estado cuando se necesita cambiar de modo sin saltos.
```

## Conceptos clave

- Un contador cambia de estado al ritmo de una senal de reloj.
- La cuenta puede ser ascendente o descendente mediante una linea de modo.
- HOLD permite congelar el estado cuando se necesita cambiar de modo sin saltos.
- Los contadores asincronos pueden pasar por estados transitorios durante la propagacion.
- Los diagramas de transicion resumen el comportamiento secuencial del circuito.

## Practica guiada

1. Programa un contador ascendente/descendente de cuatro bits; usa la {numref}`fig-verilog-08-contador` para definir entradas, salidas y modo de cuenta.
2. Observa que ocurre al cambiar de modo sin limpiar el contador; explica los estados transitorios con ayuda de la {numref}`fig-verilog-08-analisis`.
3. Anade PRESET, CLEAR y HOLD para controlar mejor las transiciones; compara tu diseno con la {numref}`fig-verilog-08-contsinc` y la {numref}`fig-verilog-08-cont01`.
4. Analiza un contador de cuenta arbitraria y dibuja su diagrama de estados; usa la {numref}`fig-verilog-08-transis`, la {numref}`fig-verilog-08-jkarn` y la {numref}`fig-verilog-08-contarb`.

## Indice teoria-practica-figuras

Usa esta tabla como mapa rapido: cuando un ejercicio mencione una figura, esa figura forma parte del enunciado y debe consultarse antes de escribir el codigo.

| Bloque de teoria | Ejercicios relacionados | Figuras que se deben consultar |
|---|---|---|
| Cuenta ascendente/descendente | Ejercicios 1 y 2 | {numref}`fig-verilog-08-contador`, {numref}`fig-verilog-08-analisis` |
| Control de transiciones | Ejercicio 3 | {numref}`fig-verilog-08-10a0`, {numref}`fig-verilog-08-contsinc`, {numref}`fig-verilog-08-cont01` |
| Estados y biestables JK | Ejercicio 4 | {numref}`fig-verilog-08-transjk`, {numref}`fig-verilog-08-transis`, {numref}`fig-verilog-08-jkarn`, {numref}`fig-verilog-08-contarb` |

## Figuras de referencia
Las figuras siguientes recogen los esquemas y tablas que conviene tener a mano mientras se resuelven los ejercicios de la sesion.

La {numref}`fig-verilog-08-contador` sirve como referencia para: contador con seleccion de cuenta ascendente o descendente.

```{figure} ../../_static/verilog/sesion_08/contador.png
---
name: fig-verilog-08-contador
alt: Contador con seleccion de cuenta ascendente o descendente.
width: 85%
align: center
---
Contador con seleccion de cuenta ascendente o descendente.
```

La {numref}`fig-verilog-08-10a0` sirve como referencia para: contador de 10 a 0.

```{figure} ../../_static/verilog/sesion_08/10a0.png
---
name: fig-verilog-08-10a0
alt: Contador de 10 a 0.
width: 85%
align: center
---
Contador de 10 a 0.
```

La {numref}`fig-verilog-08-contsinc` sirve como referencia para: contador sincrono.

```{figure} ../../_static/verilog/sesion_08/contsinc.png
---
name: fig-verilog-08-contsinc
alt: Contador sincrono.
width: 85%
align: center
---
Contador sincrono.
```

La {numref}`fig-verilog-08-analisis` sirve como referencia para: analisis de estados y transiciones.

```{figure} ../../_static/verilog/sesion_08/analisis.png
---
name: fig-verilog-08-analisis
alt: Analisis de estados y transiciones.
width: 85%
align: center
---
Analisis de estados y transiciones.
```

La {numref}`fig-verilog-08-cont01` sirve como referencia para: circuito contador auxiliar.

```{figure} ../../_static/verilog/sesion_08/cont01.png
---
name: fig-verilog-08-cont01
alt: Circuito contador auxiliar.
width: 85%
align: center
---
Circuito contador auxiliar.
```

La {numref}`fig-verilog-08-transjk` sirve como referencia para: transiciones de un biestable JK.

```{figure} ../../_static/verilog/sesion_08/transJK.png
---
name: fig-verilog-08-transjk
alt: Transiciones de un biestable JK.
width: 85%
align: center
---
Transiciones de un biestable JK.
```

La {numref}`fig-verilog-08-transis` sirve como referencia para: diagrama de transicion de estados.

```{figure} ../../_static/verilog/sesion_08/transis.png
---
name: fig-verilog-08-transis
alt: Diagrama de transicion de estados.
width: 85%
align: center
---
Diagrama de transicion de estados.
```

La {numref}`fig-verilog-08-jkarn` sirve como referencia para: mapa de Karnaugh para entradas JK.

```{figure} ../../_static/verilog/sesion_08/jkarn.png
---
name: fig-verilog-08-jkarn
alt: Mapa de Karnaugh para entradas JK.
width: 85%
align: center
---
Mapa de Karnaugh para entradas JK.
```

La {numref}`fig-verilog-08-contarb` sirve como referencia para: contador de cuenta arbitraria.

```{figure} ../../_static/verilog/sesion_08/contarb.png
---
name: fig-verilog-08-contarb
alt: Contador de cuenta arbitraria.
width: 85%
align: center
---
Contador de cuenta arbitraria.
```

## Cierre

Antes de pasar a la sesion siguiente, guarda el fichero Verilog de cada ejercicio y anota dos cosas: que esperabas obtener y que imprimio realmente la simulacion. Esa comparacion es la forma mas rapida de localizar errores.

## Fuente original

Contenido redactado y ampliado a partir de la presentacion de clase y de la pagina de referencia: <http://avellano.fis.usal.es/~compi/sesion8.htm>.
