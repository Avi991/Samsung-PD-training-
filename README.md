# Samsung-PD-training-
## Day-0-Installation

 <details>
 <summary> ICC2 </summary>

It appears that "icc2 compiler" might refer to an abbreviation of "Intel C++ Compiler 2," which would be the second version of Intel's C++ compiler. Intel's C++ Compiler is a tool used to compile C and C++ programs, optimizing them for Intel processors and architectures. It offers features like advanced vectorization, parallelization, and optimization techniques to enhance the performance of code on Intel-based systems.

I installed ICC2 using the following commands and Below is the screenshot showing sucessful launch:

<img width="1085" alt="ICC2" src="https://github.com/Avi991/Samsung-PD-training-/blob/cbd01432461cd5fbbf5f74a0625776a4dc6b082d/Samsung_PD_%23day0/icc2.png">
</details>
------------------------------

<details>
 <summary> lc_shell </summary>

LC_shell, also known as Design Compiler Graphical, is a part of the Synopsys suite of Electronic Design Automation (EDA) tools. It's used in the digital design flow for logic synthesis and optimization. Design Compiler Graphical is an advanced version of the original Design Compiler tool, providing additional features and a more user-friendly graphical interface.
I invoked lc_shell using the following commands and Below is the screenshot showing sucessful launch:

<img width="1085" alt="lc_shell" src="https://github.com/Avi991/Samsung-PD-training-/blob/cbd01432461cd5fbbf5f74a0625776a4dc6b082d/Samsung_PD_%23day0/lc.png">
</details>
-------------------------------
<details>
 <summary>dc_shell</summary>
Design Compiler is the command line interface of Synopsys synthesis tool. It includes innovative topographical technology that enables a predictable flow resulting in faster time to results.It is invoked using the command dc_shell    

Below is the screenshot showing the successful launch:

<img width="1085" alt="dc_shell" src="https://github.com/Avi991/Samsung-PD-training-/blob/857bc676cc691d6f1ca6e79cda309159fe38d58e/training_1/dc.png">
</details>

------------------------------

<details>
 <summary> pt_shell </summary>

"PrimeTime" is a widely used Electronic Design Automation (EDA) tool developed by Synopsys. It is used for static timing analysis, which is a crucial step in the digital design flow to ensure that the design meets its timing requirements. The "PrimeTime Shell" is the user interface through which engineers interact with the PrimeTime tool to perform timing analysis and optimization.
I invoked pt_shell using the following commands and Below is the screenshot showing sucessful launch:

<img width="1085" alt="pt_shell" src="https://github.com/Avi991/Samsung-PD-training-/blob/cbd01432461cd5fbbf5f74a0625776a4dc6b082d/Samsung_PD_%23day0/pt.png">
</details>



## Day-1-Introduction to Verilog RTL Design and Synthesis
<details>
 <summary> Introduction to RTL-Design, Test-bench, Simulators </summary>
-RTL Design : The RTL Design stands for Register Transfer Language. It sits between the high-level system specification and the lower-level gate-level implementation. This is a design abstraction which models the flow of digital signals between hardware registers, and the logical operations performed on those signals. RTL is preferred because it is easy to understand and implement compared to structural and behavioral models.

-HDL : A hardware description language (HDL) enables a precise, formal description of an electronic circuit that allows for the automated analysis and simulation of an electronic circuit.

-Simulator : Simulator is the tool used for checking adherence to the specification by simulating the design. iverilog is the tool used for RTL simulation. A simulator looks for change in the input signals and when no change in input, the output also doesn't change. It produces an output in the form of a .vcd file.

-Design : Design is the actual verilog code or set of Verilog codeswhich has the intended functionality to meet the required specifications. Design may have one or more primary inputs or primary outputs.  RTL design is the behavioral representation of the required specification.

