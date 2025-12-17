# JKFLIPFLOP-USING-IF-ELSE

**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/a649c30b-232b-4558-b188-fd6c09845180)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/c4360742-e8a8-4937-b089-c46c0433f9a3)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/6c275261-a6d5-4c37-a3a7-1e88ca11c4cd)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/5174f41b-0ce0-4329-a372-6d1943ea6673)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

**Procedure**

/* write all the steps invloved*/
```
1.Open Quartus Prime and create a new project using the New Project Wizard.

2.Create a Verilog HDL file and write the JK flip-flop code using if-else statements.

3.Define inputs J, K, CLK and output Q.

4.Save the file and set it as the Top-Level Entity.

5.Compile the design and ensure there are no errors.

6.Simulate using VWF/ModelSim and verify the output with the functional table.
```

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by:NITESH BHANDARI K  RegisterNumber:25009039
*/
```
module jk(j,k,clk,q,qbar);
input j,k,clk;
output reg q,qbar;
initial 
begin
q=1'b0;
qbar=1'b1;
end 

always @(posedge clk)
begin 
q<=(j&~q)|(~k&q);
qbar<=~q;
end
endmodule
```

**RTL LOGIC FOR FLIPFLOPS**

<img width="1919" height="958" alt="exp7delg" src="https://github.com/user-attachments/assets/5a0ed2ef-93dc-4b9f-bf50-937d45797cac" />


**TIMING DIGRAMS FOR FLIP FLOPS**

<img width="1919" height="1004" alt="exp7dewave" src="https://github.com/user-attachments/assets/b1967d5e-0a99-4251-ad9c-4f1f5d57f29b" />


**RESULTS**


```The JK flip-flop was successfully implemented using Verilog with if–else statements.```
