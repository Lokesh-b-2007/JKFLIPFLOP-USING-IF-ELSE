JKFLIPFLOP-USING-IF-ELSE
AIM:

To implement JK flipflop using verilog and validating their functionality using their functional tables

SOFTWARE REQUIRED:

Quartus prime

THEORY

JK Flip-Flop

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![300541519-a649c30b-232b-4558-b188-fd6c09845180](https://github.com/user-attachments/assets/fa7f5550-3533-40c4-9975-a0a3d4456178)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![300541618-c4360742-e8a8-4937-b089-c46c0433f9a3](https://github.com/user-attachments/assets/5b7d0e31-3477-4f82-85cd-5d882b342e6b)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State

![300541696-6c275261-a6d5-4c37-a3a7-1e88ca11c4cd](https://github.com/user-attachments/assets/193d4282-8b71-4fd9-b1f7-490fd1a4a053)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![300541801-5174f41b-0ce0-4329-a372-6d1943ea6673](https://github.com/user-attachments/assets/a434b8ee-87bf-470c-97b1-7e2692fe9e4e)


The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

Procedure

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

PROGRAM

Program for flipflops and verify its truth table in quartus using Verilog programming.

Developed by: Lokesh B
RegisterNumber: 212224040172
~~~
module ex7(J,K,clk,q,qbar);
input J,K,clk;
output reg q;
output reg qbar;
initial q=0;
initial qbar=1;
always @(posedge clk)
begin
q=((J&(~q))|((~K)&q));
qbar=~q;
end
endmodule
~~~
RTL LOGIC FOR FLIPFLOPS ![440815979-f0ce75b5-1b07-457c-9efb-472f11bba667](https://github.com/user-attachments/assets/5c4a9d6e-b56e-4f97-8567-c17dbe4cf550)


TIMING DIGRAMS FOR FLIP FLOPS ![440816054-85cb07ff-7c5a-48d2-8788-5c1e90643311](https://github.com/user-attachments/assets/c3db3914-57d2-4d28-9e6a-53b9b48ee952)


RESULTS

Thus the JK flipflop is verfied