<summary> Labs on examples of iverilog and gtkwave </summary>
We made a directory namely VLSI and inside that directory we cloned vsdflow and sky130RTLDesignAndSynthesisWorkshop repository. This repository consists of the required .lib files and verilog codes and its testbenches for practice.
I installed the needed tools and attached the required screenshots:

</details>

 
Below is the output wave form in gtkwave generated by performing a simulation of good_mux using iverilog.

The syntax of the code is: iverilog <RTL_code> <Its_Testbench>
 <details>
 <summary> GTK Wave </summary>

GTKWave is an open-source waveform viewer and analyzer primarily used in digital design and electronic design automation (EDA) workflows. It allows users to visualize and analyze the waveforms generated by digital simulations, making it a valuable tool for debugging and verifying digital designs.

I installed GTKwave using the following commands and Below is the screenshot showing sucessful launch:

<img width="1085" alt="GTKwave" src="https://github.com/Avi991/Samsung-PD-training-/blob/cbd01432461cd5fbbf5f74a0625776a4dc6b082d/Samsung_PD_%23day1/4.png">
</details>
<details>
 <summary> Yosys </summary>
Yosys is an open-source framework for Verilog RTL synthesis. RTL stands for Register Transfer Level, which is a high-level abstraction used to describe digital circuits at the level of registers and their interactions. Yosys is primarily used in the digital design and electronic design automation (EDA) community to convert RTL descriptions of digital circuits, written in languages like Verilog or SystemVerilog, into a netlist representation that can be further optimized, analyzed, and eventually implemented in hardware.

I installed Yosys using the following commands and Below is the screenshot showing sucessful launch:

<img width="1085" alt="yosys" src="https://github.com/Avi991/Samsung-PD-training-/blob/cbd01432461cd5fbbf5f74a0625776a4dc6b082d/Samsung_PD_%23day1/5.png">
</details>
<details>
<summary>Labs on Yosys </summary>
 We were given the overview of this tool and the basic files required to perform the experiment on 2:1 MUX. 
 
 **Procedure** : First we need to read the liberty file using the code
 
 **read_liberty -lib <path of the .lib>**
 
 Then we need read the RTL Design code

 **read_verilog <RTL_Design_file>**

 After this we need to perform synthesis 

 **synth -top <instance_name>**
 
 generating netlist

 **abc -liberty <.lib path>**
 
This Netlist can be viewed in the synthesized circuit form using the **show** command    

<img width="1085" alt="ckt" src="https://github.com/Avi991/Samsung-PD-training-/blob/d0c56f29c950594bf4d7302ad2fca09563c63e3c/Samsung_PD_%23day1/6.png">
<img width="1085" alt="ckt" src="https://github.com/Avi991/Samsung-PD-training-/blob/d0c56f29c950594bf4d7302ad2fca09563c63e3c/Samsung_PD_%23day1/7.png">
<img width="1085" alt="ckt" src="https://github.com/Avi991/Samsung-PD-training-/blob/d0c56f29c950594bf4d7302ad2fca09563c63e3c/Samsung_PD_%23day1/8.png">
<img width="1085" alt="ckt" src="https://github.com/Avi991/Samsung-PD-training-/blob/d0c56f29c950594bf4d7302ad2fca09563c63e3c/Samsung_PD_%23day1/9.png">
<img width="1085" alt="ckt" src="https://github.com/Avi991/Samsung-PD-training-/blob/d0c56f29c950594bf4d7302ad2fca09563c63e3c/Samsung_PD_%23day1/9a.png">

Simplified Netlist code 
<img width="1085" alt="netlist" src="https://github.com/Avi991/Samsung-PD-training-/blob/d0c56f29c950594bf4d7302ad2fca09563c63e3c/Samsung_PD_%23day1/9b.png">
</details>

## Day-2-Introduction to Timing libraries, Hierarchical vs flat synthesis, and flip flop coding
<details>
	
 <summary> Introduction to Timing Library File (.Lib),Hierarchical vs Flat Synthesis </summary>
 
