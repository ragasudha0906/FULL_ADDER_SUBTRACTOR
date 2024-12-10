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

![Screenshot 2024-12-10 141656](https://github.com/user-attachments/assets/a6f94ffe-5cc4-466a-b40e-833888583471)
![Screenshot 2024-12-10 141719](https://github.com/user-attachments/assets/0fb6c224-b4c6-4f95-86ec-20591bc3fad4)

**Procedure**
Write the detailed procedure here
1. Write the code in Quartus software by creating a new project wizard.
2. Run the program to get output.
3. Then open RTL viewer and download that image.
4. Open new file with University program VWF
5. Set end timer and execute, then download the waveform.
**Program:**
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by:Ragasudha R  RegisterNumber:24900684*/
```
/full adder module EXP_4(sum, cout, a, b, cin);
output sum;
output
cout;
input a;
input b;
input cin;
internal nets wire sl,cl,c2;
Instantiate logic gate primitives
xor(sl,a,b);
and(cl,a,b);
xor(sum, sl, cin);
and (c2, sl,cin);
or (cout, c2,cl);
endmodule
```
```
module EXP_4_2 (df, bo, a, b, bin);
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
```


**RTL Schematic**

![WhatsApp Image 2024-11-20 at 08 22 50_42f1ae35](https://github.com/user-attachments/assets/06e67e87-2bc5-42d9-9776-8be8e85fed1a)

![WhatsApp Image 2024-11-20 at 08 22 50_3ecd8883](https://github.com/user-attachments/assets/a4e7b2dd-8d27-4be6-9056-ae9a9b91e395)

**Output Timing Waveform**

![WhatsApp Image 2024-11-20 at 08 22 51_96992e44](https://github.com/user-attachments/assets/4beba69e-c9eb-43b3-8519-33b632964cd8)

![WhatsApp Image 2024-11-20 at 08 22 52_4e0d0074](https://github.com/user-attachments/assets/7c510a6b-3b9e-4779-9d04-f688bf44c7ce)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



