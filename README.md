# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## NAME: Shaik Samreen 
## REGISTER NUMBER: 23013412
## AIM:
  To design a half subtractor and full subtractor circuit and verify its truth table in Quartus 
  using Verilog programming.

## Equipments Required:
  Hardware – PCs, Cyclone II , USB flasher
  Software – Quartus prime
  
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor and Full Subtractor
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
   1.Use module projname(input,output) to start the Verilog programming.
   2.Assign inputs and outputs using the word input and output respectively.
   3.Use defined keywords like wire,assign and required logic gates to represent the boolean 
   expression.
   4.Use each output to represent one for difference and the other for borrow.
   5.End the verilog program using keyword endmodule
## Program:
/*

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
## half subractor
```
   module halfsub(a,b,difference,borrow);
   input a,b;
   output difference,borrow;
   assign difference = (a^b);
   assign borrow = (~a&b);
   endmodule
```
## full subractor 
```
   module fullsub(a,b,c,difference,borrow);
   input a,b,c;
   output difference,borrow;
   assign difference=(a^b^c);
   assign borrow=(~a&(b^c)|(b&c));
   endmodule
```
*/

## Output:

## Truthtable:
## half subtractor
![293377464-aecfab06-dee6-4b34-9c23-b8133695a5fa](https://github.com/samreen-sk/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149347632/55a8aedc-cc5f-45f3-b004-ef59b688fdde)

##  full subtractor

![293378094-54f8da81-7208-4a3e-a546-f70d8cd4a75a](https://github.com/samreen-sk/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149347632/e6a465fc-2aa3-48f7-a764-ca0a8621689e)

##  RTL realization
## half subrtactor:
![293378300-2cf30aeb-bd04-49dd-a57e-93c3f563ffd3](https://github.com/samreen-sk/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149347632/2294ab9b-9545-4591-b5cf-d191109e2f12)
## full subtractor:

![293378859-d2fb8b8a-ea10-40c2-8b5e-3f72bc0c2839](https://github.com/samreen-sk/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149347632/3d4b4646-da83-426a-80db-5c2588dc0323)

## Timing diagram :
## half subtractor

![293379127-15828c87-5b81-4f27-8e09-07ee7bc0269a](https://github.com/samreen-sk/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149347632/1161b425-4459-4cfa-bcd2-65a2b7abb8fd)
## full subtractor
![293379255-47b386b0-668c-46a5-b831-8e2ddfd823bb](https://github.com/samreen-sk/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149347632/d4c5e902-928e-4fab-a8bf-2ce1324d9c6a)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
