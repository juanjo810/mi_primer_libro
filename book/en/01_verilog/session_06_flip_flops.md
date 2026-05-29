# Session 6. Flip-Flops

This session moves from combinational logic to memory. Flip-flops keep state, which forces us to reason about clocks, edges, asynchronous inputs, and delays.

```{admonition} Learning objectives
:class: tip

- An RS flip-flop can be built with two cross-coupled NOR gates.
- Blocking and non-blocking assignments do not always have the same timing effect.
- A clock can be generated with an `always` block that periodically toggles a signal.
```

## Key concepts

- An RS flip-flop can be built with two cross-coupled NOR gates.
- Blocking and non-blocking assignments do not always have the same timing effect.
- A clock can be generated with an `always` block that periodically toggles a signal.
- Edge detectors convert a level condition into a short pulse.
- PRESET and CLEAR are often asynchronous and take priority over the clock.

## Guided practice

1. Program an RS flip-flop and run the proposed input sequence; consult {numref}`fig-verilog-en-06-rs` and compare the results with {numref}`fig-verilog-en-06-rstabla`.
2. Replace some assignments with non-blocking assignments and observe the differences near the invalid states shown in {numref}`fig-verilog-en-06-rstabla`.
3. Add a level-sensitive clock input; use {numref}`fig-verilog-en-06-rsc` and {numref}`fig-verilog-en-06-rsctabla` to check when the output should change.
4. Build an edge-triggered version and then a JK flip-flop with PRESET and CLEAR; follow {numref}`fig-verilog-en-06-det`, {numref}`fig-verilog-en-06-jk`, and {numref}`fig-verilog-en-06-jktabla`.

## Theory-practice-figures index

Use this table as a quick map: when an exercise mentions a figure, that figure is part of the statement and should be consulted before writing the code.

| Theory block | Related exercises | Figures to consult |
|---|---|---|
| RS flip-flop | Exercises 1 and 2 | {numref}`fig-verilog-en-06-rs`, {numref}`fig-verilog-en-06-rstabla` |
| Level-sensitive clock | Exercise 3 | {numref}`fig-verilog-en-06-rsc`, {numref}`fig-verilog-en-06-rsctabla` |
| Edges and JK | Exercise 4 | {numref}`fig-verilog-en-06-det`, {numref}`fig-verilog-en-06-jk`, {numref}`fig-verilog-en-06-jktabla` |

## Reference figures

The following figures collect the diagrams and tables that are useful while solving the exercises in this session.

The {numref}`fig-verilog-en-06-rs` is the reference for: rS flip-flop with NOR gates.

```{figure} ../../_static/verilog/sesion_06/rs.png
---
name: fig-verilog-en-06-rs
alt: RS flip-flop with NOR gates.
width: 85%
align: center
---
RS flip-flop with NOR gates.
```

The {numref}`fig-verilog-en-06-rstabla` is the reference for: rS flip-flop behavior table.

```{figure} ../../_static/verilog/sesion_06/rstabla.png
---
name: fig-verilog-en-06-rstabla
alt: RS flip-flop behavior table.
width: 85%
align: center
---
RS flip-flop behavior table.
```

The {numref}`fig-verilog-en-06-rsc` is the reference for: clocked RS flip-flop.

```{figure} ../../_static/verilog/sesion_06/rsc.png
---
name: fig-verilog-en-06-rsc
alt: Clocked RS flip-flop.
width: 85%
align: center
---
Clocked RS flip-flop.
```

The {numref}`fig-verilog-en-06-rsctabla` is the reference for: clocked RS flip-flop behavior table.

```{figure} ../../_static/verilog/sesion_06/rsctabla.png
---
name: fig-verilog-en-06-rsctabla
alt: Clocked RS flip-flop behavior table.
width: 85%
align: center
---
Clocked RS flip-flop behavior table.
```

The {numref}`fig-verilog-en-06-det` is the reference for: edge detector.

```{figure} ../../_static/verilog/sesion_06/det.png
---
name: fig-verilog-en-06-det
alt: Edge detector.
width: 85%
align: center
---
Edge detector.
```

The {numref}`fig-verilog-en-06-jk` is the reference for: jK flip-flop with control inputs.

```{figure} ../../_static/verilog/sesion_06/jk.png
---
name: fig-verilog-en-06-jk
alt: JK flip-flop with control inputs.
width: 85%
align: center
---
JK flip-flop with control inputs.
```

The {numref}`fig-verilog-en-06-jktabla` is the reference for: jK flip-flop behavior table.

```{figure} ../../_static/verilog/sesion_06/jktabla.png
---
name: fig-verilog-en-06-jktabla
alt: JK flip-flop behavior table.
width: 85%
align: center
---
JK flip-flop behavior table.
```

## Closing checkpoint

Before moving to the next session, save each Verilog exercise file and write down two things: what you expected to obtain and what the simulation actually printed. That comparison is the fastest way to locate errors.

## Original source

Content translated and expanded from the class presentation and the reference page: <http://avellano.fis.usal.es/~compi/sesion6.htm>.
