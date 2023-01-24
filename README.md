# mod3downcounter

Aim:
Design and simulate mod 3 synchronous counter using Verilog.
Introduction : These types of counters fall under the category of synchronous controller counter. Here the mode control input is used to decide whether which sequence will be generated by the counter. In this case, mode control input is used to decide whether the counter will perform up counting or down counting .In synchronous counter clock is provided to all the flip-flops simultaneously. Circuit becomes complex as the number of states increases,Speed is high

Program: 

module md3(input CLK,input reset,output[0:3]counter);
reg[0:3] counter_down;
always@(posedge CLK or posedge reset)
begin
if (reset)
counter_down <= 4'd0;
else
counter_down<=counter_down-4'd1;
end
assign counter = counter_down;
endmodule

Program Input:

![Coding](https://user-images.githubusercontent.com/119476322/214327964-2bc389fe-b874-4a1c-99a3-85d746688bdd.png)

Logic Diagram : 

![LG](https://user-images.githubusercontent.com/119476322/214329686-24ed537f-dbc1-41cd-81a5-dff3e3b5e6bf.png)

Truth Table: 

![Truthtable](https://user-images.githubusercontent.com/119476322/214329912-49f2219d-8e99-4944-8f00-b4eefc07fec2.png)

RTL Diagram: 

![md3Logic Diagram](https://user-images.githubusercontent.com/119476322/214327309-1be96f43-c968-44ab-8ec5-38854b351eb8.png)

Timing Diagram: 

![md3TimingDiagram](https://user-images.githubusercontent.com/119476322/214330034-34fb1525-5921-4335-8c83-3b533ce29096.png)

Result:

Simulate mod 3 synchronous counter using Verilog is executed sucessfully.
