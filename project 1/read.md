# 1-Bit Full Adder using Verilog HDL

## Overview

This project implements a 1-Bit Full Adder using Verilog HDL. A Full Adder performs the addition of three binary inputs (A, B, Cin) and produces two outputs:

- Sum
- Carry Out (Cout)

## Features

- Verilog HDL implementation
- Complete testbench
- Truth table verification
- Simulation waveform
- Compatible with ModelSim, Icarus Verilog and GTKWave

## Project Structure

```
src/
testbench/
simulation/
images/
README.md
```

## Inputs

- A
- B
- Cin

## Outputs

- Sum
- Cout

## Logic Equations

Sum = A XOR B XOR Cin

Cout = (A AND B) OR (B AND Cin) OR (A AND Cin)

## Truth Table

|A|B|Cin|Sum|Cout|
|--|--|---|---|----|
|0|0|0|0|0|
|0|0|1|1|0|
|0|1|0|1|0|
|0|1|1|0|1|
|1|0|0|1|0|
|1|0|1|0|1|
|1|1|0|0|1|
|1|1|1|1|1|

## Simulation

Compile:

```
iverilog -o fulladder src/full_adder.v testbench/full_adder_tb.v
```

Run:

```
vvp fulladder
```

Generate waveform:

```
gtkwave full_adder.vcd
```

## Output

The simulation verifies all eight input combinations and confirms the correctness of the Full Adder.

## Author

Your Name