Liberty File(.lib) contains all std cells used in IC design their specifications are stored in .lib file. Also, Liberty File(.lib) consists of ASCII representations of Timing, Area, and Power associated with the Standard cell. The Naming convention in the timing file follows technology node and PVT format (Process, Voltage, Temperature).The Standard library used in our case was sky130_fd_sc_hd_tt_025C_1v8, File description 130 depicts technology node 130nm process is typical(tt), temperature is 25C, and 1v8 represents the 1.8V Voltage .
Screenshot of a standard library file shown below: 
<img width="1085" alt="lib" src="https://github.com/Avi991/Samsung-PD-training-/blob/e80dfe2463278a272ef026609f0bf2b1e7826dc4/Samsung_PD_%23day2/2.png">
	
The Liberty File also consists of the technology used for standard cells as in the above example it is CMOS, it also specifies the delay model, unit of time, unit of voltage, unit of resistance, and many other units.
All the data i.e std cells delays, leakage power, capacitance is stored in form of lookup tables(LUTs). For each gate cell based on the number of inputs(N), there will be 2^N combinations, and for each combination leakage power, area, delay, and all related parameters are mentioned. 

The timing file consists of many different variations of the same gate cells. As we move toward faster cell (cell with higher drive strength) the area and power increases. In liberty file area, power, timing values are given for same cell of different drive strength and it also consist if the inform about leakage power of all the possible logic of different configration shown below.
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/e80dfe2463278a272ef026609f0bf2b1e7826dc4/Samsung_PD_%23day2/2.png">
</details>

<details>
 <summary> Hierarchical vs Flat synthesis in Yosys </summary>
Hierarchical synthesis : The basic flow of hierarchical design is Dividing a design into multiple blocks (i.e. sub-chips, sub-blocks, modules, hierarchical blocks, etc.) which can also be user defined. Hierarchial design has blocks, subblocks in an hierarchy.
In Yosys we have done synthesis of a multimodule combinational circuit which consists of two sub_modules one that of ** AND ** gate and other of ** OR ** gate. Below is the RTL Design code of multimodules is gvien below:
	<img width="1085" alt="lib" src="https://github.com/Avi991/Samsung-PD-training-/blob/e80dfe2463278a272ef026609f0bf2b1e7826dc4/Samsung_PD_%23day2/4.png">

We do synthesis in yosys it generates the following gate level netlist :

<img width="1085" alt="lib" src="https://github.com/Avi991/Samsung-PD-training-/blob/e80dfe2463278a272ef026609f0bf2b1e7826dc4/Samsung_PD_%23day2/5(synthesis).png">

The yosys considers the module hierarchy and does mapping according to the instantiation i.e by using sub blocks.The netlist code for hierarchical implementation of the multiple_modules.

<img width="1085" alt="lib" src="https://github.com/Avi991/Samsung-PD-training-/blob/e80dfe2463278a272ef026609f0bf2b1e7826dc4/Samsung_PD_%23day2/7(synthesisize%20hier).png">

In the netlist it can observed that separate modules namely sub_module1 sub_module2 are created  i.e submodules are getting instanstiated not the std cells present in library

<img width="1085" alt="lib" src="https://github.com/Avi991/Samsung-PD-training-/blob/e80dfe2463278a272ef026609f0bf2b1e7826dc4/Samsung_PD_%23day2/6(show%20hier).png">

Flat synthesis : In Flat synthesis the hierarchies the flattened out and every submodule is created using std cells. We apply flat synthesis on the same design mentioned above. The command used to perform Flat synthesis from yosys are as follows :

--- read_liberty -lib <path of the .lib>

--- read_verilog <RTL_file>

--- synth -top <instance_name>

--- abc -liberty <.lib_path>

--- flatten

