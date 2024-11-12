
# 32-bit RISC-V Processor in Verilog

## Overview
This project implements a 32-bit RISC-V processor in Verilog, designed for educational purposes to demonstrate basic CPU architecture concepts.

## Features
- R-type, I-type, B-type, and S-type instruction support
- Instruction Fetch, Decode, Execute, Memory, and Write-back stages
- Register file with 32 32-bit registers
- ALU for arithmetic and logic operations
- Control unit for instruction decoding

## Project Structure
```
├── src/
│   ├── TopModule.v
│   ├── InstructionFetch.v
│   ├── ControlUnit.v
│   ├── RegisterFile.v
│   ├── ALUDecoder.v
│   └── ALU.v
├── sim/
│   ├── TopModule_tb.v
│   └── ...
├── README.md
```

## Modules
- **TopModule.v**: Top-level module connecting all components
- **InstructionFetch.v**: Handles program counter and instruction fetching
- **ControlUnit.v**: Decodes instructions and generates control signals
- **RegisterFile.v**: Implements the register file
- **ALUDecoder.v**: Decodes instructions and determine exact arithmetic and logical operations
- **ALU.v**: Performs arithmetic and logical operations

## Getting Started
1. Clone this repository.
2. Open the project in a Verilog simulator such as Xilinx Vivado.
3. Run simulations using the provided testbench files.

## Testbench
The provided testbench (`TopModule_tb.v`) tests basic functionality, including:
- Reset behavior
- Instruction execution
- ALU operations

## Example Instructions
Example machine code instructions used for testing:
- `00000000000100000000000010110011` - ADD x1, x0, x1 (R-type)
- `00000000001000000010000100010011` - ADDI x2, x0, 2 (I-type)
- `00000000001100001000001010110011` - ADD x5, x1, x3 (R-type)
- `00000000001000000000000001100011` - BEQ x2, x0, 4 (B-type)
- `00000000000100000010000000100011` - SW x1, 0(x0) (S-type)

## Simulation
To run the simulation:
1. Ensure all modules are included.
2. Run `TopModule_tb.v` in your simulator.


