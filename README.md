# Simple 8-bit Processor Design – VHDL FPGA Implementation

VHDL implementation of an 8-bit processor on FPGA. Custom ALU supports shift-right, (A–B)+4, max(A,B), bitwise AND, rotate-left, and more. Modified FSM outputs parity check: odd → "y", even → "n". Built and tested in Quartus II and ModelSim with FPGA board implementation.

---

## Project Overview

This processor design was created as part of COE328 Lab 6 (Digital Systems) at Toronto Metropolitan University. It includes an Arithmetic Logic Unit (ALU), register storage, decoder, and finite-state machine (FSM) control unit.

The project implements the following:

- Problem 2(d): A custom 9-operation ALU with control via microcode
- Problem 3(c): FSM that checks parity and outputs "y" or "n" on 7-segment display

---

## Features

- ALU with 9 custom operations:
  1. Shift A right by 2 (fill = 1)
  2. (A – B) + 4
  3. Max(A, B)
  4. Swap upper 4 bits of A with lower 4 bits of B
  5. Increment A
  6. A AND B
  7. Invert upper 4 bits of A
  8. Rotate B left by 3 (ROL)
  9. Null output

- FSM Control:
  - Cycles through 9 states using clock input
  - Parity of FSM output checked each cycle
  - "y" displayed for odd parity, "n" for even parity

- Real hardware interface:
  - Inputs A and B via DIP switches
  - Clock input via push button
  - Output displayed on LEDs and 7-segment

---

## Tools Used

- Quartus II (Intel/Altera)
- ModelSim (simulation)
- FPGA board for implementation and testing
- Git and GitHub for version control

---
