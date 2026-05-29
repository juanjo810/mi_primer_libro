# Session 5. Routers and Adders

This session works with buses, tri-state buffers, multiplexers, and adders. The thread that connects them is controlling where a signal flows and how carry propagates.

```{admonition} Learning objectives
:class: tip

- Tri-state buffers can place an output in high impedance.
- When several signals reach the same wire, types such as `tri`, `tri0`, `tri1`, `wand`, or `wor` are useful.
- `assign` creates a continuous connection between an expression and a wire.
```

## Key concepts

- Tri-state buffers can place an output in high impedance.
- When several signals reach the same wire, types such as `tri`, `tri0`, `tri1`, `wand`, or `wor` are useful.
- `assign` creates a continuous connection between an expression and a wire.
- Multiplexers select one input among several using control lines.
- A full adder can be built from half adders and auxiliary gates.

## Guided practice

1. Program a one-bit bus transceiver; use {numref}`fig-verilog-en-05-trans` and {numref}`fig-verilog-en-05-transnombres` to name the signals.
2. Build a 4x1 multiplexer with output enable and then an 8x1 multiplexer; use {numref}`fig-verilog-en-05-mux8x1` as a reference.
3. Implement a half adder and a full adder; relate your code to {numref}`fig-verilog-en-05-semisuma` and {numref}`fig-verilog-en-05-sumador1`.
4. Add delays and estimate the safe stabilization time in a four-bit adder; justify the calculation with {numref}`fig-verilog-en-05-propaga4` and compare it with {numref}`fig-verilog-en-05-anticipa`.

## Theory-practice-figures index

Use this table as a quick map: when an exercise mentions a figure, that figure is part of the statement and should be consulted before writing the code.

| Theory block | Related exercises | Figures to consult |
|---|---|---|
| Tri-state and buses | Exercise 1 | {numref}`fig-verilog-en-05-bufif1`, {numref}`fig-verilog-en-05-bufif0`, {numref}`fig-verilog-en-05-trans`, {numref}`fig-verilog-en-05-transnombres`, {numref}`fig-verilog-en-05-transtest` |
| Multiplexers | Exercise 2 | {numref}`fig-verilog-en-05-mux8x1`, {numref}`fig-verilog-en-05-h4` |
| Adders | Exercise 3 | {numref}`fig-verilog-en-05-semisuma`, {numref}`fig-verilog-en-05-sumador1` |
| Delays and carry | Exercise 4 | {numref}`fig-verilog-en-05-propaga4`, {numref}`fig-verilog-en-05-anticipa` |

## Reference figures

The following figures collect the diagrams and tables that are useful while solving the exercises in this session.

The {numref}`fig-verilog-en-05-bufif1` is the reference for: tri-state buffer active high.

```{figure} ../../_static/verilog/sesion_05/bufif1.png
---
name: fig-verilog-en-05-bufif1
alt: Tri-state buffer active high.
width: 85%
align: center
---
Tri-state buffer active high.
```

The {numref}`fig-verilog-en-05-bufif0` is the reference for: tri-state buffer active low.

```{figure} ../../_static/verilog/sesion_05/bufif0.png
---
name: fig-verilog-en-05-bufif0
alt: Tri-state buffer active low.
width: 85%
align: center
---
Tri-state buffer active low.
```

The {numref}`fig-verilog-en-05-trans` is the reference for: one-bit bus transceiver.

```{figure} ../../_static/verilog/sesion_05/trans.png
---
name: fig-verilog-en-05-trans
alt: One-bit bus transceiver.
width: 85%
align: center
---
One-bit bus transceiver.
```

The {numref}`fig-verilog-en-05-transnombres` is the reference for: auxiliary signal names in the transceiver.

```{figure} ../../_static/verilog/sesion_05/transNombres.png
---
name: fig-verilog-en-05-transnombres
alt: Auxiliary signal names in the transceiver.
width: 85%
align: center
---
Auxiliary signal names in the transceiver.
```

The {numref}`fig-verilog-en-05-transtest` is the reference for: transceiver test module.

```{figure} ../../_static/verilog/sesion_05/transTest.png
---
name: fig-verilog-en-05-transtest
alt: Transceiver test module.
width: 85%
align: center
---
Transceiver test module.
```

The {numref}`fig-verilog-en-05-mux8x1` is the reference for: 8x1 multiplexer built from smaller multiplexers.

```{figure} ../../_static/verilog/sesion_05/mux8x1.png
---
name: fig-verilog-en-05-mux8x1
alt: 8x1 multiplexer built from smaller multiplexers.
width: 85%
align: center
---
8x1 multiplexer built from smaller multiplexers.
```

The {numref}`fig-verilog-en-05-h4` is the reference for: auxiliary structure for signal selection.

```{figure} ../../_static/verilog/sesion_05/h4.png
---
name: fig-verilog-en-05-h4
alt: Auxiliary structure for signal selection.
width: 85%
align: center
---
Auxiliary structure for signal selection.
```

The {numref}`fig-verilog-en-05-semisuma` is the reference for: half adder.

```{figure} ../../_static/verilog/sesion_05/semisuma.png
---
name: fig-verilog-en-05-semisuma
alt: Half adder.
width: 85%
align: center
---
Half adder.
```

The {numref}`fig-verilog-en-05-sumador1` is the reference for: one-bit full adder.

```{figure} ../../_static/verilog/sesion_05/sumador1.png
---
name: fig-verilog-en-05-sumador1
alt: One-bit full adder.
width: 85%
align: center
---
One-bit full adder.
```

The {numref}`fig-verilog-en-05-propaga4` is the reference for: four-bit ripple-carry adder.

```{figure} ../../_static/verilog/sesion_05/propaga4.png
---
name: fig-verilog-en-05-propaga4
alt: Four-bit ripple-carry adder.
width: 85%
align: center
---
Four-bit ripple-carry adder.
```

The {numref}`fig-verilog-en-05-anticipa` is the reference for: carry-lookahead adder.

```{figure} ../../_static/verilog/sesion_05/anticipa.png
---
name: fig-verilog-en-05-anticipa
alt: Carry-lookahead adder.
width: 85%
align: center
---
Carry-lookahead adder.
```

## Closing checkpoint

Before moving to the next session, save each Verilog exercise file and write down two things: what you expected to obtain and what the simulation actually printed. That comparison is the fastest way to locate errors.

## Original source

Content translated and expanded from the class presentation and the reference page: <http://avellano.fis.usal.es/~compi/sesion5.htm>.
