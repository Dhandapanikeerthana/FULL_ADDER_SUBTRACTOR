## FULL_ADDER_SUBTRACTOR
## DEVELOPED BY: KEERTHANA D
## REG NO: 212224040155

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

  ![Screenshot 2025-04-15 232557](https://github.com/user-attachments/assets/55bce77d-9494-44bf-85eb-50390eafb26c)
  
  ![Screenshot 2025-04-15 232616](https://github.com/user-attachments/assets/75812374-bddf-4c87-87a7-6cea1b4bd444)



**Procedure**
```
  1.Type the program in Quartus software.
  2.Compile and run the program.
  3.Generate the RTL schematic and save the logic diagram.
  4.Create nodes for inputs and outputs to generate the timing diagram.
  5.For different input combinations generate the timing diagram.
```
 
**Program:**
```

FULL ADDER

module exp4(a,b,c,sum, carry);
input a,b,c;
output sum, carry;
wire w1,w2,w3;
assign sum=a^b^c;
assign w1=a&b;
assign w2=b&c;
assign w3=c&a;
assign carry=w1|w2|w3;
endmodule;

FULL SUBTRACTOR

module fs(df, bo, a, b, bin);
input a,b,bin;
output df,bo;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule;
```

**RTL Schematic**

 ![Screenshot (43)](https://github.com/user-attachments/assets/8dac6c65-f418-473d-8f9b-31765c6b2c6f)
 ![Screenshot (45)](https://github.com/user-attachments/assets/b07d4597-77f0-4de2-bf62-e4881a86364c)


**Output Timing Waveform**

 ![Screenshot (44)](https://github.com/user-attachments/assets/7bebeeb0-67db-47b5-b8c3-30c8afb18830)
 ![Screenshot (46)](https://github.com/user-attachments/assets/4df8051e-1036-4a32-b2eb-c9a274118663)


**Result:**

  Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



