8-Bit Arithmetic Logic Unit (ALU) Using Verilog HDL

 Project Overview

This project implements an 8-bit Arithmetic Logic Unit (ALU) using Verilog Hardware Description Language (HDL).

The ALU performs basic arithmetic and logical operations based on a 3-bit selection input.

 Objective

To design, simulate, and synthesize an 8-bit ALU using Verilog HDL and understand the basic operations of digital circuits.

 ALU Operations

The ALU supports the following operations:

Sel| Operation| Description
000| Addition| A + B
001| Subtraction| A - B
010| AND| A & B
011| OR| A | B
100| XOR| A ^ B

Other selection values produce zero.

 Input and Output Signals

Inputs

- A [7:0] – 8-bit input A
- B [7:0] – 8-bit input B
- Sel [2:0] – Operation selection input

Outputs

- Result [7:0] – 8-bit operation result
- CarryOut – Carry output
- Zero – Indicates whether the result is zero

 Tools and Technologies

- Verilog HDL
- Icarus Verilog
- GTKWave
- Yosys Synthesis Tool
- Ubuntu Linux

 Project Structure

- "alu.v" – Main ALU design
- "tb_alu.v" – Testbench for simulation
- "alu.vcd" – Simulation waveform data
- "alu_tb" – Simulation executable
- "Waveform.png" – Simulation waveform screenshot
- "synthesized_alu.v" – Synthesized Verilog netlist
- "synthesis_report.txt" – Yosys synthesis report
- "alu_circuit.png" – ALU circuit diagram
- "alu_circuit.dot" – Circuit graph source

 How to Run the Project

1. Compile the Verilog files

iverilog -o alu_tb alu.v tb_alu.v

2. Run the simulation

vvp alu_tb

3. View the waveform

gtkwave alu.vcd

4. Perform synthesis using Yosys

yosys -p "read_verilog alu.v; synth -top alu; stat"

 Testing

The testbench verifies:

1. Addition
2. Subtraction
3. Bitwise AND
4. Bitwise OR
5. Bitwise XOR
6. Zero result condition

 Results

The ALU design was simulated using a Verilog testbench. Waveform data was generated, and the design was synthesized using Yosys.

The synthesis report and circuit diagram are included in this repository.

 Future Improvements

- Add more arithmetic operations.
- Extend the ALU to 16-bit or 32-bit.
- Implement additional status flags.
- Test the design on FPGA hardware

Project: 8-Bit ALU Using Verilog HDL
