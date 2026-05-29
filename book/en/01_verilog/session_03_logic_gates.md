# Session 3. Logic Gates

This session connects the logic gates studied in theory with their instantiation in Verilog. It also introduces the special values `x` and `z`, which are essential in digital simulation.

```{admonition} Learning objectives
:class: tip

- Verilog primitive gates are instantiated by listing the output first and then the inputs.
- The values `x` and `z` represent uncertainty and high impedance.
- A complete truth table must include 0, 1, x, and z when the exercise requires it.
```

## Key concepts

- Verilog primitive gates are instantiated by listing the output first and then the inputs.
- The values `x` and `z` represent uncertainty and high impedance.
- A complete truth table must include 0, 1, x, and z when the exercise requires it.
- Gate interconnection makes it possible to build more complex combinational functions.
- The same function can be implemented in different ways, for example using only NAND gates.

## Guided practice

1. Complete the AND truth table with the 16 combinations of 0, 1, x, and z; use {numref}`fig-verilog-en-03-and` and {numref}`fig-verilog-en-03-andvar` as references.
2. Repeat the check for OR, NAND, NOR, XOR, XNOR, and BUFFER; consult {numref}`fig-verilog-en-03-or` through {numref}`fig-verilog-en-03-buf` depending on the gate being simulated.
3. Build the proposed function with gates and verify its truth table; use {numref}`fig-verilog-en-03-f2`, {numref}`fig-verilog-en-03-f2var`, and {numref}`fig-verilog-en-03-tablaf2`.
4. Reimplement the function using only NAND gates and compare the outputs; follow {numref}`fig-verilog-en-03-f3`, {numref}`fig-verilog-en-03-f3for`, and {numref}`fig-verilog-en-03-f3nand`.

## Theory-practice-figures index

Use this table as a quick map: when an exercise mentions a figure, that figure is part of the statement and should be consulted before writing the code.

| Theory block | Related exercises | Figures to consult |
|---|---|---|
| Basic gates | Exercises 1 and 2 | {numref}`fig-verilog-en-03-and`, {numref}`fig-verilog-en-03-andvar`, {numref}`fig-verilog-en-03-or`, {numref}`fig-verilog-en-03-not`, {numref}`fig-verilog-en-03-nand`, {numref}`fig-verilog-en-03-nor`, {numref}`fig-verilog-en-03-xor`, {numref}`fig-verilog-en-03-xnor`, {numref}`fig-verilog-en-03-buf` |
| Combinational function f2 | Exercise 3 | {numref}`fig-verilog-en-03-f2`, {numref}`fig-verilog-en-03-f2var`, {numref}`fig-verilog-en-03-tablaf2` |
| NAND equivalence | Exercise 4 | {numref}`fig-verilog-en-03-f3for`, {numref}`fig-verilog-en-03-f3`, {numref}`fig-verilog-en-03-f3nand` |

## Reference figures

The following figures collect the diagrams and tables that are useful while solving the exercises in this session.

The {numref}`fig-verilog-en-03-and` is the reference for: basic AND gate.

```{figure} ../../_static/verilog/sesion_03/and.png
---
name: fig-verilog-en-03-and
alt: Basic AND gate.
width: 85%
align: center
---
Basic AND gate.
```

The {numref}`fig-verilog-en-03-andvar` is the reference for: instantiation of an AND gate in Verilog.

```{figure} ../../_static/verilog/sesion_03/andvar.png
---
name: fig-verilog-en-03-andvar
alt: Instantiation of an AND gate in Verilog.
width: 85%
align: center
---
Instantiation of an AND gate in Verilog.
```

The {numref}`fig-verilog-en-03-or` is the reference for: oR gate and its conceptual connection.

```{figure} ../../_static/verilog/sesion_03/or.png
---
name: fig-verilog-en-03-or
alt: OR gate and its conceptual connection.
width: 85%
align: center
---
OR gate and its conceptual connection.
```

