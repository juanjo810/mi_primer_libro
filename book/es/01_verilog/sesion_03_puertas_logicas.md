# Sesion 3. Puertas logicas

La sesion conecta las puertas logicas vistas en teoria con su instanciacion en Verilog. Tambien introduce los valores especiales `x` y `z`, importantes en simulacion digital.

```{admonition} Objetivos de aprendizaje
:class: tip

- Las puertas primitivas de Verilog se instancian indicando salida y entradas.
- Los valores `x` e `z` permiten representar incertidumbre y alta impedancia.
- Una tabla de verdad completa debe contemplar 0, 1, x y z cuando el ejercicio lo exige.
```

## Conceptos clave

- Las puertas primitivas de Verilog se instancian indicando salida y entradas.
- Los valores `x` e `z` permiten representar incertidumbre y alta impedancia.
- Una tabla de verdad completa debe contemplar 0, 1, x y z cuando el ejercicio lo exige.
- La interconexion de puertas permite construir funciones combinacionales mas complejas.
- Una misma funcion puede implementarse de varias formas, por ejemplo solo con puertas NAND.

## Practica guiada

1. Completa la tabla de verdad de AND con las 16 combinaciones de 0, 1, x y z; usa la {numref}`fig-verilog-03-and` y la {numref}`fig-verilog-03-andvar` como referencia.
2. Repite la comprobacion para OR, NAND, NOR, XOR, XNOR y BUFFER; consulta de la {numref}`fig-verilog-03-or` a la {numref}`fig-verilog-03-buf` segun la puerta que estes simulando.
3. Construye la funcion propuesta con puertas y verifica su tabla de verdad; usa la {numref}`fig-verilog-03-f2`, la {numref}`fig-verilog-03-f2var` y la {numref}`fig-verilog-03-tablaf2`.
4. Reimplementa la funcion usando solo NAND y compara las salidas; toma como guia la {numref}`fig-verilog-03-f3`, la {numref}`fig-verilog-03-f3for` y la {numref}`fig-verilog-03-f3nand`.

## Indice teoria-practica-figuras

Usa esta tabla como mapa rapido: cuando un ejercicio mencione una figura, esa figura forma parte del enunciado y debe consultarse antes de escribir el codigo.

| Bloque de teoria | Ejercicios relacionados | Figuras que se deben consultar |
|---|---|---|
| Puertas basicas | Ejercicios 1 y 2 | {numref}`fig-verilog-03-and`, {numref}`fig-verilog-03-andvar`, {numref}`fig-verilog-03-or`, {numref}`fig-verilog-03-not`, {numref}`fig-verilog-03-nand`, {numref}`fig-verilog-03-nor`, {numref}`fig-verilog-03-xor`, {numref}`fig-verilog-03-xnor`, {numref}`fig-verilog-03-buf` |
| Funcion combinacional f2 | Ejercicio 3 | {numref}`fig-verilog-03-f2`, {numref}`fig-verilog-03-f2var`, {numref}`fig-verilog-03-tablaf2` |
| Equivalencia con NAND | Ejercicio 4 | {numref}`fig-verilog-03-f3for`, {numref}`fig-verilog-03-f3`, {numref}`fig-verilog-03-f3nand` |

## Figuras de referencia
Las figuras siguientes recogen los esquemas y tablas que conviene tener a mano mientras se resuelven los ejercicios de la sesion.

La {numref}`fig-verilog-03-and` sirve como referencia para: puerta AND basica.

```{figure} ../../_static/verilog/sesion_03/and.png
---
name: fig-verilog-03-and
alt: Puerta AND basica.
width: 85%
align: center
---
Puerta AND basica.
```

La {numref}`fig-verilog-03-andvar` sirve como referencia para: instanciacion de una puerta AND en Verilog.

```{figure} ../../_static/verilog/sesion_03/andvar.png
---
name: fig-verilog-03-andvar
alt: Instanciacion de una puerta AND en Verilog.
width: 85%
align: center
---
Instanciacion de una puerta AND en Verilog.
```

La {numref}`fig-verilog-03-or` sirve como referencia para: puerta OR y su conexion conceptual.

```{figure} ../../_static/verilog/sesion_03/or.png
---
name: fig-verilog-03-or
alt: Puerta OR y su conexion conceptual.
width: 85%
align: center
---
Puerta OR y su conexion conceptual.
```

