# SR-FLIPFLOP-USING-CASE

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

**Procedure**<br>
Type the program in Quartus software.<br>
Compile and run the program.<br>
Generate the RTL schematic and save the logic diagram.<br>
Create nodes for inputs and outputs to generate the timing diagram.<br>
For different input combinations generate the timing diagram.<br>

/* write all the steps invloved */

**PROGRAM**<br>

module srflipflop(s, r, clk, rst, q, qbar); <br> 
    input s; <br> 
    input r; <br> 
    input clk; <br> 
    input rst; <br> 
    output q; <br> 
    output qbar; <br> 
  reg q,qbar; <br> 
  always @ (posedge(clk) or posedge(rst)) begin <br> 
  if(rst==1'b1) begin <br> 
  q= 1'b0;qbar= 1'b1;<br> 
  end<br>  
  else if(s==1'b0 && r==1'b0)<br>  
   begin <br> 
  q=q; qbar=qbar; <br> 
  end <br> 
   else if(s==1'b0 && r==1'b1) <br> 
    begin <br> 
  q= 1'b0; qbar= 1'b1;<br>  
  end <br> 
    else if(s==1'b1 && r==1'b0) <br> 
    begin <br> 
  q= 1'b1; qbar= 1'b0; <br> 
  end <br> 
  else <br>  
  begin <br> 
  q=1'bx;qbar=1'bx; <br> 
  end <br> 
  end <br> 
endmodule<br>  


/* Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by:Lokesh.M RegisterNumber:24900227
*/

**RTL LOGIC FOR FLIPFLOPS**
![Screenshot 2024-12-09 205855](https://github.com/user-attachments/assets/e2999572-1af6-4607-bb98-ccdb93a7c5c6)


**TIMING DIGRAMS FOR FLIP FLOPS**
![Screenshot 2024-12-09 205924](https://github.com/user-attachments/assets/b1f28841-829a-45ce-a807-651c0de70221)


**RESULTS**
 Encoder implemented successfully SR-FLIPFLOP-USING-CASE verified.
