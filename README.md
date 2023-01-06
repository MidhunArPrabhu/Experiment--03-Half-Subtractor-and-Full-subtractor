# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
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

### PROCEDURE:

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.  
Developed by: MIDHUN AZHAHU RAJA P  
RegisterNumber:  22008311

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### PROGRAM:  


HALF ADDER:  

module secexp(a,b,difference,borrow);  
input a,b;  
output difference,borrow;  
assign difference=(a^b);  
assign borrow=(~a&b);  
endmodule  

FULL ADDER:

module secexp(a,b,c,difference,borrow);
input a,b,c;
output difference,borrow;
assign borrow=(~a&(b^c)|(b&c));
assign difference=(a^b^c);
endmodule

### LOGIC GATES :

AND GATE :

<img width="145" alt="210804186-b2fd26ff-4908-4580-b064-b49bb33c4b6b" src="https://user-images.githubusercontent.com/118054670/211067110-3f48e804-9284-408a-ac7c-2c5d43cee25a.png">

OR GATE :

![210806829-e8faa983-2648-444c-8290-2b1082744d52](https://user-images.githubusercontent.com/118054670/211067279-90a43b92-1543-4c1b-9394-e82c15495807.jpg)

NOT GATE : 

<img width="153" alt="210804437-c8289936-6877-4420-ac8e-b6de9497de25" src="https://user-images.githubusercontent.com/118054670/211067802-a0a0d45d-573b-4899-8564-8d08a53f8425.png">

XOR GATE :

<img width="157" alt="210804204-908a6987-8a7f-449d-b33b-42b08166e0d9" src="https://user-images.githubusercontent.com/118054670/211067911-0fb99182-1b1a-4f16-9bd8-d61c5a477b57.png">


###OUTPUT :

### TRUTH TABLE :

HALF SUBTRACTOR:

![210802334-f7ee77a0-38db-4917-986a-e0c154cd17a8](https://user-images.githubusercontent.com/118054670/211055581-ed8eef1c-68a9-43c4-a4b1-fa144f4487be.jpg)

FULL SUBTRACTOR:

<img width="162" alt="210804152-d3067756-db97-49b6-81f9-859224ab815e" src="https://user-images.githubusercontent.com/118054670/211066726-53d1cea4-2666-44cc-a9d0-6c6f868087ca.png">

### RTL :
RTL FOR HALF ADDER :  

![Screenshot_20230106_095516](https://user-images.githubusercontent.com/118054670/211056187-7fd555c3-4e3c-4546-a6f2-4629429e67fe.png)

RTL FOR FULL ADDER:

![Screenshot_20230106_100128](https://user-images.githubusercontent.com/118054670/211056497-4153e7f1-1765-407c-a54c-665c31d14348.png)

### TIMING DIAGRAM

HALF SUBTRACTOR

![Screenshot_20230106_104953](https://user-images.githubusercontent.com/118054670/211064357-9e4829db-4d72-4c9b-af29-ec9043db20ec.png)


![Screenshot_20230106_103940](https://user-images.githubusercontent.com/118054670/211064304-8b2aec64-d0af-4676-b3a0-dd4a5a8ef3b4.png)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
