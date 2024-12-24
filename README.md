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
Program to design a full adder and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by:G.T.GOWTHAM
RegisterNumber: 24901330

Full Adder

module exp4(df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule
Full Subtractor

module full_subtractor(diff, borrow, a, b, bin);
  output diff;
  output borrow;
  input a;
  input b;
  input bin;
  assign diff = a ^ b ^ bin;
  assign borrow = (~a & b) | (~(a ^ b) & bin);
endmodule


```
RTL Schematic Full Adder
![394118789-993f7ad7-9159-46a4-8769-48a7a7b701f3](https://github.com/user-attachments/assets/3ab9325e-31fb-4a73-8a18-cc06679861aa)

Full Subtractor
![394120412-5d7d76ec-1151-443f-adde-8d9412dd223b](https://github.com/user-attachments/assets/e9dc8384-b8d7-4bac-9b02-e7e1cb40a8af)

Output Timing Waveform Full Adder
![3rd](https://github.com/user-attachments/assets/5b38fa88-8ede-4a29-a6a8-55610cbc7826)

Full Subtractor
![4th](https://github.com/user-attachments/assets/e1fac703-f516-4031-9e91-e9113f3b3519)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



