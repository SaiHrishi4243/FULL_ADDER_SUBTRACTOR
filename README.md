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

![Screenshot 2024-11-28 113315](https://github.com/user-attachments/assets/0b54a790-e2aa-45f5-bdcc-f57cc98b8a7c)

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: Sai Hrishi M    RegisterNumber: 24900846 */

```
module full(A,B,Cin,Bin,Sum,Carry,Diff,Borrow);
input A,B,Cin,Bin;
output Sum,Carry,Diff,Borrow;
assign Sum=A^(B^Cin);
assign Carry=(A&B)|(A&Cin)|(B&Cin);
assign Diff=A^(B^Bin);
assign Borrow=(~A&Bin)|(~A&B)|(B&Bin);
endmodule
```

**RTL Schematic**

![Screenshot 2024-11-28 112108](https://github.com/user-attachments/assets/350cb978-cb6e-4eca-89ba-3ac3bba1557f)

**Output Timing Waveform**

![Screenshot 2024-11-28 112245](https://github.com/user-attachments/assets/939bab87-7f2c-4e52-989e-e409934c08b8)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



