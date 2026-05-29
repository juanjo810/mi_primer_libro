# Sesion 5. Encaminadores y sumadores

La sesion trabaja buses, buffers triestado, multiplexores y sumadores. El hilo conductor es controlar por donde circula una senal y como se propaga el acarreo.

```{admonition} Objetivos de aprendizaje
:class: tip

- Los buffers triestado permiten dejar una salida en alta impedancia.
- Cuando varias senales llegan al mismo cable, conviene usar tipos como `tri`, `tri0`, `tri1`, `wand` o `wor`.
- `assign` crea una conexion continua entre una expresion y un cable.
```

## Conceptos clave

- Los buffers triestado permiten dejar una salida en alta impedancia.
- Cuando varias senales llegan al mismo cable, conviene usar tipos como `tri`, `tri0`, `tri1`, `wand` o `wor`.
- `assign` crea una conexion continua entre una expresion y un cable.
- Los multiplexores seleccionan una entrada entre varias mediante lineas de control.
- Un sumador completo se puede construir a partir de semisumadores y puertas auxiliares.

## Practica guiada

1. Programa un transmisor/receptor de bus de un bit; usa la {numref}`fig-verilog-05-trans` y la {numref}`fig-verilog-05-transnombres` para nombrar las senales.
2. Construye un multiplexor 4x1 con salida habilitable y despues un 8x1; toma como referencia la {numref}`fig-verilog-05-mux8x1`.
3. Implementa un semisumador y un sumador completo; relaciona tu codigo con la {numref}`fig-verilog-05-semisuma` y la {numref}`fig-verilog-05-sumador1`.
4. Anade retardos y estima el tiempo seguro de estabilizacion en un sumador de cuatro bits; justifica el calculo con la {numref}`fig-verilog-05-propaga4` y compara con la alternativa de la {numref}`fig-verilog-05-anticipa`.

## Indice teoria-practica-figuras

Usa esta tabla como mapa rapido: cuando un ejercicio mencione una figura, esa figura forma parte del enunciado y debe consultarse antes de escribir el codigo.

| Bloque de teoria | Ejercicios relacionados | Figuras que se deben consultar |
|---|---|---|
| Triestado y buses | Ejercicio 1 | {numref}`fig-verilog-05-bufif1`, {numref}`fig-verilog-05-bufif0`, {numref}`fig-verilog-05-trans`, {numref}`fig-verilog-05-transnombres`, {numref}`fig-verilog-05-transtest` |
| Multiplexores | Ejercicio 2 | {numref}`fig-verilog-05-mux8x1`, {numref}`fig-verilog-05-h4` |
| Sumadores | Ejercicio 3 | {numref}`fig-verilog-05-semisuma`, {numref}`fig-verilog-05-sumador1` |
| Retardos y acarreo | Ejercicio 4 | {numref}`fig-verilog-05-propaga4`, {numref}`fig-verilog-05-anticipa` |

## Figuras de referencia
Las figuras siguientes recogen los esquemas y tablas que conviene tener a mano mientras se resuelven los ejercicios de la sesion.

La {numref}`fig-verilog-05-bufif1` sirve como referencia para: buffer triestado activo a nivel alto.

```{figure} ../../_static/verilog/sesion_05/bufif1.png
---
name: fig-verilog-05-bufif1
alt: Buffer triestado activo a nivel alto.
width: 85%
align: center
---
Buffer triestado activo a nivel alto.
```

La {numref}`fig-verilog-05-bufif0` sirve como referencia para: buffer triestado activo a nivel bajo.

```{figure} ../../_static/verilog/sesion_05/bufif0.png
---
name: fig-verilog-05-bufif0
alt: Buffer triestado activo a nivel bajo.
width: 85%
align: center
---
Buffer triestado activo a nivel bajo.
```

La {numref}`fig-verilog-05-trans` sirve como referencia para: transmisor/receptor de bus de un bit.

```{figure} ../../_static/verilog/sesion_05/trans.png
---
name: fig-verilog-05-trans
alt: Transmisor/receptor de bus de un bit.
width: 85%
align: center
---
Transmisor/receptor de bus de un bit.
```

La {numref}`fig-verilog-05-transnombres` sirve como referencia para: nombres de senales auxiliares en el transceptor.

```{figure} ../../_static/verilog/sesion_05/transNombres.png
---
name: fig-verilog-05-transnombres
alt: Nombres de senales auxiliares en el transceptor.
width: 85%
align: center
---
Nombres de senales auxiliares en el transceptor.
```

La {numref}`fig-verilog-05-transtest` sirve como referencia para: modulo de comprobacion del transceptor.

```{figure} ../../_static/verilog/sesion_05/transTest.png
---
name: fig-verilog-05-transtest
alt: Modulo de comprobacion del transceptor.
width: 85%
align: center
---
Modulo de comprobacion del transceptor.
```

La {numref}`fig-verilog-05-mux8x1` sirve como referencia para: multiplexor 8x1 construido a partir de multiplexores menores.

```{figure} ../../_static/verilog/sesion_05/mux8x1.png
---
name: fig-verilog-05-mux8x1
alt: Multiplexor 8x1 construido a partir de multiplexores menores.
width: 85%
align: center
---
Multiplexor 8x1 construido a partir de multiplexores menores.
```

La {numref}`fig-verilog-05-h4` sirve como referencia para: estructura auxiliar para seleccion de senales.

```{figure} ../../_static/verilog/sesion_05/h4.png
---
name: fig-verilog-05-h4
alt: Estructura auxiliar para seleccion de senales.
width: 85%
align: center
---
Estructura auxiliar para seleccion de senales.
```

La {numref}`fig-verilog-05-semisuma` sirve como referencia para: semisumador.

```{figure} ../../_static/verilog/sesion_05/semisuma.png
---
name: fig-verilog-05-semisuma
alt: Semisumador.
width: 85%
align: center
---
Semisumador.
```

La {numref}`fig-verilog-05-sumador1` sirve como referencia para: sumador completo de un bit.

```{figure} ../../_static/verilog/sesion_05/sumador1.png
---
name: fig-verilog-05-sumador1
alt: Sumador completo de un bit.
width: 85%
align: center
---
Sumador completo de un bit.
```

La {numref}`fig-verilog-05-propaga4` sirve como referencia para: sumador de cuatro bits con propagacion de acarreo.

```{figure} ../../_static/verilog/sesion_05/propaga4.png
---
name: fig-verilog-05-propaga4
alt: Sumador de cuatro bits con propagacion de acarreo.
width: 85%
align: center
---
Sumador de cuatro bits con propagacion de acarreo.
```

La {numref}`fig-verilog-05-anticipa` sirve como referencia para: sumador con anticipacion de acarreo.

```{figure} ../../_static/verilog/sesion_05/anticipa.png
---
name: fig-verilog-05-anticipa
alt: Sumador con anticipacion de acarreo.
width: 85%
align: center
---
Sumador con anticipacion de acarreo.
```

## Cierre

Antes de pasar a la sesion siguiente, guarda el fichero Verilog de cada ejercicio y anota dos cosas: que esperabas obtener y que imprimio realmente la simulacion. Esa comparacion es la forma mas rapida de localizar errores.

## Fuente original

Contenido redactado y ampliado a partir de la presentacion de clase y de la pagina de referencia: <http://avellano.fis.usal.es/~compi/sesion5.htm>.
