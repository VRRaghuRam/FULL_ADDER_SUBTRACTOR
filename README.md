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

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: raghu ram v r
RegisterNumber: 24900512
*/
```
**full adder**
module full_adder(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        

and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);

or(carry,w2,w3,w4);
endmodule

**full subtractor**
module full_subtracter(a,b,Bin,BO,DIFF);![Screenshot 2024-03-28 154124](https://github.com/priyadharshini210/FULL_ADDER_SUBTRACTOR/assets/148514638/dc75caa2-c185-4074-b910-18363ceccbf4)

input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
  assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
```
**RTL Schematic**
![314523275-2d86d03d-584f-4527-b9fb-d9d892f1c056](https://github.com/priyadharshini210/FULL_ADDER_SUBTRACTOR/assets/148514638/f68047b7-4451-4baa-88b8-6d21af3a423a)
![314523356-d9734426-62a3-4b80-a363-2e1869805d8c](https://github.com/priyadharshini210/FULL_ADDER_SUBTRACTOR/assets/148514638/de720dfc-9d76-4cbf-b05b-16255a1ce86b)

**Output Timing Waveform**

**Full adder**
![Screenshot 2024-03-28 154124](https://github.com/priyadharshini210/FULL_ADDER_SUBTRACTOR/assets/148514638/cd86403a-9bfd-4442-ad05-96204ce44a6c)
**Full subractor**
![Screenshot 2024-03-28 154106](https://github.com/priyadharshini210/FULL_ADDER_SUBTRACTOR/assets/148514638/e86ad945-b84f-4510-83bc-ca30eb56bedd)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



