# Experiment--04-Implementation-of-combinational-logic-using-universal-gates-
 ## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.
F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate


## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

## Theory
 A universal gate is a logic gate which can implement any Boolean function without the need to use any other type of logic gate. The NOR gate and NAND gate are universal gates. This means that you can create any logical Boolean expression using only NOR gates or only NAND gates. In practice, this is advantageous since NOR and NAND gates are economical and easier to fabricate than other logic gates. Similarly, an OR gate is typically realised as a NOR gate followed by an inverter.
 
 
 


## Procedure

1. Create a project with required entities.

2. Create a module along with respective file name.

3. Run the respective programs for the given boolean equations.

4. Run the module and get the respective RTL outputs.

5. Create university program(VWF) for getting timing diagram.

6. Give the respective inputs for timing diagram and obtain the results.





## Program:
/*
Program to design a Implementation of combinational logic using universal gates-  and verify its truth table in quartus using Verilog programming.
Developed by: 212221230025
RegisterNumber: Evangelin.S 
*/

```
## F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate

module Combination(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R;
assign P = C&(~B)&(~A);
assign Q = D&(~C)&(~A);
assign R = (~C)&B&(~A);
assign F = (~P&~Q&~R);
endmodule
```

## F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
```
module norcombination(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R,S;
assign P = C&(~B)&A;
assign Q = D&(~C)&A;
assign R = C&(~B)&A;
assign S = ~(P|Q|R);
not(F,S);
endmodule
```

## Output:
## F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
## Truthtable
![image](https://user-images.githubusercontent.com/94219798/167289038-a653c78c-c6ff-42c7-95d3-1ef95dd14bec.png)



##  RTL realization
![image](https://user-images.githubusercontent.com/94219798/167289040-0d3933c1-9157-42c7-b648-0c627ca11d27.png)


## Timing diagram 
![image](https://user-images.githubusercontent.com/94219798/167289046-1f20023e-aa37-4611-ba61-39d59a4afcf6.png)

## F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Truthtable
![image](https://user-images.githubusercontent.com/94219798/167289066-fcdcf8c5-d04e-45b8-b072-e1c05f261a55.png)


## RTL Realization
![image](https://user-images.githubusercontent.com/94219798/167289082-a1e0b893-682d-4a55-9fd7-c5cab943895a.png)


## Timing diagram
![image](https://user-images.githubusercontent.com/94219798/167289096-bf4bd5b7-9e8d-489e-b86c-8890c9438fdd.png)


## Result:
 Thus implementation of logic functions using NAND and NOR gates is done and its operation is verified in Quartus using Verilog programming.
