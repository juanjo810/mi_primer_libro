# Sesion 4. Modulos

Esta sesion introduce el diseno modular. Un modulo en Verilog encapsula entradas, salidas y comportamiento, de forma parecida a una caja reutilizable.

```{admonition} Objetivos de aprendizaje
:class: tip

- Un modulo debe tener una interfaz clara: `input`, `output` e `inout`.
- La jerarquia permite construir sistemas grandes a partir de modulos pequenos.
- Las puertas logicas pueden verse como modulos predefinidos del lenguaje.
```

## Conceptos clave

- Un modulo debe tener una interfaz clara: `input`, `output` e `inout`.
- La jerarquia permite construir sistemas grandes a partir de modulos pequenos.
- Las puertas logicas pueden verse como modulos predefinidos del lenguaje.
- Un comparador de un bit es un buen primer ejemplo de modulo reutilizable.
- Los codificadores muestran como cambia el circuito cuando se introduce prioridad.

## Practica guiada

1. Define la interfaz de un comparador de un bit; identifica entradas y salidas en la {numref}`fig-verilog-04-compar1`.
2. Implementa el comparador con puertas NOT, AND y NOR; sigue la estructura interna de la {numref}`fig-verilog-04-compar11`.
3. Crea un modulo de prueba que recorra todas las entradas; compara tu planteamiento con la {numref}`fig-verilog-04-testcomp1`.
4. Usa dos comparadores de un bit para construir un comparador de dos bits; toma como referencia la jerarquia de la {numref}`fig-verilog-04-comp2`.

## Indice teoria-practica-figuras

Usa esta tabla como mapa rapido: cuando un ejercicio mencione una figura, esa figura forma parte del enunciado y debe consultarse antes de escribir el codigo.

| Bloque de teoria | Ejercicios relacionados | Figuras que se deben consultar |
|---|---|---|
| Interfaz de modulo | Ejercicio 1 | {numref}`fig-verilog-04-modulo`, {numref}`fig-verilog-04-compar1` |
| Circuito interno del comparador | Ejercicio 2 | {numref}`fig-verilog-04-compar11` |
| Modulo de comprobacion | Ejercicio 3 | {numref}`fig-verilog-04-testcomp1` |
| Jerarquia y codificadores | Ejercicio 4 y ampliaciones | {numref}`fig-verilog-04-comp2`, {numref}`fig-verilog-04-priocod`, {numref}`fig-verilog-04-and4` |

## Figuras de referencia
Las figuras siguientes recogen los esquemas y tablas que conviene tener a mano mientras se resuelven los ejercicios de la sesion.

La {numref}`fig-verilog-04-modulo` sirve como referencia para: esquema general de un modulo con puertos.

```{figure} ../../_static/verilog/sesion_04/mOdulo.png
---
name: fig-verilog-04-modulo
alt: Esquema general de un modulo con puertos.
width: 85%
align: center
---
Esquema general de un modulo con puertos.
```

La {numref}`fig-verilog-04-compar1` sirve como referencia para: comparador de un bit.

```{figure} ../../_static/verilog/sesion_04/compar1.png
---
name: fig-verilog-04-compar1
alt: Comparador de un bit.
width: 85%
align: center
---
Comparador de un bit.
```

La {numref}`fig-verilog-04-compar11` sirve como referencia para: implementacion interna del comparador de un bit.

```{figure} ../../_static/verilog/sesion_04/compar11.png
---
name: fig-verilog-04-compar11
alt: Implementacion interna del comparador de un bit.
width: 85%
align: center
---
Implementacion interna del comparador de un bit.
```

La {numref}`fig-verilog-04-testcomp1` sirve como referencia para: modulo de comprobacion del comparador.

```{figure} ../../_static/verilog/sesion_04/TestComp1.png
---
name: fig-verilog-04-testcomp1
alt: Modulo de comprobacion del comparador.
width: 85%
align: center
---
Modulo de comprobacion del comparador.
```

La {numref}`fig-verilog-04-comp2` sirve como referencia para: comparador de dos bits construido jerarquicamente.

```{figure} ../../_static/verilog/sesion_04/comp2.png
---
name: fig-verilog-04-comp2
alt: Comparador de dos bits construido jerarquicamente.
width: 85%
align: center
---
Comparador de dos bits construido jerarquicamente.
```

La {numref}`fig-verilog-04-priocod` sirve como referencia para: codificador con prioridad.

```{figure} ../../_static/verilog/sesion_04/priocod.png
---
name: fig-verilog-04-priocod
alt: Codificador con prioridad.
width: 85%
align: center
---
Codificador con prioridad.
```

La {numref}`fig-verilog-04-and4` sirve como referencia para: puerta AND de cuatro entradas.

```{figure} ../../_static/verilog/sesion_04/and4.png
---
name: fig-verilog-04-and4
alt: Puerta AND de cuatro entradas.
width: 85%
align: center
---
Puerta AND de cuatro entradas.
```

## Cierre

Antes de pasar a la sesion siguiente, guarda el fichero Verilog de cada ejercicio y anota dos cosas: que esperabas obtener y que imprimio realmente la simulacion. Esa comparacion es la forma mas rapida de localizar errores.

## Fuente original

Contenido redactado y ampliado a partir de la presentacion de clase y de la pagina de referencia: <http://avellano.fis.usal.es/~compi/sesion4.htm>.
