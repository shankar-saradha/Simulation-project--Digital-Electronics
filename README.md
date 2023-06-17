# TITTLE
## MINIMISE THE FUNCTION USING K MAP F(A,B,C)=A'B' +BC'+ BC + A'B'C' AND SIMULATE THE LOGIC DIAGRAM USING VERILOG


# THEORY
## K Map:

A Karnaugh map, also known as a K-map, is a graphical representation used to simplify Boolean functions.
It provides a systematic method for grouping adjacent 1s in a truth table or a Boolean expression.
The K-map is organized in a grid format, with the input variables represented along the rows and columns.
In this case, we have a 3-variable K-map for the function F(A, B, C).

## Minimization Process:

To minimize a Boolean function using a Karnaugh map, we follow these steps:
a. Fill the K-map with the corresponding truth table values of the Boolean function.
b. Group adjacent 1s in the K-map to identify patterns.
c. Each group should contain 2^n adjacent 1s (where n is a positive integer).
d. Determine the minimal expression for each group using Boolean algebra.
e. Combine the minimal expressions obtained from each group to form the simplified expression for the function.

## Logic Diagram Simulation using Verilog:

Verilog is a hardware description language (HDL) used for designing and simulating digital systems.
To simulate a logic diagram using Verilog, we define a module that represents the circuit and its inputs/outputs.
The combinational logic is implemented inside an always block, where the output is calculated based on the input values.
The reg data type is used to declare the output as it is driven by the procedural block.
The Verilog code can be compiled and simulated using a Verilog simulator or an HDL tool.
# LOGIC DIAGRAM
![1](https://github.com/shankar-saradha/Simulation-project--Digital-Electronics/assets/93978702/bfec80e4-6fc1-4c4b-8d2c-0b86c3cae118)

# NETLIST DIAGRAM

# TIMING DIAGRAM
![de lol ](https://github.com/shankar-saradha/Simulation-project--Digital-Electronics/assets/93978702/c8c9fa46-3129-4e37-b134-b8f5c521af85)

# PROGRAM
```c 
module logic_circuit(
  input A,
  input B,
  input C,
  output reg F
);

  always @(A, B, C) begin
    F = (~A & B) | (B & ~C) | (B & C) | (A & ~B & ~C);
  end

endmodule
```
# REFERENCE
