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

**Procedure**
1.Type the program in Quartus software.
2.Compile and run the program.
3.Generate the RTL schematic and save the logic diagram.
4.Create nodes for inputs and outputs to generate the timing diagram.
5.For different input combinations generate the timing diagram.

**PROGRAM**

 Program for 4 Bit Ripple Counter and verify its truth table in quartus using Verilog programming.
```
module ex12(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out-1;
end
endmodule
```

**RTL LOGIC FOR 4 Bit Ripple Counter**
<img width="1472" height="773" alt="Screenshot 2025-12-15 133719" src="https://github.com/user-attachments/assets/5f16a55c-70cc-4ee3-9374-4d19ddc4c56d" />

**TIMING DIGRAMS FOR 4 Bit Ripple Counter**
<img width="1686" height="411" alt="Screenshot 2025-12-15 133815" src="https://github.com/user-attachments/assets/c8da765e-e30b-4ef1-8713-0bd9abf5538c" />

**RESULTS**
Thus 4-bit ripple counter is implemented using verilog and the functionality is validated using function tables.
