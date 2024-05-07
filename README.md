D-FLIPDLOP-NEGEDGE
AIM:

To implement D flipflop using verilog and validating their functionality using their functional tables

SOFTWARE REQUIRED:

Quartus prime

THEORY

D Flip-Flop

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

image

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

image

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

image

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

Procedure

.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

PROGRAM

BY SRIRRAM B
212223040203
module D_FF(D,Clock,reset,Q);
input D,Clock,reset;
output reg Q;
always@(negedge Clock)//use negative edge clock for triggering condition
if(!reset)
Q<=0;
else
Q<=D;
endmodule
RTL LOGIC FOR FLIPFLOPS de4

TIMING DIGRAMS FOR FLIP FLOPS

de5

RESULTS

Thus the program to implement a D flipflop using verilog and validating their functionality using their functional tables.
