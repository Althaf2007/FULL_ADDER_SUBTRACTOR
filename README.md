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

**Procedure**

Write the detailed procedure here
```
1.Type the program in Quartus software. 
2.Compile and run the program.
3.Generate the RTL schematic and save the logic diagram.
4.Create nodes for inputs and outputs to generate the timing diagram. 
5.For different input combinations generate the timing diagram.
```

**Program:**

Program to design a full adder and full subtractor circuit and verify its truth table in quartus using Verilog programming.

```
module fulladder(A,B,Cin,sum,carry);
input A,B,Cin;
output sum,carry;
assign sum = (A ^ B ^ Cin);
assign carry = ((A & B) | ((A ^ B) & Cin));
endmodule
```

```
module fullsub(a,b,bin,diff,borr);
input a,b,bin;
output diff,borr;
assign diff = (a ^ b ^ bin);
assign borr = ((~a & b) | (b & bin) | (~a & bin));
endmodule
```

Developed by:K.Mohamed Althaf

RegisterNumber:24005994

**Truthtable**

![fa t](https://github.com/user-attachments/assets/5c813a0e-c8de-4129-b11f-a6b996dcb50e)

![fs t](https://github.com/user-attachments/assets/ab105be3-2883-401d-978b-b326fb812b06)


**RTL Schematic**

![Screenshot 2024-11-18 141645](https://github.com/user-attachments/assets/e020f123-66dd-4c61-b666-de79fcbae30d)

![Screenshot 2024-11-18 142229](https://github.com/user-attachments/assets/bf8d5545-f2a8-4c41-8f59-0cf54630981f)

**Output Timing Waveform**

![Screenshot 2024-11-18 141620](https://github.com/user-attachments/assets/9a597f5b-2b8c-4464-9911-51ac2dc7d542)

![Screenshot 2024-11-18 142201](https://github.com/user-attachments/assets/be86cc51-8933-4a53-a538-23ecb5511a01)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



