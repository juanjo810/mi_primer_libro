# Session 4. Modules

This session introduces modular design. A Verilog module encapsulates inputs, outputs, and behavior, like a reusable circuit block.

```{admonition} Learning objectives
:class: tip

- A module needs a clear interface: `input`, `output`, and `inout`.
- Hierarchy lets us build large systems from smaller modules.
- Logic gates can be viewed as predefined modules in the language.
```

## Key concepts

- A module needs a clear interface: `input`, `output`, and `inout`.
- Hierarchy lets us build large systems from smaller modules.
- Logic gates can be viewed as predefined modules in the language.
- A one-bit comparator is a good first example of a reusable module.
- Encoders show how a circuit changes when priority is introduced.

## Guided practice

1. Define the interface of a one-bit comparator; identify inputs and outputs in {numref}`fig-verilog-en-04-compar1`.
2. Implement the comparator with NOT, AND, and NOR gates; follow the internal structure in {numref}`fig-verilog-en-04-compar11`.
3. Create a test module that enumerates all input combinations; compare your approach with {numref}`fig-verilog-en-04-testcomp1`.
4. Use two one-bit comparators to build a two-bit comparator; take the hierarchy in {numref}`fig-verilog-en-04-comp2` as a reference.

## Theory-practice-figures index

Use this table as a quick map: when an exercise mentions a figure, that figure is part of the statement and should be consulted before writing the code.

| Theory block | Related exercises | Figures to consult |
|---|---|---|
| Module interface | Exercise 1 | {numref}`fig-verilog-en-04-modulo`, {numref}`fig-verilog-en-04-compar1` |
| Comparator internal circuit | Exercise 2 | {numref}`fig-verilog-en-04-compar11` |
| Test module | Exercise 3 | {numref}`fig-verilog-en-04-testcomp1` |
| Hierarchy and encoders | Exercise 4 and extensions | {numref}`fig-verilog-en-04-comp2`, {numref}`fig-verilog-en-04-priocod`, {numref}`fig-verilog-en-04-and4` |

## Reference figures

The following figures collect the diagrams and tables that are useful while solving the exercises in this session.

The {numref}`fig-verilog-en-04-modulo` is the reference for: general diagram of a module with ports.

```{figure} ../../_static/verilog/sesion_04/mOdulo.png
---
name: fig-verilog-en-04-modulo
alt: General diagram of a module with ports.
width: 85%
align: center
---
General diagram of a module with ports.
```

The {numref}`fig-verilog-en-04-compar1` is the reference for: one-bit comparator.

```{figure} ../../_static/verilog/sesion_04/compar1.png
---
name: fig-verilog-en-04-compar1
alt: One-bit comparator.
width: 85%
align: center
---
One-bit comparator.
```

The {numref}`fig-verilog-en-04-compar11` is the reference for: internal implementation of the one-bit comparator.

```{figure} ../../_static/verilog/sesion_04/compar11.png
---
name: fig-verilog-en-04-compar11
alt: Internal implementation of the one-bit comparator.
width: 85%
align: center
---
Internal implementation of the one-bit comparator.
```

The {numref}`fig-verilog-en-04-testcomp1` is the reference for: comparator test module.

```{figure} ../../_static/verilog/sesion_04/TestComp1.png
---
name: fig-verilog-en-04-testcomp1
alt: Comparator test module.
width: 85%
align: center
---
Comparator test module.
```

The {numref}`fig-verilog-en-04-comp2` is the reference for: two-bit comparator built hierarchically.

```{figure} ../../_static/verilog/sesion_04/comp2.png
---
name: fig-verilog-en-04-comp2
alt: Two-bit comparator built hierarchically.
width: 85%
align: center
---
Two-bit comparator built hierarchically.
```

The {numref}`fig-verilog-en-04-priocod` is the reference for: priority encoder.

```{figure} ../../_static/verilog/sesion_04/priocod.png
---
name: fig-verilog-en-04-priocod
alt: Priority encoder.
width: 85%
align: center
---
Priority encoder.
```

The {numref}`fig-verilog-en-04-and4` is the reference for: four-input AND gate.

```{figure} ../../_static/verilog/sesion_04/and4.png
---
name: fig-verilog-en-04-and4
alt: Four-input AND gate.
width: 85%
align: center
---
Four-input AND gate.
```

## Closing checkpoint

Before moving to the next session, save each Verilog exercise file and write down two things: what you expected to obtain and what the simulation actually printed. That comparison is the fastest way to locate errors.

## Original source

Content translated and expanded from the class presentation and the reference page: <http://avellano.fis.usal.es/~compi/sesion4.htm>.
