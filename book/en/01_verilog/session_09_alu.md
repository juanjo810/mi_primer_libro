# Session 9. ALU

The final session applies modular work to a 74181 ALU. It practices file inclusion and the combination of arithmetic and logic operations.

```{admonition} Learning objectives
:class: tip

- `include` inserts the contents of another Verilog file at the indicated point.
- The 74181 ALU receives selection lines that determine the operation.
- Negated carry lines require care when interpreting inputs and outputs.
```

## Key concepts

- `include` inserts the contents of another Verilog file at the indicated point.
- The 74181 ALU receives selection lines that determine the operation.
- Negated carry lines require care when interpreting inputs and outputs.
- Compound operations are solved by storing intermediate results.
- The test module must clearly state the inputs, selected operation, and expected output.

## Guided practice

1. Include the `74181.v` file from a test module; identify the ports in {numref}`fig-verilog-en-09-74181`.
2. Check operations such as `7+4`, `2+6+1`, AND, XOR, and OR combined with NOT/XNOR; select the control lines using {numref}`fig-verilog-en-09-74181t`.
3. Implement small multiplications as repeated additions; use {numref}`fig-verilog-en-09-74181t` again to justify each intermediate step.
4. Document each control-line selection so that errors can be debugged; your table must explicitly refer to {numref}`fig-verilog-en-09-74181` and {numref}`fig-verilog-en-09-74181t`.

## Theory-practice-figures index

Use this table as a quick map: when an exercise mentions a figure, that figure is part of the statement and should be consulted before writing the code.

| Theory block | Related exercises | Figures to consult |
|---|---|---|
| ALU interface | Exercise 1 | {numref}`fig-verilog-en-09-74181` |
| Operation selection | Exercises 2 to 4 | {numref}`fig-verilog-en-09-74181t` |

## Reference figures

The following figures collect the diagrams and tables that are useful while solving the exercises in this session.

The {numref}`fig-verilog-en-09-74181` is the reference for: functional diagram of the 74181 ALU.

```{figure} ../../_static/verilog/sesion_09/74181.png
---
name: fig-verilog-en-09-74181
alt: Functional diagram of the 74181 ALU.
width: 85%
align: center
---
Functional diagram of the 74181 ALU.
```

The {numref}`fig-verilog-en-09-74181t` is the reference for: operation table of the 74181 ALU.

```{figure} ../../_static/verilog/sesion_09/74181t.png
---
name: fig-verilog-en-09-74181t
alt: Operation table of the 74181 ALU.
width: 85%
align: center
---
Operation table of the 74181 ALU.
```

## Closing checkpoint

Before moving to the next session, save each Verilog exercise file and write down two things: what you expected to obtain and what the simulation actually printed. That comparison is the fastest way to locate errors.

## Original source

Content translated and expanded from the class presentation and the reference page: <http://avellano.fis.usal.es/~compi/sesion9.htm>.
