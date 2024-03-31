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
FULL ADDER
![316380387-d0433287-bca1-4a42-941b-7ebe73f982fa](https://github.com/RamkumarGunasekaran/FULL_ADDER_SUBTRACTOR/assets/144870820/d2ff3833-f609-4054-af8b-d834a088a135)

FULL SUBRACTOR
![316380435-89454d27-9645-4632-a76b-83fd89b93be1](https://github.com/RamkumarGunasekaran/FULL_ADDER_SUBTRACTOR/assets/144870820/70d90a4d-3b7e-4fd9-9830-4d6cf3fb29c2)

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/
```
module EX04(a,b,c,sum,carry,BO,DIFF);
input a,b,c;
output sum,carry,BO,DIFF;
//FULL ADDER
assign sum = a^b^c;
assign carry = (a&b) | (b&c) | (a&c);
wire a0;
not (a0,a);
//FUKK SUBTRACTOR
assign DIFF = a^b^c;
assign BO = (a0&b) | (b&c) | (a0&c);
endmodule

```

**RTL Schematic**
![Screenshot 2024-03-31 222839](https://github.com/RamkumarGunasekaran/FULL_ADDER_SUBTRACTOR/assets/144870820/c689f8bf-6987-441d-bbcd-4a7780cc638b)


**Output Timing Waveform**
![316380043-ac6a4ddd-bf53-4d24-a049-082f31171294](https://github.com/RamkumarGunasekaran/FULL_ADDER_SUBTRACTOR/assets/144870820/520d4182-9020-46f6-a9d7-cfe4a0719267)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



