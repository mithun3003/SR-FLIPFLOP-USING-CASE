# EXP-06 SR-FLIPFLOP-USING-CASE

**AIM:**

To implement  SR flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

SR Flip-Flop SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/0f710028-ad52-4d3e-9276-8714cf023a25)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dabfc4f4-87e3-4cbc-9472-f89ee1b5ed30)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dd90d16c-aec5-4290-a586-e2346b1e9eb5)

 
By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/473efad6-d70b-4ca7-aeb7-898bbfca319f)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

**Procedure**

1.Write Verilog code for SR flip-flop using a case statement.

2.Compile and check the design for syntax or logic errors.

3.Create a testbench to apply various SR input combinations.

4.Simulate the design and observe Q and Qbar waveforms.

5.Record and analyze results for all input cases, including invalid.

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by: MITHUN S

RegisterNumber: 212224240088
*/
```
 module exp06(S,R,clk,Q,Qbar);
 input S,R,clk;
 output reg Q;
 output reg Qbar;
 initial Q=0;
 initial Qbar=1;
 always @(posedge clk) begin Q=S|((~R)&Q);
 Qbar=R|((~S) & (Qbar));
 end endmodule
```

**RTL LOGIC FOR FLIPFLOPS**

![image](https://github.com/user-attachments/assets/7e1fb88c-41e3-4eae-b2ee-fcc7444256cf)


**TIMING DIGRAMS FOR FLIP FLOPS**

![image](https://github.com/user-attachments/assets/b83fee26-a4e5-4f79-87ce-18ae725c8049)


**RESULTS**

To implement SR flipflop using verilog and validating their functionality using their functional tables is verified.
