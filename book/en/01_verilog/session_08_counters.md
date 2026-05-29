# Session 8. Counters

This session uses flip-flops to build counters and analyze state transitions. The important point is to distinguish ideal behavior, delays, and transient states.

```{admonition} Learning objectives
:class: tip

- A counter changes state according to a clock signal.
- Counting can be upward or downward depending on a mode line.
- HOLD freezes the state when the count direction must change without jumps.
```

## Key concepts

- A counter changes state according to a clock signal.
- Counting can be upward or downward depending on a mode line.
- HOLD freezes the state when the count direction must change without jumps.
- Asynchronous counters can pass through transient states while signals propagate.
- State transition diagrams summarize the sequential behavior of a circuit.

## Guided practice

1. Program a four-bit up/down counter; use {numref}`fig-verilog-en-08-contador` to define inputs, outputs, and count mode.
2. Observe what happens when changing mode without clearing the counter; explain the transient states with {numref}`fig-verilog-en-08-analisis`.
3. Add PRESET, CLEAR, and HOLD to control transitions better; compare your design with {numref}`fig-verilog-en-08-contsinc` and {numref}`fig-verilog-en-08-cont01`.
4. Analyze an arbitrary-count counter and draw its state diagram; use {numref}`fig-verilog-en-08-transis`, {numref}`fig-verilog-en-08-jkarn`, and {numref}`fig-verilog-en-08-contarb`.

## Theory-practice-figures index

Use this table as a quick map: when an exercise mentions a figure, that figure is part of the statement and should be consulted before writing the code.

| Theory block | Related exercises | Figures to consult |
|---|---|---|
| Up/down counting | Exercises 1 and 2 | {numref}`fig-verilog-en-08-contador`, {numref}`fig-verilog-en-08-analisis` |
| Transition control | Exercise 3 | {numref}`fig-verilog-en-08-10a0`, {numref}`fig-verilog-en-08-contsinc`, {numref}`fig-verilog-en-08-cont01` |
| States and JK flip-flops | Exercise 4 | {numref}`fig-verilog-en-08-transjk`, {numref}`fig-verilog-en-08-transis`, {numref}`fig-verilog-en-08-jkarn`, {numref}`fig-verilog-en-08-contarb` |

## Reference figures

The following figures collect the diagrams and tables that are useful while solving the exercises in this session.

The {numref}`fig-verilog-en-08-contador` is the reference for: counter with up/down selection.

```{figure} ../../_static/verilog/sesion_08/contador.png
---
name: fig-verilog-en-08-contador
alt: Counter with up/down selection.
width: 85%
align: center
---
Counter with up/down selection.
```

The {numref}`fig-verilog-en-08-10a0` is the reference for: counter from 10 down to 0.

```{figure} ../../_static/verilog/sesion_08/10a0.png
---
name: fig-verilog-en-08-10a0
alt: Counter from 10 down to 0.
width: 85%
align: center
---
Counter from 10 down to 0.
```

The {numref}`fig-verilog-en-08-contsinc` is the reference for: synchronous counter.

```{figure} ../../_static/verilog/sesion_08/contsinc.png
---
name: fig-verilog-en-08-contsinc
alt: Synchronous counter.
width: 85%
align: center
---
Synchronous counter.
```

The {numref}`fig-verilog-en-08-analisis` is the reference for: analysis of states and transitions.

```{figure} ../../_static/verilog/sesion_08/analisis.png
---
name: fig-verilog-en-08-analisis
alt: Analysis of states and transitions.
width: 85%
align: center
---
Analysis of states and transitions.
```

The {numref}`fig-verilog-en-08-cont01` is the reference for: auxiliary counter circuit.

```{figure} ../../_static/verilog/sesion_08/cont01.png
---
name: fig-verilog-en-08-cont01
alt: Auxiliary counter circuit.
width: 85%
align: center
---
Auxiliary counter circuit.
```

The {numref}`fig-verilog-en-08-transjk` is the reference for: transitions of a JK flip-flop.

```{figure} ../../_static/verilog/sesion_08/transJK.png
---
name: fig-verilog-en-08-transjk
alt: Transitions of a JK flip-flop.
width: 85%
align: center
---
Transitions of a JK flip-flop.
```

The {numref}`fig-verilog-en-08-transis` is the reference for: state transition diagram.

```{figure} ../../_static/verilog/sesion_08/transis.png
---
name: fig-verilog-en-08-transis
alt: State transition diagram.
width: 85%
align: center
---
State transition diagram.
```

The {numref}`fig-verilog-en-08-jkarn` is the reference for: karnaugh map for JK inputs.

```{figure} ../../_static/verilog/sesion_08/jkarn.png
---
name: fig-verilog-en-08-jkarn
alt: Karnaugh map for JK inputs.
width: 85%
align: center
---
Karnaugh map for JK inputs.
```

The {numref}`fig-verilog-en-08-contarb` is the reference for: arbitrary-count counter.

```{figure} ../../_static/verilog/sesion_08/contarb.png
---
name: fig-verilog-en-08-contarb
alt: Arbitrary-count counter.
width: 85%
align: center
---
Arbitrary-count counter.
```

## Closing checkpoint

Before moving to the next session, save each Verilog exercise file and write down two things: what you expected to obtain and what the simulation actually printed. That comparison is the fastest way to locate errors.

## Original source

Content translated and expanded from the class presentation and the reference page: <http://avellano.fis.usal.es/~compi/sesion8.htm>.
