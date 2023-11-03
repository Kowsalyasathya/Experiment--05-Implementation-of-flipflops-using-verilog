# Experiment--05-Implementation-of-flipflops-using-verilog
## AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
## HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
## SOFTWARE REQUIRED:   Quartus prime
## THEORY 
SR Flip-Flop :
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
STEP 1: Open Quartus II and select new project and choose the file location.

STEP 2: Module Declaration. Module should have the file name.

STEPS 3: Input-Output Delecaration.

STEPS 4: Use assign declaration and wire to define the functionality of logic circuits.

STEP 5: At the end give endmodule.

STEP 6: Run the program and choose RTL viewer to get RTL realization



## PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: Kowsalya M
RegisterNumber:  212222230069
*/
### SR FLIPFLOPS CODE:
```
module ex5(S,R,clk,Q,Qbar);
input S,R,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin
Q=S|((~R)&Q);
Qbar=R|((~S)&(Qbar));
end
endmodule
```
### JK FLIPFLOPS CODE:
```
module ex5(J,K,clk,Q,Qbar);
input J,K,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin
Q=(J&(~Q))|((~K)&Q);
Qbar=((~J)&(Qbar))|K&(~Qbar);
end
endmodule
```
### D FLIPFLOPS CODE:
```
module ex5(D,clk,Q,Qbar);
input D,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin
Q=D;
Qbar=~D;
end
endmodule
```
### T FLIPFLOPS CODE:
```
module ex5(T,clk,Q,Qbar);
input T,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin
Q=(T&(~Q))|((~T)&Q);
Qbar=((~T)&Qbar)|(T&(~Qbar));
end
endmodule
```
## RTL LOGIC FOR FLIPFLOPS 
### SR FLIPFLOPS CODE:
![279302218-3309e653-4412-4502-afd5-29a55722dcd8](https://github.com/Kowsalyasathya/Experiment--05-Implementation-of-flipflops-using-verilog/assets/118671457/7b5f3b53-ed23-4f91-a595-8b65b7e76319)
### JK FLIPFLOPS CODE:
![279302537-db08d95c-be36-4fe2-9ec5-20482c162d30](https://github.com/Kowsalyasathya/Experiment--05-Implementation-of-flipflops-using-verilog/assets/118671457/4eabeac1-f826-44e4-ba0d-84aa3df3ace3)
### D FLIPFLOPS CODE:
![279302620-7316ad8f-a156-4097-a3a8-8cd38905c2ef](https://github.com/Kowsalyasathya/Experiment--05-Implementation-of-flipflops-using-verilog/assets/118671457/5d29a344-6eb5-4b88-92a1-a788f685379d)
### T FLIPFLOPS CODE:
![279302868-79f18cf4-33ae-482b-b7cd-d0730462676a](https://github.com/Kowsalyasathya/Experiment--05-Implementation-of-flipflops-using-verilog/assets/118671457/9daec9e2-4659-43d7-b8a5-64f895b51417)

## TIMING DIGRAMS FOR FLIP FLOPS 
### SR FLIPFLOPS CODE:
![279302975-d20a3534-0329-4f5f-ac02-2320911508ea](https://github.com/Kowsalyasathya/Experiment--05-Implementation-of-flipflops-using-verilog/assets/118671457/97a924e9-42df-4183-ba51-ca4285ee77fa)
### JK FLIPFLOPS CODE:
![279308181-75d4f6b3-7d86-428e-a477-cb534743ed15](https://github.com/Kowsalyasathya/Experiment--05-Implementation-of-flipflops-using-verilog/assets/118671457/a2042ddd-2714-40b5-b91d-86f53281dbdc)
### D FLIPFLOPS CODE:
![279303323-11f12ad1-be0e-4fb2-a7b8-e8698d6941ab](https://github.com/Kowsalyasathya/Experiment--05-Implementation-of-flipflops-using-verilog/assets/118671457/6a2e8d63-5319-4b10-9971-3755f3f892d8)
### T FLIPFLOPS CODE:
![279303447-53549664-d67e-45f2-bd9a-88252f6b8c12](https://github.com/Kowsalyasathya/Experiment--05-Implementation-of-flipflops-using-verilog/assets/118671457/62817357-8c13-45b6-b926-0e36acdb2cc3)
### RESULTS :
Thus,Implementation-of-flipflops-using-verilog successfully completed.
