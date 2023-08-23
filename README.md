# Samsung-PD-training-
## Day-0-Installation
<details>
 <summary> Summary </summary>

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
## Day-2-ntroduction to Timing libraries, Hierarchical vs flat synthesis, and flip flop coding

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
```
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
 
 Here the output signal goes low when the reset signal is high , irrespective of the clock's edge(+ve,-ve or dual edge ).
 RTL Design code of positive edge trigerred asynchronous reset D FF:
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

Here the output signal goes high when the reset signal is high , irrespective of the clock's edge(+ve,-ve or dual edge ).
 RTL Design code of positive edge trigerred asynchronous set D FF:
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

Synchronous reset D Flop :

The reset depend on the clock edge. Here the output signal goes low whenever the reset signal is high and at the clock edge(positive or negative)
RTL Design code of positive edge trigerred synchronous reset D FF:
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
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/5dac4460dd9d997d4620d6b16521449a1ec30edd/Samsung_PD_%23day2/11(async_set).png">

Its Yosys synthesised netlist:
<img width="1085" alt="lib1" src="https://github.com/Avi991/Samsung-PD-training-/blob/5dac4460dd9d997d4620d6b16521449a1ec30edd/Samsung_PD_%23day2/14(async%20set%20netl).png">
</details>


<details>
 <summary> Optimization Techniques </summary>
 The Optimization involves the reducing hardware in the design to improve area, power and speed. Two example where given:
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
