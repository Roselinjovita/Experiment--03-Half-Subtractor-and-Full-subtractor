```
Developed by: S.ROSELIN MARY JOVITA
Register Number:212222230122
```
# Experiment 04 Half Subtractor and Full subtractor
## Implementation of Half subtractor and Full subtractor circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
 Hardware – PCs, Cyclone II , USB flasher
 
 Software – Quartus prime
 
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 

1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output to represnt onre for differnce and the other for borrow.

5.End the verilog program using keyword endmodule.


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
```
HALF SUBRACTOR
module exp4(A,B,Bin,Difference,Borrow);
input A,B,Bin;
output Difference,Borrow;
assign Borrow=(~A&(B^Bin)|(B&Bin));
assign Difference=(A^B^Bin);
endmodule
```
```
FULL SUBRACTOR
module exp4fullsub(A,B,Bin,Difference,Borrow);
input A,B,Bin;
output Difference,Borrow;
assign Difference=(A^B^Bin);
assign Borrow =((~A)&B)| ((~A^B)&Bin);
endmodule 
```
*/

## Truthtable

## HALF SUBTRACTOR
![hst](https://github.com/Roselinjovita/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119104296/7ab4793f-7da7-4ea6-aabb-efc018ffb6b2)

## FULL SUBRTACTOR
![ft](https://github.com/Roselinjovita/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119104296/48786833-a936-48e5-9bcb-7e302d783814)




##  RTL realization:

## HALF SUBRTACTOR
![HALFSUB4RTL](https://github.com/Roselinjovita/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119104296/5bf92253-23ac-4e2a-9b32-2a35c8f4a705)

## FULL SUBRTACTOR
![fullsubrtl](https://github.com/Roselinjovita/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119104296/11a83420-a514-4f54-bf18-1a2b46266fa0)




## Timing diagram :

## HALF SUBTRACTOR
![HALFSUB4WF](https://github.com/Roselinjovita/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119104296/9ac8ed12-ab5c-4c49-8da8-6f4d72f2fc9c)

## FULL SUBTRACTOR

![FULLSUBWF](https://github.com/Roselinjovita/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119104296/b9b66c70-7a0a-4e4d-baea-8ad5f1e33de1)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