--- write_verilog -noattr <.v_File_name>
The synthesized circuit for a flattened netlist is shown in the below: 
<img width="1085" alt="lib" src="https://github.com/Avi991/Samsung-PD-training-/blob/e80dfe2463278a272ef026609f0bf2b1e7826dc4/Samsung_PD_%23day2/8(synthesized%20op%20flat).png">
<img width="1085" alt="lib" src="https://github.com/Avi991/Samsung-PD-training-/blob/e80dfe2463278a272ef026609f0bf2b1e7826dc4/Samsung_PD_%23day2/9(show%20flat).png">
</details>

<details>
 <summary> Flip-flop Coding Styles </summary>
 Flip-flops :A flip-flop is a sequential digital electronic circuit having two stable states that can be used to store one bit of binary data. Flip-flops are the fundamental building blocks of all memory devices.

 The complexity of cobinational circuit increases the chance of glitch, hence FFs are used to avoid it and it stable output.

 Asynchronous Reset D Flop: 
 
 Here the output signal goes low when the reset signal is high , irrespective of the clock's edge(+ve,-ve edge ).
 RTL code of positive edge trigerred asynchronous reset D FF:
 ```
module dff_asyncres ( input clk ,  input async_reset , input d , output reg q );
	always @ (posedge clk , posedge async_reset)
	begin
		if(async_reset)
			q <= 1'b0;
		else	
			q <= d;
	end
endmodule
```
Its gtkwave :<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/b3717ddc1a24961d4e335d766f7df6fea792b6b1/Samsung_PD_%23day2/10(dff_async_gtk).png">
Its Yosys synthesised netlist:
<img width="1085" alt="lib1" src="https://github.com/Luffy-7744/Samsung-PD-Training-/blob/7b832441e73dd5c5bc078425a1f34ee4dea508fd/PD%23Day2/asyn_rst_synth.png">

Asynchronous set D Flop:

Here the output signal goes high when the reset signal is high , irrespective of the clock's edge(+ve,-ve edge ).
 RTL code of positive edge trigerred asynchronous set D FF:
 ```
module dff_async_set ( input clk ,  input async_set , input d , output reg q );
	always @ (posedge clk , posedge async_set)
	begin
		if(async_set)
			q <= 1'b1;
		else
			q <= d;
	end
endmodule
```
Its GTKwave :
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/b3717ddc1a24961d4e335d766f7df6fea792b6b1/Samsung_PD_%23day2/11(async_set).png">

Its Yosys synthesised netlist:
we used **dfflibmap -liberty** <> command to look from only flop library to for d flip flops
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/5dac4460dd9d997d4620d6b16521449a1ec30edd/Samsung_PD_%23day2/12(map).png">
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/5dac4460dd9d997d4620d6b16521449a1ec30edd/Samsung_PD_%23day2/13(dff%20net).png">

Its GTKwave :
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/5dac4460dd9d997d4620d6b16521449a1ec30edd/Samsung_PD_%23day2/11(async_set).png">

Its Yosys synthesised netlist:
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/5dac4460dd9d997d4620d6b16521449a1ec30edd/Samsung_PD_%23day2/14(async%20set%20netl).png">


Synchronous reset D Flop :

The reset depend on the clock edge. Here the output signal goes low whenever the reset signal is high and at the clock edge(positive or negative)
RTL code of positive edge trigerred synchronous reset D FF:
```
module dff_syncres ( input clk , input async_reset , input sync_reset , input d , output reg q );
	always @ (posedge clk )
	begin
		if (sync_reset)
			q <= 1'b0;
		else	
			q <= d;
	end
endmodule
```
Its GTKwave :
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/d249e61b0031a5effcc73aa6e54e0459942414af/Samsung_PD_%23day2/synch%20res%20gtk.png">

Its Yosys synthesised netlist:
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/d249e61b0031a5effcc73aa6e54e0459942414af/Samsung_PD_%23day2/sync%20net.png">
</details>

<details>
 <summary> Optimization Techniques </summary>
	
 The Optimization involves the reducing hardware in the design such that to improve area, power and speed. Two example where given:
 1. a*2
