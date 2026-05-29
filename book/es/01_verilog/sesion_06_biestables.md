# Sesion 6. Biestables

Esta sesion pasa de la logica combinacional a la memoria. Los biestables mantienen estado y obligan a pensar en reloj, flancos, entradas asincronas y retardos.

```{admonition} Objetivos de aprendizaje
:class: tip

- Un biestable RS puede construirse con dos puertas NOR realimentadas.
- Las asignaciones bloqueantes y no bloqueantes no producen siempre el mismo efecto temporal.
- Un reloj puede generarse con un bloque `always` que cambia periodicamente una senal.
```

## Conceptos clave

- Un biestable RS puede construirse con dos puertas NOR realimentadas.
- Las asignaciones bloqueantes y no bloqueantes no producen siempre el mismo efecto temporal.
- Un reloj puede generarse con un bloque `always` que cambia periodicamente una senal.
- Los detectores de flanco convierten una condicion de nivel en un pulso breve.
- PRESET y CLEAR suelen actuar de forma asincrona y tienen prioridad sobre el reloj.

## Practica guiada

1. Programa un biestable RS y prueba la bateria de entradas propuesta; consulta la {numref}`fig-verilog-06-rs` y contrasta los resultados con la {numref}`fig-verilog-06-rstabla`.
2. Sustituye algunas asignaciones por no bloqueantes y observa las diferencias cerca de los estados invalidos indicados en la {numref}`fig-verilog-06-rstabla`.
3. Anade una entrada de reloj activa por nivel; usa la {numref}`fig-verilog-06-rsc` y la {numref}`fig-verilog-06-rsctabla` para comprobar cuando debe cambiar la salida.
4. Construye una version activa por flanco y despues un biestable JK con PRESET y CLEAR; toma como guia la {numref}`fig-verilog-06-det`, la {numref}`fig-verilog-06-jk` y la {numref}`fig-verilog-06-jktabla`.

## Indice teoria-practica-figuras

Usa esta tabla como mapa rapido: cuando un ejercicio mencione una figura, esa figura forma parte del enunciado y debe consultarse antes de escribir el codigo.

| Bloque de teoria | Ejercicios relacionados | Figuras que se deben consultar |
|---|---|---|
| Biestable RS | Ejercicios 1 y 2 | {numref}`fig-verilog-06-rs`, {numref}`fig-verilog-06-rstabla` |
| Reloj por nivel | Ejercicio 3 | {numref}`fig-verilog-06-rsc`, {numref}`fig-verilog-06-rsctabla` |
| Flancos y JK | Ejercicio 4 | {numref}`fig-verilog-06-det`, {numref}`fig-verilog-06-jk`, {numref}`fig-verilog-06-jktabla` |

## Figuras de referencia
Las figuras siguientes recogen los esquemas y tablas que conviene tener a mano mientras se resuelven los ejercicios de la sesion.

La {numref}`fig-verilog-06-rs` sirve como referencia para: biestable RS con puertas NOR.

```{figure} ../../_static/verilog/sesion_06/rs.png
---
name: fig-verilog-06-rs
alt: Biestable RS con puertas NOR.
width: 85%
align: center
---
Biestable RS con puertas NOR.
```

La {numref}`fig-verilog-06-rstabla` sirve como referencia para: tabla de funcionamiento del biestable RS.

```{figure} ../../_static/verilog/sesion_06/rstabla.png
---
name: fig-verilog-06-rstabla
alt: Tabla de funcionamiento del biestable RS.
width: 85%
align: center
---
Tabla de funcionamiento del biestable RS.
```

La {numref}`fig-verilog-06-rsc` sirve como referencia para: biestable RS con reloj.

```{figure} ../../_static/verilog/sesion_06/rsc.png
---
name: fig-verilog-06-rsc
alt: Biestable RS con reloj.
width: 85%
align: center
---
Biestable RS con reloj.
```

La {numref}`fig-verilog-06-rsctabla` sirve como referencia para: tabla del biestable RS controlado por reloj.

```{figure} ../../_static/verilog/sesion_06/rsctabla.png
---
name: fig-verilog-06-rsctabla
alt: Tabla del biestable RS controlado por reloj.
width: 85%
align: center
---
Tabla del biestable RS controlado por reloj.
```

La {numref}`fig-verilog-06-det` sirve como referencia para: detector de flanco.

```{figure} ../../_static/verilog/sesion_06/det.png
---
name: fig-verilog-06-det
alt: Detector de flanco.
width: 85%
align: center
---
Detector de flanco.
```

La {numref}`fig-verilog-06-jk` sirve como referencia para: biestable JK con entradas de control.

```{figure} ../../_static/verilog/sesion_06/jk.png
---
name: fig-verilog-06-jk
alt: Biestable JK con entradas de control.
width: 85%
align: center
---
Biestable JK con entradas de control.
```

La {numref}`fig-verilog-06-jktabla` sirve como referencia para: tabla de funcionamiento del biestable JK.

```{figure} ../../_static/verilog/sesion_06/jktabla.png
---
name: fig-verilog-06-jktabla
alt: Tabla de funcionamiento del biestable JK.
width: 85%
align: center
---
Tabla de funcionamiento del biestable JK.
```

## Cierre

Antes de pasar a la sesion siguiente, guarda el fichero Verilog de cada ejercicio y anota dos cosas: que esperabas obtener y que imprimio realmente la simulacion. Esa comparacion es la forma mas rapida de localizar errores.

## Fuente original

Contenido redactado y ampliado a partir de la presentacion de clase y de la pagina de referencia: <http://avellano.fis.usal.es/~compi/sesion6.htm>.