La {numref}`fig-verilog-03-not` sirve como referencia para: puerta NOT.

```{figure} ../../_static/verilog/sesion_03/not.png
---
name: fig-verilog-03-not
alt: Puerta NOT.
width: 85%
align: center
---
Puerta NOT.
```

La {numref}`fig-verilog-03-nand` sirve como referencia para: puerta NAND.

```{figure} ../../_static/verilog/sesion_03/nand.png
---
name: fig-verilog-03-nand
alt: Puerta NAND.
width: 85%
align: center
---
Puerta NAND.
```

La {numref}`fig-verilog-03-nor` sirve como referencia para: puerta NOR.

```{figure} ../../_static/verilog/sesion_03/nor.png
---
name: fig-verilog-03-nor
alt: Puerta NOR.
width: 85%
align: center
---
Puerta NOR.
```

La {numref}`fig-verilog-03-xor` sirve como referencia para: puerta XOR.

```{figure} ../../_static/verilog/sesion_03/xor.png
---
name: fig-verilog-03-xor
alt: Puerta XOR.
width: 85%
align: center
---
Puerta XOR.
```

La {numref}`fig-verilog-03-xnor` sirve como referencia para: puerta XNOR.

```{figure} ../../_static/verilog/sesion_03/xnor.png
---
name: fig-verilog-03-xnor
alt: Puerta XNOR.
width: 85%
align: center
---
Puerta XNOR.
```

La {numref}`fig-verilog-03-buf` sirve como referencia para: puerta BUFFER.

```{figure} ../../_static/verilog/sesion_03/buf.png
---
name: fig-verilog-03-buf
alt: Puerta BUFFER.
width: 85%
align: center
---
Puerta BUFFER.
```

La {numref}`fig-verilog-03-f2` sirve como referencia para: funcion logica combinacional f2.

```{figure} ../../_static/verilog/sesion_03/f2.png
---
name: fig-verilog-03-f2
alt: Funcion logica combinacional f2.
width: 85%
align: center
---
Funcion logica combinacional f2.
```

La {numref}`fig-verilog-03-f2var` sirve como referencia para: variables auxiliares de la funcion f2.

```{figure} ../../_static/verilog/sesion_03/f2var.png
---
name: fig-verilog-03-f2var
alt: Variables auxiliares de la funcion f2.
width: 85%
align: center
---
Variables auxiliares de la funcion f2.
```

La {numref}`fig-verilog-03-tablaf2` sirve como referencia para: tabla de verdad asociada a f2.

```{figure} ../../_static/verilog/sesion_03/tablaf2.png
---
name: fig-verilog-03-tablaf2
alt: Tabla de verdad asociada a f2.
width: 85%
align: center
---
Tabla de verdad asociada a f2.
```

La {numref}`fig-verilog-03-f3for` sirve como referencia para: forma algebraica de la funcion f3.

```{figure} ../../_static/verilog/sesion_03/f3for.png
---
name: fig-verilog-03-f3for
alt: Forma algebraica de la funcion f3.
width: 85%
align: center
---
Forma algebraica de la funcion f3.
```

La {numref}`fig-verilog-03-f3` sirve como referencia para: implementacion con puertas de f3.

```{figure} ../../_static/verilog/sesion_03/f3.png
---
name: fig-verilog-03-f3
alt: Implementacion con puertas de f3.
width: 85%
align: center
---
Implementacion con puertas de f3.
```

La {numref}`fig-verilog-03-f3nand` sirve como referencia para: implementacion equivalente usando NAND.

```{figure} ../../_static/verilog/sesion_03/f3nand.png
---
name: fig-verilog-03-f3nand
alt: Implementacion equivalente usando NAND.
width: 85%
align: center
---
Implementacion equivalente usando NAND.
```

## Cierre

Antes de pasar a la sesion siguiente, guarda el fichero Verilog de cada ejercicio y anota dos cosas: que esperabas obtener y que imprimio realmente la simulacion. Esa comparacion es la forma mas rapida de localizar errores.

## Fuente original

Contenido redactado y ampliado a partir de la presentacion de clase y de la pagina de referencia: <http://avellano.fis.usal.es/~compi/sesion3.htm>.