The {numref}`fig-verilog-en-03-not` is the reference for: nOT gate.

```{figure} ../../_static/verilog/sesion_03/not.png
---
name: fig-verilog-en-03-not
alt: NOT gate.
width: 85%
align: center
---
NOT gate.
```

The {numref}`fig-verilog-en-03-nand` is the reference for: nAND gate.

```{figure} ../../_static/verilog/sesion_03/nand.png
---
name: fig-verilog-en-03-nand
alt: NAND gate.
width: 85%
align: center
---
NAND gate.
```

The {numref}`fig-verilog-en-03-nor` is the reference for: nOR gate.

```{figure} ../../_static/verilog/sesion_03/nor.png
---
name: fig-verilog-en-03-nor
alt: NOR gate.
width: 85%
align: center
---
NOR gate.
```

The {numref}`fig-verilog-en-03-xor` is the reference for: xOR gate.

```{figure} ../../_static/verilog/sesion_03/xor.png
---
name: fig-verilog-en-03-xor
alt: XOR gate.
width: 85%
align: center
---
XOR gate.
```

The {numref}`fig-verilog-en-03-xnor` is the reference for: xNOR gate.

```{figure} ../../_static/verilog/sesion_03/xnor.png
---
name: fig-verilog-en-03-xnor
alt: XNOR gate.
width: 85%
align: center
---
XNOR gate.
```

The {numref}`fig-verilog-en-03-buf` is the reference for: bUFFER gate.

```{figure} ../../_static/verilog/sesion_03/buf.png
---
name: fig-verilog-en-03-buf
alt: BUFFER gate.
width: 85%
align: center
---
BUFFER gate.
```

The {numref}`fig-verilog-en-03-f2` is the reference for: combinational logic function f2.

```{figure} ../../_static/verilog/sesion_03/f2.png
---
name: fig-verilog-en-03-f2
alt: Combinational logic function f2.
width: 85%
align: center
---
Combinational logic function f2.
```

The {numref}`fig-verilog-en-03-f2var` is the reference for: auxiliary variables for function f2.

```{figure} ../../_static/verilog/sesion_03/f2var.png
---
name: fig-verilog-en-03-f2var
alt: Auxiliary variables for function f2.
width: 85%
align: center
---
Auxiliary variables for function f2.
```

The {numref}`fig-verilog-en-03-tablaf2` is the reference for: truth table associated with f2.

```{figure} ../../_static/verilog/sesion_03/tablaf2.png
---
name: fig-verilog-en-03-tablaf2
alt: Truth table associated with f2.
width: 85%
align: center
---
Truth table associated with f2.
```

The {numref}`fig-verilog-en-03-f3for` is the reference for: algebraic form of function f3.

```{figure} ../../_static/verilog/sesion_03/f3for.png
---
name: fig-verilog-en-03-f3for
alt: Algebraic form of function f3.
width: 85%
align: center
---
Algebraic form of function f3.
```

The {numref}`fig-verilog-en-03-f3` is the reference for: gate implementation of f3.

```{figure} ../../_static/verilog/sesion_03/f3.png
---
name: fig-verilog-en-03-f3
alt: Gate implementation of f3.
width: 85%
align: center
---
Gate implementation of f3.
```

The {numref}`fig-verilog-en-03-f3nand` is the reference for: equivalent implementation using NAND gates.

```{figure} ../../_static/verilog/sesion_03/f3nand.png
---
name: fig-verilog-en-03-f3nand
alt: Equivalent implementation using NAND gates.
width: 85%
align: center
---
Equivalent implementation using NAND gates.
```

## Closing checkpoint

Before moving to the next session, save each Verilog exercise file and write down two things: what you expected to obtain and what the simulation actually printed. That comparison is the fastest way to locate errors.

## Original source

Content translated and expanded from the class presentation and the reference page: <http://avellano.fis.usal.es/~compi/sesion3.htm>.
