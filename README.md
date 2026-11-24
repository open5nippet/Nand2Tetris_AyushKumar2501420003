# Nand2Tetris Course Work

This repository contains HDL implementations, Hack assembly programs, custom Python assemblers, simulator outputs, and capstone work completed for the Nand2Tetris course.

## Repository Overview

| Section | Topics covered |
| --- | --- |
| [Project 1](Project%201%20of%20nand_2_tetris) | Boolean logic, elementary gates, multiplexers, and demultiplexers |
| [Project 2](project%202%20of%20nand_2_tetris) | Adders, incrementing, and the 16-bit ALU |
| [Project 3](project%203%20of%20nand_2_tetris) | Registers, counters, and the memory hierarchy |
| [Project 5](Project%205%20of%20nand_2_tetris) | CPU, memory map, and complete Hack computer |
| [Assembly](Assembly) | Arithmetic, branching, loops, keyboard input, and screen output |
| [Capstone](Capstone) | ZOSIMA report, custom assembler, and interactive box demo |

## Project 1 — Boolean Logic

The [Project 1](Project%201%20of%20nand_2_tetris) HDL chips implement:

- Basic gates: `And`, `Or`, `Xor`, `Not`
- 16-bit gates: `And16`, `Or16`, `Not16`
- Multi-way logic: `Or8Way`
- Data selection: `Mux`, `Mux16`, `Mux4Way16`, `Mux8Way16`
- Data routing: `DMux`, `DMux4Way`, `DMux8Way`

The associated [lab PDF](Project%201%20of%20nand_2_tetris/Nand2Tetris_Lab1_Project1_Sameer_Mishra.pdf) documents the lab submission.

## Project 2 — Arithmetic

The [Project 2](project%202%20of%20nand_2_tetris) implementations include:

- `HalfAdder` and `FullAdder`
- `Add16` and `Inc16`
- `ALU`, with output status flags for zero (`zr`) and negative (`ng`)

## Project 3 — Sequential Logic and Memory

The [Project 3](project%203%20of%20nand_2_tetris) directory contains:

- `Bit`
- `Register`
- `PC`
- `RAM8`, `RAM64`, `RAM512`, `RAM4K`, and `RAM16K`

The [Project 3 submission PDF](project%203%20of%20nand_2_tetris/Nand2Tetris_Project3_HDL_Code_and_Screenshots_Updated.pdf) includes HDL code and Hardware Simulator screenshots.

## Project 5 — Computer Architecture

The [Project 5](Project%205%20of%20nand_2_tetris) chips form the major components of the Hack computer:

- [`CPU.hdl`](Project%205%20of%20nand_2_tetris/CPU.hdl) — decodes instructions, executes ALU operations, handles memory writes, and evaluates jump conditions.
- [`Memory.hdl`](Project%205%20of%20nand_2_tetris/Memory.hdl) — maps the 16K RAM, screen memory, and keyboard register.
- [`Computer.hdl`](Project%205%20of%20nand_2_tetris/Computer.hdl) — connects the ROM32K, CPU, and memory chips.

## Hack Assembly Programs

### Basic Assembly

- [`Add.asm`](Assembly/Basics/Add.asm) adds `R0` and `R1` and stores the result in `R2`.
- [`branching.asm`](Assembly/Basics/branching.asm) compares values and places the larger value in `R2`.
- [`loop.asm`](Assembly/Basics/loop.asm) demonstrates loop counters and repeated addition.

### Input and Output

- [`keyboard.asm`](Assembly/IO/keyboard.asm) waits for the `q` key.
- [`screen.asm`](Assembly/IO/screen.asm) writes black values to selected screen-memory addresses.
- [`Hack-to-Binary.asm`](Assembly/IO/Hack-to-Binary.asm) shows the binary form of example Hack instructions.

## Capstone — ZOSIMA

The [Capstone](Capstone) project contains the complete report and additional implementations:

### Part A — Complete Hack Computer

The [Part A](Capstone/PartA) directory contains:

- `CPU.hdl`
- `Memory.hdl`
- `Computer.hdl`
- Hardware Simulator screenshots for CPU, memory, and computer tests

### Part B — Assembler and Duplicate-Label Check

The [Part B](Capstone/PartB) directory contains:

- [`assembler.py`](Capstone/PartB/assembler.py) — a two-pass Hack assembler with predefined symbols, labels, variables, A-instructions, C-instructions, bounds checking, and `.hack` output.
- [`Add.asm`](Capstone/PartB/Add.asm) and [`Add.hack`](Capstone/PartB/Add.hack) — a simple assembly program and its machine code.
- [`TestDuplicate.asm`](Capstone/PartB/TestDuplicate.asm) — duplicate-label test input for the K = 44 extra feature.
- Screenshots showing successful assembly and duplicate-label warnings.

Run the assembler:

```bash
cd "Capstone/PartB"
python assembler.py TestDuplicate.asm
python assembler.py Add.asm
```

### Part C — Interactive Keyboard-Controlled Box

The [Part C](Capstone/PartC) directory contains:

- [`Box.asm`](Capstone/PartC/Box.asm) — draws a 16-pixel-wide, 20-row box at row 44; pressing any key changes the box to black.
- [`assembler.py`](Capstone/PartC/assembler.py) — converts the program into [`Box.hack`](Capstone/PartC/Box.hack).
- Screenshots for the released-key and pressed-key states.

Run the interactive demo:

```bash
cd "Capstone/PartC"
python assembler.py Box.asm
```

Load `Box.hack` in the Nand2Tetris CPU Emulator and run the program. Press a key to change the box from white to black.

## Running the HDL Projects

1. Install the Nand2Tetris software suite.
2. Open `HardwareSimulator`.
3. Load an `.hdl` implementation.
4. Load the matching course test scripts, if available.
5. Run the test and confirm that it completes without mismatches.

## Running Assembly Programs

1. Open the official Nand2Tetris `Assembler` for standard `.asm` files.
2. Load an assembly program from `Assembly/`.
3. Generate the `.hack` output.
4. Load the machine code into `CPUEmulator` to execute it.

For the custom assemblers in `Capstone/PartB` and `Capstone/PartC`, run `python assembler.py <file.asm>` from a terminal.

## Submission Documents

- [Nand2Tetris Lab 1 submission](Project%201%20of%20nand_2_tetris/Nand2Tetris_Lab1_Project1_Sameer_Mishra.pdf)
- [Project 3 HDL and screenshots](project%203%20of%20nand_2_tetris/Nand2Tetris_Project3_HDL_Code_and_Screenshots_Updated.pdf)
- [ZOSIMA capstone report](Capstone/The%20ZOSIMA%20Report.pdf)

## Author

**Ayush Kumar**
