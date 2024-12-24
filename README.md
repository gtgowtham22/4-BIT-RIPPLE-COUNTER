# 4-BIT-RIPPLE-COUNTER

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

Procedure

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

Program:
```
Program to design a full adder and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: G.T.GOWTHAM
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
![12 1](https://github.com/user-attachments/assets/a343f20a-52bd-4968-b7c3-d0aea8f8dcee)

Full Subtractor 

![12 2](https://github.com/user-attachments/assets/82e6f70e-7896-4e5c-93ee-01ffeab385f7)

Output Timing Waveform Full Adder
![12 3](https://github.com/user-attachments/assets/dfa81746-0a9f-4998-b073-c5f963a63cfe)

Full Subtractor 
![12 4](https://github.com/user-attachments/assets/34c4f73a-78e9-455f-9eb1-71d082441d68)

Result:

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
