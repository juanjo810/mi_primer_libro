# Session 2. Bit Operations

This session focuses on bit manipulation with masks. The central idea is to change selected positions of a register while leaving the rest unchanged.

```{admonition} Learning objectives
:class: tip

- One's complement is obtained with `~`, turning each 0 into 1 and each 1 into 0.
- To set bits, use a mask with ones in the target positions and a bitwise OR operation.
- To clear bits, combine an inverted mask with a bitwise AND operation.
```

## Key concepts

- One's complement is obtained with `~`, turning each 0 into 1 and each 1 into 0.
- To set bits, use a mask with ones in the target positions and a bitwise OR operation.
- To clear bits, combine an inverted mask with a bitwise AND operation.
- To toggle bits, use bitwise XOR with a mask marking the positions that must change.
- Reduction operators condense many bits into one result, for example to compute parity.

## Guided practice

1. Declare a 16-bit register and assign an initial value that is easy to read in binary.
2. Set one bit, clear three bits, and toggle another bit using masks.
3. Compute the even parity bit of an 8-bit register.
4. Solve the operations by hand first and then compare them with the simulation; in this session the main reference is the bit table you build during the calculation.

## Theory-practice-figures index

Use this table as a quick map: when an exercise mentions a figure, that figure is part of the statement and should be consulted before writing the code.

| Theory block | Related exercises | Figures to consult |
|---|---|---|
| Masks, parity, and bit reduction | Exercises 1 to 4 | Manual bit table from the statement; no external figure is associated with this session |

## Work without an associated figure

This session relies mainly on operations over registers and masks. Use a handwritten bit table to track each position before running the code.

## Closing checkpoint

Before moving to the next session, save each Verilog exercise file and write down two things: what you expected to obtain and what the simulation actually printed. That comparison is the fastest way to locate errors.

## Original source

Content translated and expanded from the class presentation and the reference page: <http://avellano.fis.usal.es/~compi/sesion2.htm>.
