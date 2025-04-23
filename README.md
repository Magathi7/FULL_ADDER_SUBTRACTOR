# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

FULL ADDER:

![image](https://github.com/user-attachments/assets/f7c9d067-1896-4737-8416-6c4d017c9cc3)

FULL SUBTRACTOR:

![image](https://github.com/user-attachments/assets/4adf89f1-9965-4c26-b169-5b9ad088f565)

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by:MAGATHI D

RegisterNumber:212223040108

module fulladd_top(a,b,c,sum,carry,BO,DIFF);

input a,b,c;

output sum,carry,BO,DIFF;

assign sum=a^b^c;

assign carry= a&b | a&c | b&c;

wire a0;

not (a0,a);

assign BO= b&c | a0&c | a0&b;

assign DIFF=a^b^c;

endmodule

*/

**RTL Schematic**

FULL ADDER:

![image](https://github.com/user-attachments/assets/667e9ac5-0688-45fb-9c69-ef8724253f10)

FULL SUBTRACTOR:

![image](https://github.com/user-attachments/assets/99f2d56f-9cc8-4d67-ab21-fdde61118a13)

**Output Timing Waveform**

FULL ADDER:

![image](https://github.com/user-attachments/assets/704c2f69-a89c-4f86-bdee-2882590898c8)


FULL SUBTRACTOR:


![image](https://github.com/user-attachments/assets/7391fd63-36f1-4dda-be88-80d73bf57b49)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



