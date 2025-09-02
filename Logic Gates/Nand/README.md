# NandGame – Level 1: Nand Gate

In this level, the goal is to build a NAND gate using the relay components provided.  
To figure this out, I started by writing down the truth tables for the two types of relay circuits: **relay off** and **relay on**.

---

## Relay Off

When the relay is off, the circuit behaves like an AND gate. Both inputs must be high for the output to be high.

| Input A | Input B | Output |
|---------|----------|--------|
| 0       | 0        | 0      |
| 0       | 1        | 0      |
| 1       | 0        | 0      |
| 1       | 1        | 1      |

---

## Relay On

When the relay is on, the circuit flips the output whenever the input is high.  
This makes the output the inverse of the input.

| Input | Output |
|-------|--------|
| 0     | 0      |
| 1     | 0      |

Wait, let’s check carefully. If the relay is on and the input goes high, the output is forced low. So the behavior is:

| Input | Output |
|-------|--------|
| 0     | 1      |
| 1     | 0      |

---

## Building the NAND

By combining the relay off and relay on circuits, we can first generate an **AND** with the relay off, then pass that signal into the relay on to invert it.  

The result is a NAND gate:

| Input A | Input B | NAND Output |
|---------|----------|-------------|
| 0       | 0        | 1           |
| 0       | 1        | 1           |
| 1       | 0        | 1           |
| 1       | 1        | 0           |

---

## Summary

- **Relay off** acts like an AND gate.  
- **Relay on** acts like a NOT gate.  
- Putting them together gives a NAND gate, which is exactly what this level asks for.
