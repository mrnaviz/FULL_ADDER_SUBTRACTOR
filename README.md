# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.
### DEVELOPED BY : NAVEEN KUMAR B
### REG NO :212222230091


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
### FULL ADDER
```
module ex04(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=(a^b^cin);
assign carry=((a&b) | (b&cin) | (cin&a));
endmodule
```

### FULL SUBTRACTOR
```
module ex04.2(a,b,bin,borr,diff);
input a,b,bin;
output borr,diff;
assign diff=(a^b^bin);
assign borr=((~a&b) | (b&bin) | (bin&~a));
endmodule

```
**RTL Schematic**
### FULL ADDER
![image](https://github.com/user-attachments/assets/f0ec5086-42d4-4720-a397-0986b4c37590)


### FULL SUBTRACTOR
![image](https://github.com/user-attachments/assets/d5123ac4-391b-4cc5-b510-a7ac49341448)


**Output Timing Waveform**
### FULL ADDER
![image](https://github.com/user-attachments/assets/8f972f88-f2b6-4860-be1f-94b91f676ff1)


### FULL SUBTRACTOR
![image](https://github.com/user-attachments/assets/fe8b5442-62d3-4cf2-adb1-d51ff4a31ef9)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



