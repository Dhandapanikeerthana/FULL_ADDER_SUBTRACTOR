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
full adder
![full adder](https://github.com/user-attachments/assets/4c72e512-3899-4d0b-b6b1-fb64de39647f)


full subtractor
![full subtractor](https://github.com/user-attachments/assets/530eeb43-40d6-4ad7-b6c9-511604838106)


**Procedure** 

Full adder
A full adder is a combinational logic circuit that adds three one-bit binary numbers to produce a two-bit output. The output is the sum and the carry value. The truth table for a full adder can be used to implement the full adder logic. 
Full subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits: A (minuend), B (subtrahend), and Bin (borrow-in). It produces two outputs: D (difference) and Bout (borrow out). 

**Program:**

 Developed by:ATCHAYA B
 RegisterNumber:24900268
 
 Full Adder
 module adder(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule


Full Subtractor
module subtractor(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule



**RTL Schematic**

Full Adder
![exp 4 rtl](https://github.com/user-attachments/assets/fe9041d0-f80d-4eac-8aed-93de624924e0)
Full Subtractor
![exp 4 1 rtl](https://github.com/user-attachments/assets/1518c2cd-d3ec-49d5-8089-7b8d9d946a63)



**Output Timing Waveform**

Full Adder
![exp 4](https://github.com/user-attachments/assets/ac2fdf67-a7f1-478a-bd0d-2f3576fa6ca1)
Full Subtractor
![exp 4 1](https://github.com/user-attachments/assets/472b1a62-b0d4-4e5f-b6fe-dfc266fb4542)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



