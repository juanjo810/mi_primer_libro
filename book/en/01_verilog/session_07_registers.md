# Session 7. Registers

This session builds registers from flip-flops and introduces an essential debugging tool: waveforms with GTKWave.

```{admonition} Learning objectives
:class: tip

- A register stores several bits distributed across flip-flops.
- SISO registers shift information serial-in, serial-out.
- SIPO registers receive data serially and output it in parallel.
```

## Key concepts

- A register stores several bits distributed across flip-flops.
- SISO registers shift information serial-in, serial-out.
- SIPO registers receive data serially and output it in parallel.
- `$dumpfile` and `$dumpvars` generate waveform files for signal inspection.
- Real or simulated delays can explain unexpected behavior.

## Guided practice

1. Build a D flip-flop from the blocks already studied; use {numref}`fig-verilog-en-07-d` to verify inputs and output.
2. Use several flip-flops to form a SISO register; follow the connection in {numref}`fig-verilog-en-07-siso`.
3. Generate a waveform file and open it with GTKWave; compare the expected window with {numref}`fig-verilog-en-07-gtkwave`.
4. Modify the register to obtain a parallel SIPO output; use {numref}`fig-verilog-en-07-sipo` and, for the extension, {numref}`fig-verilog-en-07-pisiso`.

## Theory-practice-figures index

Use this table as a quick map: when an exercise mentions a figure, that figure is part of the statement and should be consulted before writing the code.

| Theory block | Related exercises | Figures to consult |
|---|---|---|
| D flip-flop | Exercise 1 | {numref}`fig-verilog-en-07-d` |
| SISO register | Exercise 2 | {numref}`fig-verilog-en-07-siso` |
| Waveforms | Exercise 3 | {numref}`fig-verilog-en-07-gtkwave` |
| SIPO registers and parallel load | Exercise 4 | {numref}`fig-verilog-en-07-sipo`, {numref}`fig-verilog-en-07-pisiso` |

## Reference figures

The following figures collect the diagrams and tables that are useful while solving the exercises in this session.

The {numref}`fig-verilog-en-07-d` is the reference for: d flip-flop.

```{figure} ../../_static/verilog/sesion_07/d.png
---
name: fig-verilog-en-07-d
alt: D flip-flop.
width: 85%
align: center
---
D flip-flop.
```

The {numref}`fig-verilog-en-07-siso` is the reference for: sISO register.

```{figure} ../../_static/verilog/sesion_07/siso.png
---
name: fig-verilog-en-07-siso
alt: SISO register.
width: 85%
align: center
---
SISO register.
```

The {numref}`fig-verilog-en-07-gtkwave` is the reference for: signal visualization with GTKWave.

```{figure} ../../_static/verilog/sesion_07/gtkwave.png
---
name: fig-verilog-en-07-gtkwave
alt: Signal visualization with GTKWave.
width: 85%
align: center
---
Signal visualization with GTKWave.
```

The {numref}`fig-verilog-en-07-sipo` is the reference for: sIPO register.

```{figure} ../../_static/verilog/sesion_07/sipo.png
---
name: fig-verilog-en-07-sipo
alt: SIPO register.
width: 85%
align: center
---
SIPO register.
```

The {numref}`fig-verilog-en-07-pisiso` is the reference for: register with parallel load and serial shift.

```{figure} ../../_static/verilog/sesion_07/pisiso.png
---
name: fig-verilog-en-07-pisiso
alt: Register with parallel load and serial shift.
width: 85%
align: center
---
Register with parallel load and serial shift.
```

## Closing checkpoint

Before moving to the next session, save each Verilog exercise file and write down two things: what you expected to obtain and what the simulation actually printed. That comparison is the fastest way to locate errors.

## Original source

Content translated and expanded from the class presentation and the reference page: <http://avellano.fis.usal.es/~compi/sesion7.htm>.
