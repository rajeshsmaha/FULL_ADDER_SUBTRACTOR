# FULL ADDER AND SUBTRACTOR

## EXP NO:3 FULL ADDER AND SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

## AIM:

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

## EQUIPMENTS REQUIRED:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

## Full Adder and Full Subtractor

## FULL ADDER:
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

## FULL SUBTRACTOR:

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

## Truthtable:
FULL ADDER:


![full-adder2](https://github.com/user-attachments/assets/b89c130b-0d10-4c30-8194-d7cd8f5adda7)

FULL SUBTRACTOR:

![full-subtractor2](https://github.com/user-attachments/assets/31efd26a-5553-4798-a5fc-7f6e520987e4)

## PROCEDURE:

Write the detailed procedure here

## PROGRAM:


FULL ADDER:
~~~
module fulladder (a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum = ((a^b)^cin);
assign carry = ((a&b)|(cin&(a^b)));
endmodule
~~~

FULL SUBTRACTOR:
~~~
module fullsubtractor(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference=((a^b)^bin);
assign borrow=((~a&b)|(bin&(~(a^b))));
endmodule
~~~

## RTL OUTPUT:

FULL ADDER:

![Screenshot 2024-11-19 085019](https://github.com/user-attachments/assets/1d4b0fbb-f9a6-4074-ac7c-565ea2557b8b)

FULL SUBTRACTOR:

![Screenshot 2024-11-19 091018](https://github.com/user-attachments/assets/952ff071-ff77-4afd-9cc7-faa0ec9482ad)


## OUTPUT WAVEFORM:
FULL ADDER:

![Screenshot 2024-11-19 085835](https://github.com/user-attachments/assets/a2daf309-f3a4-44ef-9080-5fab58b55441)

FULL SUBTRACTOR:

![Screenshot 2024-11-19 091315](https://github.com/user-attachments/assets/a60e0f8c-d1a8-4535-b779-b3d1ac83ed31)



## RESULT:

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



