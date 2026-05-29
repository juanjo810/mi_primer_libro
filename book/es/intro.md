# Computadores I

Bienvenido al libro de prácticas de **Computadores I**.

Este material acompaña el aprendizaje de los fundamentos de diseño digital usando **Verilog** como lenguaje de descripción de hardware. La asignatura parte de una idea sencilla: un computador no es una caja mágica, sino una composición ordenada de señales, puertas lógicas, módulos, registros, contadores y unidades aritmético-lógicas.

## Qué vas a aprender

Al trabajar con este libro aprenderás a:

- describir circuitos digitales mediante módulos Verilog;
- simular el comportamiento de puertas lógicas, buses, biestables, registros y contadores;
- interpretar señales, estados y retardos de propagación;
- construir componentes combinacionales y secuenciales de forma incremental;
- relacionar cada ejercicio con los esquemas y tablas de referencia de la sesión.

## Cómo está organizado el curso

El curso se estructura en sesiones prácticas. Cada sesión incluye una breve explicación teórica, ejercicios guiados, un índice que relaciona teoría, práctica y figuras, y esquemas de referencia para no perder de vista el circuito que se está programando.

```{admonition} Método de trabajo recomendado
:class: tip

Antes de escribir código, identifica las entradas, salidas y señales internas del circuito. Después consulta las figuras de referencia, escribe el módulo Verilog y comprueba la simulación. Si el resultado no coincide con lo esperado, vuelve a la figura y revisa las conexiones.
```

## Recorrido de las sesiones

```{table} Mapa inicial de la asignatura
:name: tab-mapa-computadores-i

| Sesión | Tema | Idea principal |
|---|---|---|
| 1 | Introducción a Verilog | Entorno de trabajo, módulos básicos y salida por pantalla |
| 2 | Operaciones con bits | Máscaras, paridad y reducción de bits |
| 3 | Puertas lógicas | AND, OR, NOT, NAND, NOR, XOR, XNOR y funciones combinacionales |
| 4 | Módulos | Interfaces, jerarquía, comparadores y codificadores |
| 5 | Encaminadores y sumadores | Buses, multiplexores, semisumadores y sumadores |
| 6 | Biestables | Memoria elemental, reloj, flancos y entradas asíncronas |
| 7 | Registros | Registros SISO/SIPO y depuración con cronogramas |
| 8 | Contadores | Cuenta ascendente/descendente y transiciones de estado |
| 9 | ALU | Inclusión de ficheros y uso de la ALU 74181 |
```

## Material disponible

Empieza por la primera sesión del curso:

- [Sesión 1. Introducción a Verilog](01_verilog/sesion_01_introduccion.md)

También puedes cambiar al libro en inglés desde el selector de idioma de la barra superior.
