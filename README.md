# FULL_ADDER_SUBTRACTOR
# Developed By: Manikandan G
# Ref no: 25002356



Implementation-of-Full-Adder-and-Full-subtractor-circuit

# AIM:

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

# Equipments Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

# Full Adder and Full Subtractor:

# Full Adder:

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

# Full Subtractor:

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

# Truthtable:


<img width="1166" height="678" alt="image" src="https://github.com/user-attachments/assets/a5d0346e-d71e-44fd-9ccb-0dfcc4f3c530" />

# Procedure :

Write the detailed procedure here 1.Create a new project in Quartus II and open a Block Diagram/Schematic file. 2.Place logic symbols and connect inputs A, B, Cin and outputs Sum, Cout. 3.Implement logic: Sum = A ⊕ B ⊕ Cin, Cout = AB + Cin(A ⊕ B). 4.Compile and simulate to verify the output waveform.

# Program:
```
module full_add_sub(a,b,cin,sum,diff,carry,borrow);
input a,b,cin;
output sum,diff,carry,borrow;
assign sum = (a^b^cin);
assign carry = (a&b)|(a&cin)|(b&cin);
assign diff = (a^b^cin);
assign borrow = (~a&cin)|(~a&b)|(b&cin);
endmodule
```


# RTL Schematic:

<img width="731" height="633" alt="Screenshot 2025-11-24 221942" src="https://github.com/user-attachments/assets/0c80d5cd-604c-4cf2-ba78-df2c3789ec05" />


# Output Timing Waveform:
<img width="1826" height="980" alt="Screenshot 2025-11-24 222225" src="https://github.com/user-attachments/assets/b3b85662-7025-44fd-b401-ad13dc529cce" />

# Result:
verified
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



