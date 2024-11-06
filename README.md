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
![WhatsApp Image 2024-11-05 at 11 48 56 AM](https://github.com/user-attachments/assets/3f784f87-d891-4f50-9ab5-b2372e676ec5)

**Procedure**

Write the detailed procedure here

**Program:**
```
module exp4(a,b,cy,sm,df,bo);
input a,b;
output sm,cy,df,bo;
xor(sm,a,b);
and(cy,a,b);
xor(df,a,b);
and(bo,~a,b);
endmodule
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:24901330
*/
```
**RTL Schematic**
![ep4 rtl view](https://github.com/user-attachments/assets/502df6c5-5769-4e70-a38c-5aa478947a3f)

**Output Timing Waveform**
![rtl waveform exp4](https://github.com/user-attachments/assets/17fdec3d-4f7b-4881-a308-a96b72d7c3b8)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



