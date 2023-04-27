# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime

## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

## Procedure:
The input and output variables are allocated with letter symbols. The exact truth table that defines the required relationships between inputs and outputs is derived. The simplified Boolean function is obtained from each output. The logic diagram is drawn.
## Program:
```
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: Laakshit D
RegisterNumber: 212222230071
*/
module Combinational(A,B,C,D,W,X,Y,Z,F1,F2);
input A,B,C,D,W,Y,X,Z;
output F1,F2;
wire A1,A2,A3,A4,A5,B1,B2,B3,B4,B5;
assign A1 = ((~A)&(~B)&(~C)&(~D));
assign A2 = (A&(~C)&(~D));
assign A3 = ((~B)&C&(~D));
assign A4 = ((~A)&B&C&D);
assign A5 = (B&(~C)&D);
assign B1 = (X&(~Y)&Z);
assign B2 = ((~X)&(~Y)&Z);
assign B3 = ((~W)&X&Y);
assign B4 = (W&(~X)&Y);
assign B5 = (W&X&Y);
assign F1 = (A1|A2|A3|A4|A5);
assign F2 = (B1|B2|B3|B4|B5);
endmodule
```
## Output:
## RTL realization
### F1
![Screenshot 2023-04-27 125717](https://user-images.githubusercontent.com/119559976/234790808-84a3b29e-6026-43b6-a83d-fa56dd5aeead.png)
### F2
![Screenshot 2023-04-27 125648](https://user-images.githubusercontent.com/119559976/234790916-2d1a91ce-9053-4558-a93f-fd8efb365d6b.png)
## Timing Diagram:
![Screenshot 2023-04-27 125737](https://user-images.githubusercontent.com/119559976/234791116-a9287eab-7c1c-48ce-8d02-baa3e9c66fcd.png)
## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
