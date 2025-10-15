# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

1. Type the program in Quartus software.
2. Compile and run the program.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for inputs and outputs to generate the timing diagram.
5. For different input combinations generate the timing diagram

**PROGRAM**

1. module ex5(clk, sin, q);
2. input clk;
3. input sin;
4. output [3:0] q;
5. reg [3:0] q;
6. always @(posedge clk)
7. begin
8. q[0] <= sin;
9. q[1] <= q[0];
10. q[2] <= q[1];
11. q[3] <= q[2];
12. end
13. endmodule


Developed by: RIHAB ZAKKAIR HUSSAIN 

RegisterNumber: 25015140


**RTL LOGIC FOR SISO Shift Register**
<img width="590" height="381" alt="ex5" src="https://github.com/user-attachments/assets/aa2d6791-134d-48a4-a528-8216c628647c" />

**TIMING DIGRAMS FOR SISO Shift Register**
<img width="1912" height="242" alt="ex5 1" src="https://github.com/user-attachments/assets/d9a12749-3546-489d-83f5-caabf657fce0" />

**RESULTS**
the siso shift register have been implemented and validated using their funtional table in verilog hdl
