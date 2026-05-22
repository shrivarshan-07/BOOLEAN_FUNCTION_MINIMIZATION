# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: Shrivarshan
RegisterNumber:212225240146 */

```
module EXP2 (
    input A, B, C, D,
    input w, x, y, z,
    output F1, F2
);

// F1 Implementation
assign F1 = (~A & ~B & ~C & ~D) |
            (A & ~C & ~D) |
            (~B & C & ~D) |
            (~A & B & C & D) |
            (B & ~C & D);

// F2 Implementation
assign F2 = (x & ~y & z) |
            (~x & ~y & z) |
            (~w & x & y) |
            (w & ~x & y) |
            (w & x & y);

endmodule
```




**RTL:**

<img width="712" height="821" alt="Screenshot 2026-05-21 183723" src="https://github.com/user-attachments/assets/7fb7194f-a2c0-4d94-b578-a936535a0373" />


**Output : Timing diagram**
<img width="1918" height="545" alt="Screenshot 2026-05-21 184144" src="https://github.com/user-attachments/assets/3ccfb514-902c-4be8-9e8b-b4c436c1e55a" />

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

