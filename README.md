# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

## Developed by:Mahajannai.R 
## RegisterNumber:*/212224230147
## Date: 19.03.2025

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

![ha (2)](https://github.com/user-attachments/assets/d58074b4-45c8-4535-9f2d-7f923d687316)

![hs (2)](https://github.com/user-attachments/assets/3e34a9d5-7239-4c60-b0f4-50d2ba7f7e48)
**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

### Half Adder:
```
 module ha(a,b,sum,carry);
 input a,b;
 output sum,carry;
 assign sum=(a^b);
 assign carry=(a&b);
 endmodule
```

### Half Subtractor:
```
 module hs(a,b,difference,borrow);
 input a,b;
 output difference,borrow;
 assign difference=(a^b);
 assign borrow=(~a&b);
 endmodule
```

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.



**RTL Schematic**

 ![ha (3)](https://github.com/user-attachments/assets/99ab04ad-8be7-41f0-ad68-b31c12e56d44)
 ![hs (3)](https://github.com/user-attachments/assets/3e2eb68e-333e-4b8a-8c49-9a1cc3d23efa)

**Output/TIMING Waveform**

![ha](https://github.com/user-attachments/assets/20919a2b-e12a-4708-b502-8f8853644047)
![hs](https://github.com/user-attachments/assets/bf1c0504-e7fc-4d70-aa46-5081adc98c5a)


**Result:**
Thus the half adder and half subtractor are studied and the truth table table,logic gates are verified in Quartus II using Verilog programming.
