# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D F2=xy’z+x’y’z+w’xy+wx’y+wxy

1.AND gate The AND gate is an electronic circuit that gives a high output (1) only if all its inputs are high. A dot (.) is used to show the AND operation i.e. A.B or can be written as AB Y= A.B

2.OR gate The OR gate is an electronic circuit that gives a high output (1) if one or more of its inputs are high. A plus (+) is used to show the OR operation. Y= A+B

## Procedure
```
### Step 1
Create a project with required entities.

### Step 2
Create a module along with respective file name.

### Step 3
Run the respective programs for the given boolean equations.

### Step 4
Run the module and get the respective RTL outputs.

### Step 5
Create university program(VWF) for getting timing diagram.

### Step 6
Give the respective inputs for timing diagram and obtain the results.
```

## Program:
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by:LOGESHWARI.P
RegisterNumber:212221230055 
*/
## F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
```
module f1(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire p,q,r,s,t;
assign p = (~A & ~B & ~C & ~D);
assign q = (A & ~C & ~D);
assign r = (~B & C & ~D);
assign s = (~A & B & C & D);
assign t = (B & ~C & D);
assign F1 = p | q | r | s | t;
endmodule
```
## F2=xy’z+x’y’z+w’xy+wx’y+wxy
```
module imp(w,x,y,z,F2);
input w,x,y,z;
output F2;
wire p,q,r,s,t;
assign p= (x & ~y & z);
assign q= (~x & ~y & z);
assign r= (~w & x & y);
assign s= (w & ~x & y);
assign t= (w & x & y);
assign F2= p | q | r | s | t;
endmodule
```

## RTL realization
## F1
![243377344-4a0c2912-b4dd-4896-8605-79cbea53db68](https://github.com/logeshwari2004/Experiment--02-Implementation-of-combinational-logic-/assets/94211349/a9aef1af-e9ae-45aa-905c-2a39f2c7348f)
## F2
![243377377-ac278eda-5a27-4658-a1ff-7bba9f8decf9](https://github.com/logeshwari2004/Experiment--02-Implementation-of-combinational-logic-/assets/94211349/2c0b0695-a1a7-4779-85e8-ba468d8bab93)
## Timing Diagram
## F1
![243377392-b09e5fea-aa3b-4ee3-903f-f4d06b30c353](https://github.com/logeshwari2004/Experiment--02-Implementation-of-combinational-logic-/assets/94211349/207891c0-7176-4961-b7c3-454bec447093)
## F2
![243377418-ab8302e6-9378-4200-8d04-914b9b312f1f](https://github.com/logeshwari2004/Experiment--02-Implementation-of-combinational-logic-/assets/94211349/2b59908f-6936-4948-a919-7e5e0abdedfb)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
