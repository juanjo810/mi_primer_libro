# Session 1. Introduction to Verilog

This session introduces Verilog as a hardware description language and sets up the minimum workflow for compiling and simulating simple examples. The goal is not to write conventional software, but to describe circuits and observe their behavior.

```{admonition} Learning objectives
:class: tip

- Verilog is an HDL: it describes hardware, not just a sequence of software instructions.
- The basic workflow is to write a `.v` file, compile it, and run the simulation.
- Modules delimit the design; an `initial` block defines a sequence of test actions.
```

## Key concepts

- Verilog is an HDL: it describes hardware, not just a sequence of software instructions.
- The basic workflow is to write a `.v` file, compile it, and run the simulation.
- Modules delimit the design; an `initial` block defines a sequence of test actions.
- Registers (`reg`) store values during simulation and wires (`wire`) connect signals.
- The `$display` format codes help inspect values in binary, octal, decimal, or hexadecimal.

## Guided practice

1. Create a working directory and save a `hello.v` file inside it.
2. Compile the file with `iverilog` and run the generated output.
3. Modify the example so that it prints an integer in decimal, binary, and hexadecimal; compare your output with {numref}`fig-verilog-en-01-ej-1-9`.
4. Declare a 16-bit register and observe what happens when assigning values beyond its capacity; use {numref}`fig-verilog-en-01-ej-1-9-comentado` to identify which code fragment produces each output.

## Theory-practice-figures index

Use this table as a quick map: when an exercise mentions a figure, that figure is part of the statement and should be consulted before writing the code.

| Theory block | Related exercises | Figures to consult |
|---|---|---|
| Output formats and base conversion | Exercises 3 and 4 | {numref}`fig-verilog-en-01-ej-1-9`, {numref}`fig-verilog-en-01-ej-1-9-comentado` |

## Reference figures

The following figures collect the diagrams and tables that are useful while solving the exercises in this session.

The {numref}`fig-verilog-en-01-ej-1-9` is the reference for: expected output for an introductory conversion and display exercise.

```{figure} ../../_static/verilog/sesion_01/ej_1_9.png
---
name: fig-verilog-en-01-ej-1-9
alt: Expected output for an introductory conversion and display exercise.
width: 85%
align: center
---
Expected output for an introductory conversion and display exercise.
```

The {numref}`fig-verilog-en-01-ej-1-9-comentado` is the reference for: commented version of the same example, useful for locating each instruction in the code.

```{figure} ../../_static/verilog/sesion_01/ej_1_9_comentado.png
---
name: fig-verilog-en-01-ej-1-9-comentado
alt: Commented version of the same example, useful for locating each instruction in the code.
width: 85%
align: center
---
Commented version of the same example, useful for locating each instruction in the code.
```

## Closing checkpoint

Before moving to the next session, save each Verilog exercise file and write down two things: what you expected to obtain and what the simulation actually printed. That comparison is the fastest way to locate errors.

## Original source

Content translated and expanded from the class presentation and the reference page: <http://avellano.fis.usal.es/~compi/sesion1.htm>.
