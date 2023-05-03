Download Link: https://assignmentchef.com/product/solved-cs39001-assignment5-verilog-design-of-bit-sliced-arithmetic-logic-unit-alu-and-fast-adders
<br>



<ol>

 <li><strong>[4-bit Combinational ALU/Functional Generator (74181)] </strong>The 74181 is a classic commercially available 4–bit combinational ALU/function generator IC. Its main inputs are: two 4–bit operands <em>A</em>[3 : 0] and <em>B</em>[3 : 0], an 1–bit <em>mode control signal M </em>which controls the mode of operation (<em>M </em>= 1 for logic operations and <em>M </em>= 0 for arithmetic operations), and a 4–bit <em>function select </em>signal <em>S</em>[3 : 0]. Its main output is a 4–bit <em>data out </em>signal <em>F</em>[3 : 0]. In the <em>logic mode </em>of operation, i.e., with <em>M </em>= 1, the <em>i</em>-th bit of <em>F </em>is given by:</li>

</ol>

From the above expression for <em>F<sub>i</sub></em>, it is evident 74181 can be used as a <em>universal function generator </em>for two Boolean variables, for different values of <em>S</em>[3 : 0], i.e., it can be used to generate all two–variable Boolean functions <em>F</em>(<em>A,B</em>). On the other hand, for <em>M </em>= 0. the circuits performs various arithmetic operations on the input operands <em>A </em>(see datasheet mentioned below for details).

Refer to the datasheet of 74181 uploaded on <em>Moodle </em>(consider the <em>Active HIGH Operand </em>version), particularly the function table given on page-2 of the datasheet. Design, simulate (using a proper testbench) and implement in Verilog (on a target FPGA supported by your CAD tool) the function table. Note that as per the manual, for the add/subtract operation, full 4-bit carry lookahead is supported, and this should also be the case in your implementation. Come up with a proper interface of your design referring to the logic diagram for the <em>Active HIGH </em>version, as given on page-1 of the datasheet. DO NOT DIRECTLY IMPLEMENT THE LOGIC DIAGRAM GIVEN ON PAGE-3 OF THE DATASHEET, YOU WILL GET

ZERO MARKS IF YOU DO SO.

<ol start="2">

 <li><strong>[16-bit Bit-sliced ALU/Functional Generator Using the 74181 IC] </strong>The 74181 has carry-in and carryout ports. This makes it possible to concatenate multiple instances of the IC to design larger ALU/function generator IC. This type of design belongs to the <em>Bit-slice design paradigm</em>, and was common in the early days of digital ICs, when it was difficult to implement in silicon digital circuits that could process operands with large number of bits. Design, simulate (using a proper testbench) and implement in Verilog (on a target FPGA supported by your CAD tool), an 16-bit ALU/function generator circuit by concatenating four instances of the 74181 circuit, which you designed to solve Question-(1). (4 marks)</li>

</ol>

– 2 –

<ol start="3">

 <li><strong>[Carry-Select Adder] </strong>Design, simulate (using a proper testbench) and implement in Verilog (on a</li>

</ol>

target FPGA supported by your CAD tool), a Carry-Select Adder circuit to add two 16-bit numbers.

<ol start="4">

 <li><strong>[Carry-Save Adder] </strong>Design, simulate (using a proper testbench) and implement in Verilog (on a target FPGA supported by your CAD tool), a Carry-Save Adder circuit capable of adding nine 16-bit numbers. Your design should consist of several Carry-Save Adder (CSA) blocks connected in a tree configuration, and a carry-lookahead adder in the last stage. (10 marks)</li>

</ol>