Consider a case where 3 bit number is multiplied by 2 in this case we dont need any additional hardware and only needs connecting bits to the output and grounding the LSB bit,same is realized by yosys. When binary number is multiplied by 2^n then result will gave same number by appending zero in LSB by n times.
RTL code:
	
```
	module mul2 (input [2:0] a, output [3:0] y);
	assign y = a * 2; // assign y={a,1'b0}
	endmodule
```

Yosys Synthesis result : 
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/4aa1beeae13c1dcd880195cfe9758467617731a4/Samsung_PD_%23day2/15(mult%20%20synth).png">

 2. a*9
Multiplying a 3 bit number by 9, gives results as concatination of same number twice {a,a}.
a*[8+1]= {a,0,0,0} + a(3bit)={a,a}

RTL code:

```
module mul8 (input [2:0] a, output [5:0] y);
	assign y = a * 9; // assign y={a,a}
endmodule
```

Yosys Synthesis result :

<img width="1085" alt="lib8" src="https://github.com/Avi991/Samsung-PD-training-/blob/4aa1beeae13c1dcd880195cfe9758467617731a4/Samsung_PD_%23day2/16(mult8).png">

</details>

## Day-3- Combinational and sequential optmizations
![dffconst(net)](https://github.com/Avi991/Samsung-PD-training-/assets/142480104/43154f44-cfb6-459d-ae97-45873fef14df)

<details>
 <summary> Combinational Optimization </summary>
Optimising the combinational logic circuit means squeezing the logic to get the most optimized digital design so that optimized circuit area and power is saved. Various techniques and gives us the most optimized circuit.Implemented using synthesis tools
Command to optimize the circuit by yosys is ** yosys> opt_clean -purge ** to remove unused nets
We have done synthesis using yosys for few examples:
	![dffconst(net)](https://github.com/Avi991/Samsung-PD-training-/assets/142480104/43154f44-cfb6-459d-ae97-45873fef14df)

**Example 1**
```
module opt_check (input a , input b , output y);
	assign y = a?b:0;
endmodule
```
yosys generated netlist :
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/9220aa9dc26021df6e5a1b6ada51b54e987adb1f/Samsung_PD_%23day3/opt1.png">
From the output we inferred that above mux implementation can be optimized to two input AND gate

**Example 2**
```
module opt_check2 (input a , input b , output y);
	assign y = a?1:b;
endmodule
```
yosys generated netlist :
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/9220aa9dc26021df6e5a1b6ada51b54e987adb1f/Samsung_PD_%23day3/opt2.png">
From the output we inferred that above mux implementation can be optimized to two input OR gate which is also realised using inverter and NAND gate as stacking of PMOS will result in more area

**Example 3**
```
module opt_check3 (input a , input b, input c , output y);
	assign y = a?(c?b:0):0;
endmodule
```
yosys generated netlist :
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/9220aa9dc26021df6e5a1b6ada51b54e987adb1f/Samsung_PD_%23day3/opt3.png"> 
From the output we inferred that above mux implementation can be optimized to 3 input gate

**Example 4**
```
module opt_check4 (input a , input b , input c , output y);
	assign y = a?(b?(a & c ):c):(!c);
endmodule
```
yosys generated netlist :
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/9220aa9dc26021df6e5a1b6ada51b54e987adb1f/Samsung_PD_%23day3/opt4.png">   
From the output we inferred that above mux implementation can be optimized to two input xnor gate

**Example 5**
Here there is multiple modules present so we will verify whether those module are being used or not and we use flatten for submudules commands to perform that
**read_liberty -lib <library_path>**
**read_verilog <verilog_file>**
**synth -top <module_name>**
**opt_clean -purge**
**abc -liberty <library_path>**
**flatten**
```
module sub_module1(input a , input b , output y);
	 assign y = a & b;
	endmodule

	module sub_module2(input a , input b , output y);
	 assign y = a^b;
	endmodule

	module multiple_module_opt(input a , input b , input c , input d , output y);
	wire n1,n2,n3;
	sub_module1 U1 (.a(a) , .b(1'b1) , .y(n1));
	sub_module2 U2 (.a(n1), .b(1'b0) , .y(n2));
	sub_module2 U3 (.a(b), .b(d) , .y(n3));

	assign y = c | (b & n1); 
	endmodule
```
Generated nelist:
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/9220aa9dc26021df6e5a1b6ada51b54e987adb1f/Samsung_PD_%23day3/mult_opt1.png"> 
Sub module 1 is an AND gate , Sub module 2 is an OR gate once optimization is done

**Example 6**

```
module sub_module(input a , input b , output y);
	assign y = a & b;
endmodule

module multiple_module_opt2(input a , input b , input c , input d , output y);
	wire n1,n2,n3;
	sub_module U1 (.a(a) , .b(1'b0) , .y(n1));
	sub_module U2 (.a(b), .b(c) , .y(n2));
	sub_module U3 (.a(n2), .b(d) , .y(n3));
	sub_module U4 (.a(n3), .b(n1) , .y(y));
endmodule
```

Generated nelist:
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/9220aa9dc26021df6e5a1b6ada51b54e987adb1f/Samsung_PD_%23day3/mult_opt2.png">   Sub module is an and gate after realization output comes out to be zero
</details>

<details>
 <summary> Sequential Optimization </summary>
There are various techniques for Sequential Logic Optimization

    - Sequentialal constant propagation

    - Advanced

        - State Optimization

        - Retiming

        - Sequential Logic cloning

Sequential Constant Propogation

For understanding we took asynchronous reset D Flip-flop is fed with d = 0(i.e GND) always so the output will always be 0 irrespective of the clock or circuit.

Advanced

State Optimisation: This is optimisation of unused state. Using this technique we can come up with most optimised state machine.

Cloning : It is an optimization technique that replicates a cell to reduce the load on heavily loaded cell. This technique is usually preffered while performing PHYSICAL AWARE SYNTHESIS. Lets consider a flop A which is connected to flop B and flop C through a combination logic. If B and C are placed far from A in the floorplan, there is a routing path delay. To avoid this, we connect A to two intermediate flops and then from these flops the output is sent to B and C thereby decreasing the delay. This phenomenon is called cloning since we are generating two new flops with same functionality as A.

Retiming : Sequential circuits can be optimised by retiming. The combinational section of the circuitry is unaffected as it only rearranges the registers in the circuit. It is a powerful sequential optimization technique used to move registers across the combinational logic or to optimize the number of registers to improve performance via power-delay trade-off, without changing the input-output behavior of the circuit.

**Example 1**
```
module dff_const2(input clk, input reset, output reg q);
	always @(posedge clk, posedge reset)
	begin
		if(reset)
			q <= 1'b1;
		else
			q <= 1'b1;
	end
endmodule
```
GTK Wave:
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/9220aa9dc26021df6e5a1b6ada51b54e987adb1f/Samsung_PD_%23day3/dffconst1(gtkwave).png">   


Yosys generated netlist:
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/9220aa9dc26021df6e5a1b6ada51b54e987adb1f/Samsung_PD_%23day3/dffconst(net).png">   
As we know the above code is for a d flipflop with an asynchronous reset this is used to reset the system asynchronously and later the system comes into normal oprtaion for next 1 clk that is synchronously so this system cannot be further optimized and a flipflop is generated 

**Example 2**
```
module dff_const2(input clk, input reset, output reg q);
	always @(posedge clk, posedge reset)
	begin
		if(reset)
			q <= 1'b1;
		else
			q <= 1'b1;
	end
endmodule
```
GTK Wave:
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/9220aa9dc26021df6e5a1b6ada51b54e987adb1f/Samsung_PD_%23day3/dffconst2(gtkwave).png">


Yosys generated netlist:
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/9220aa9dc26021df6e5a1b6ada51b54e987adb1f/Samsung_PD_%23day3/dffconst2(net).png">
From the output we can say the optimization can be done as the q value is always 1 hence no flop is generated and the optimization is done

**Example 3**
```
module dff_const3(input clk, input reset, output reg q);
	reg q1;

	always @(posedge clk, posedge reset)
	begin
		if(reset)
		begin
			q <= 1'b1;
			q1 <= 1'b0;
		end
		else
		begin
			q1 <= 1'b1;
			q <= q1;
		end
	end
	endmodule
```

GTK Wave:
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/9220aa9dc26021df6e5a1b6ada51b54e987adb1f/Samsung_PD_%23day3/dffconst3(gtkwave).png">   


Yosys generated netlist:
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/9220aa9dc26021df6e5a1b6ada51b54e987adb1f/Samsung_PD_%23day3/dffconst3(net).png">   

**Example 4**
```
module dff_const4(input clk, input reset, output reg q);
	reg q1;

	always @(posedge clk, posedge reset)
	begin
		if(reset)
		begin
			q <= 1'b1;
			q1 <= 1'b1;
		end
	else
		begin
			q1 <= 1'b1;
			q <= q1;
		end
	end
	endmodule
```

GTK Wave:
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/9220aa9dc26021df6e5a1b6ada51b54e987adb1f/Samsung_PD_%23day3/dffconst4(gtkwave).png">   


Yosys generated netlist:
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/9220aa9dc26021df6e5a1b6ada51b54e987adb1f/Samsung_PD_%23day3/dffconst4.png"> 

**Example 5**
```
module dff_const5(input clk, input reset, output reg q);
	reg q1;
	always @(posedge clk, posedge reset)
		begin
			if(reset)
			begin
				q <= 1'b0;
				q1 <= 1'b0;
			end
		else
			begin
				q1 <= 1'b1;
				q <= q1;
			end
		end
	endmodule
```
GTK Wave:
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/9220aa9dc26021df6e5a1b6ada51b54e987adb1f/Samsung_PD_%23day3/dffcosnt5(gtkwave).png">   


Yosys generated netlist:
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/9220aa9dc26021df6e5a1b6ada51b54e987adb1f/Samsung_PD_%23day3/dffconst5(net).png"> 
No scope of further optimization as the outputs a constant value is seen in all conditions therefore two flipflops getting generated
</details>


<details>
 <summary> Optimization Examples </summary>
	
**Example 1**
```
   module counter_opt (input clk , input reset , output q);
   reg [2:0] count;
   assign q = count[0];
   always @(posedge clk ,posedge reset)
   begin
   	if(reset)
   		count <= 3'b000;
   	else
   		count <= count + 1;
   end
   endmodule
```
   
GTK wave:
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/9220aa9dc26021df6e5a1b6ada51b54e987adb1f/Samsung_PD_%23day3/gtkwave(counter%20opt).png"> 

Yosys generated netlist
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/9220aa9dc26021df6e5a1b6ada51b54e987adb1f/Samsung_PD_%23day3/count_opt(netlist).png">
As the 0th bit is only used for the output hence during the synthesis only one flipflop is generated with inverter for the toggle oprtaion 
Remaining bits are unused so their respective flops are not generated
</details>

## Day-4- GLS Blocking vs Non-Blocking And Synthesis-Simulation Mismatch 
<details>
<summary> GLS Concepts And Flow Using Iverilog </summary>

-- What is GLS- Gate Level Simulation?:
GLS is generating the simulation output by running test bench with netlist file generated from synthesis as design under test. Netlist is logically same as RTL code, hence, same test bench can be used for it.

-- Why GLS?:
We perform this to verify logical correctness of the design after synthesizing it. 

If GLS is run with delay annotion then it can be used for timing analysis 

**Synthesis Simulation Mismatch** 

Synthesis simulation mismatch denotes the discrepancy between the actual behavior of a circuit as simulated during design and its real-world performance after synthesizing the design. 

Synthesis simulation mismatched are mainly caused because of the following reasons 

- Missing sensitivity list
- Blocking vs Non Blocking assignments
- Non standard verilog code

**Missing sensitivity list**
The absence of a complete sensitivity list in VLSI design can give rise to problems. In hardware description languages (HDL) like Verilog, a sensitivity list is utilized to specify the inputs that should activate the execution of a specific process or code block. Inadequate or missing signals in the sensitivity list can lead to inaccurate or unforeseen behavior of the circuit during synthesis or simulation. Ensuring an accurate representation of inputs impacting the logic within a process is vital.

As the synthesizer does not look for sensitivity list and it looks only statements in the procedural block , it infers correct circuit and if we simulate the netlist code , there will be synthesis simulation mismatch. In to order tackle this issue this issue it is important to check the behaviour of the circuit first and then match it with the expected output seen in the simulation. 

**Blocking Vs Non Blocking Assignments**

Blocking statements execute the will wait for the current one to finish.i.e. sequentially inside the always block. 
Non-Blocking statements execute all the assignment parallelly inside a always block.First all the RHS is evaluated and then assigned
This will give mismatch as sometimes, improper use of blocking statements can create latches. 

Missing sensitivity list in always block:
Lets take example of mux having inputs as i0,i1 and sel and output as y.
```
always @(sel)                  always @(*)
//It will infer a latch        // It will infer a mux.
```
If i0 and i1 change in activity will not be reflected in always block.
To avoid the synthesis and simulation mismatch. It is very important to check the behaviour of the circuit first and then match it with the expected output seen in simulation and make sure there are no synthesis and simulation mismatches. This is why we use GLS.

<details>
<summary> LABs </summary>
	
**Example 1**

```
module ternary_operator_mux (input i0 , input i1 , input sel , output y);
   assign y = sel?i1:i0;
endmodule
```
Gtkwave :
<img width="1085" alt="lib1" src="">

Hardware
<img width="1085" alt="lib1" src="">

Yosys result: 
<img width="1085" alt="lib1" src="">

GLS Simulation:
I used the below commands to carry out GLS of ternary_operator_mux.v:
```
iverilog <path to verilog model: ../mylib/verilog_model/primitives.v> <path to sky130_fd_sc_hd__tt_025C_1v80.lib: ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib> <name netlist: ternary_operator_mux_net.v> <name testbench: tb_ternary_operator_mux.v>
./a.out
gtkwave tb_ternary_operator_mux.vdc
```

<img width="1085" alt="lib1" src="">
In this example there is no mismatch between the RTL Design simulated wave and Netlist simulated wave.

**Example 2**
```
module bad_mux (input i0 , input i1 , input sel , output reg y);
	always @ (sel)
	begin
		if(sel)
			y <= i1;
		else 
			y <= i0;
	end
endmodule
```
Gtkwave:
<img width="1085" alt="lib1" src="">

Hardware
<img width="1085" alt="lib1" src="">

Yosys result: 
<img width="1085" alt="lib1" src="">

GLS Simulation:
<img width="1085" alt="lib1" src=">

From the output we can infer the netlist simulation which corrects the bad_mux design which was only changing waveform when sel was triggered while for a mux to work properly it should be sensitivity to all the input signals. No change in activities of input signal is recorded

**Example 3**
```
module blocking_caveat (input a , input b , input  c, output reg d); 
reg x;
always @ (*)
	begin
	d = x & c;
	x = a | b;
end
endmodule
```

Gtkwave:
<img width="1085" alt="lib1" src="">

Hardware
<img width="1085" alt="lib1" src="">

Yosys result: 
<img width="1085" alt="lib1" src="">

GLS Simulation:
<img width="1085" alt="lib1" src="">

