# Computer from Scratch

> A hands-on journey from logic gates to a programmable computer.

This repository documents my attempt to understand how computers truly work by building one layer at a time. I will begin with simple Boolean logic, combine those building blocks into arithmetic and memory circuits, design a CPU, and eventually assemble a complete computer capable of running programs.

The purpose is not simply to reproduce finished circuits. For every component, I want to understand **what problem it solves, how it works, how to test it, and how it connects to the next level of the computer**.

## The Goal

By the end of this journey, I want to be able to:

- Explain how binary information is represented and manipulated.
- Derive digital circuits from Boolean expressions and truth tables.
- Build and test combinational and sequential circuits.
- Design an arithmetic logic unit, registers, memory, and a control unit.
- Define a small instruction set and understand the fetch–decode–execute cycle.
- Combine the components into a working CPU and computer.
- Write simple programs for the computer I designed.
- Rebuild selected circuits physically or on an FPGA after validating them in simulation.

## Learning Philosophy

I will follow four rules throughout the project:

1. **Understand before copying.** I should be able to explain every wire and component.
2. **Build from smaller parts.** Larger circuits must reuse previously tested subcircuits.
3. **Test everything.** Each circuit needs a truth table, expected behaviour, and test circuit.
4. **Document the reasoning.** Mistakes, discoveries, and design decisions are part of the project.

## Roadmap

### Phase 1 - Digital Logic Foundations

- [ ] Binary, hexadecimal, and signed-number representation
- [ ] Boolean algebra and truth tables
- [ ] NOT, AND, OR, NAND, NOR, XOR, and XNOR gates
- [ ] Build other gates using only NAND
- [ ] De Morgan’s laws and circuit simplification

### Phase 2 - Combinational Logic

- [ ] Half adder
- [ ] Full adder
- [ ] 4-bit ripple-carry adder
- [ ] Adder/subtractor
- [ ] Multiplexer and demultiplexer
- [ ] Encoder and decoder
- [ ] Comparator
- [ ] Shifter
- [ ] 4-bit and 8-bit arithmetic logic units

### Phase 3 - Sequential Logic

- [ ] Clock signals and timing
- [ ] SR latch
- [ ] D latch
- [ ] D, JK, and T flip-flops
- [ ] Registers
- [ ] Shift registers
- [ ] Binary counters
- [ ] Finite-state machines

### Phase 4 - Memory and Data Storage

- [ ] One-bit memory cell
- [ ] Multi-bit register file
- [ ] RAM organisation
- [ ] Address decoding
- [ ] Read and write control
- [ ] Program memory and data memory

### Phase 5 - CPU Architecture

- [ ] Define the word size and instruction format
- [ ] Design a small instruction set architecture
- [ ] Build the program counter
- [ ] Build the instruction register
- [ ] Build the register file
- [ ] Connect the ALU and datapath
- [ ] Design the control unit
- [ ] Implement the fetch–decode–execute cycle
- [ ] Support branching, jumps, and memory operations

### Phase 6 - Complete Computer

- [ ] Integrate the CPU, memory, clock, and input/output
- [ ] Create a machine-code test program
- [ ] Write a small assembler
- [ ] Run arithmetic, branching, and memory programs
- [ ] Add basic input and output devices
- [ ] Document the final architecture
- [ ] Rebuild selected modules with physical components or an FPGA

## Repository Structure

```text
computer-from-scratch/
├── README.md
├── notes/
├── references/
└── logisim/
    ├── 01-logic-gates/
    ├── 02-combinational-logic/
    ├── 03-sequential-logic/
    ├── 04-memory/
    ├── 05-cpu/
    └── 06-full-computer/
```

Related circuits should be grouped into one Logisim Evolution project. For example, `adders.circ` can contain the following subcircuits:

```text
half_adder
full_adder
ripple_carry_adder_4bit
ripple_carry_adder_8bit
main
```

The `main` circuit is used as a test bench with input switches, clocks, probes, displays, and LEDs.

## Naming Conventions

- Use lowercase filenames with hyphens: `sequential-logic-notes.md`.
- Use lowercase circuit names with underscores: `full_adder`.
- Include the width where it matters: `register_8bit`, `mux_4to1`, `alu_8bit`.
- Give pins and signals meaningful names: `carry_in`, `carry_out`, `write_enable`.
- Avoid unexplained names such as `circuit1`, `input2`, or `new_file`.

## Circuit Documentation

For every important circuit, record:

- **Purpose:** What problem does it solve?
- **Inputs and outputs:** What does each signal represent?
- **Truth table or state table:** What behaviour is expected?
- **Design:** Which smaller components does it use?
- **Testing:** Which cases were tested?
- **Result:** Did the circuit behave correctly?
- **Lessons:** What was difficult or surprising?

## Definition of Done

A circuit is complete when:

- [ ] Its behaviour is understood, not merely copied.
- [ ] Inputs and outputs have meaningful labels.
- [ ] It is built from the appropriate reusable subcircuits.
- [ ] All truth-table combinations or important states have been tested.
- [ ] Invalid or unexpected conditions have been considered.
- [ ] The file is saved in the correct directory.
- [ ] The corresponding roadmap item and notes are updated.

## Tools

- [Logisim Evolution](https://github.com/logisim-evolution/logisim-evolution) — digital circuit design and simulation
- A text editor - notes, architecture documents, and assembly programs
- Git and GitHub - version history and off-device backup
- Breadboards, logic ICs, or an FPGA - later physical implementations

Launch Logisim Evolution on Kali Linux with:

```bash
logisim-evolution
```

## Progress Log

| Date | Milestone | What I learned |
| --- | --- | --- |
| 27-08-2026 | Project started | Defined the roadmap and project structure. |

## Long-Term Vision

The final computer does not need to compete with a modern processor. Its value will come from being understandable: every gate, register, instruction, and clock cycle should exist for a reason I can explain.

Once the simulated computer works, I plan to explore physical implementation, computer architecture, operating systems, compilers, embedded systems, and increasingly capable processor designs. This repository is the foundation of that journey.

## Author

**Emmanuel Ouang-namou Adoum**  
Computer Engineering student at Ashesi University

---

> Build the gates. Connect the circuits. Understand the machine.

