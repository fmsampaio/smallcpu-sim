![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge)

# SmallCPU Simulator

SmallCPU-Sim is an JavaFX-based open-source project for an instruction-level simulator for the teaching-purpose central processing unit SmallCPU.

Main functionalities:

- Graphical simulation environment
- Instruction manager interface
- Step-by-step simulation interface
- Load and save memories states from/to files

Adopted languagens and libraries:

- `Java 8`
- `JavaFX`
- `Netbeans project`

## SmallCPU - A teaching-purpose central processing unit

### Basic Specification

- 8-bit processor
- Four general-purpose registers: RA, RB, RC and RX (used for indexed memory addressing)
- Memory addessing modes: direct, immediate and indexed
- Arithmetic and logic unit (ALU):
  - 8-bit 2-complement arithmetic operations
  - Adding (SelULA=0) and subtraction (SelULA=1) operations
  - Condition codes: Z (zero) and N (negative)

### Instruction Set Architecture

| Instruction | Adressing mode | Assembly |  Execution |
| ----------- | -------- | ---------- | -- |
| LDR (load register) | Direct | LDR _reg_ _mem_ | _reg_ ← DATA_MEM\[_mem_\] |
| LDR (load register) | Immediate | LDR _reg_ #_value_ | _reg_ ← _value_ |
| LDR (load register) | Indexed | LDR _reg_ _offset_,X | _reg_ ← DATA_MEM\[RX + _offset_\] |


### RTL-Level Schematic

![SmallCPU RTL-level block diagram](https://user-images.githubusercontent.com/27533879/151595348-9dbd5bc9-4ce2-44da-98b2-ff6834ef27e8.png)
