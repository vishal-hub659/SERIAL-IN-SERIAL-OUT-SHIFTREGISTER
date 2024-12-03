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

/* write all the steps invloved */
~~~
**PROGRAM**
module de10(clk, sin, q);
input clk;
input sin;
output [3:0] q;
reg [3:0] q;
always @(posedge clk)
begin
q[0] <= sin;
q[1] <= q[0];
q[2] <= q[1];
q[3] <= q[2];
end
endmodule
/* Program for flipflops and verify its truth table in quartus using Verilog programming.

Developed by: vishal s
RegisterNumber:24008833
~~~
*/

**RTL LOGIC FOR SISO Shift Register**
![Screenshot 2024-12-03 175912](https://github.com/user-attachments/assets/902b88d9-ef29-4f06-b312-7a8035e359e3)

**TIMING DIGRAMS FOR SISO Shift Register**
![Screenshot 2024-12-03 180056](https://github.com/user-attachments/assets/9b1edbc8-1872-4e6d-b955-ef792cbfddfa)

**RESULTS**
The 4-bit SISO (Serial-In Serial-Out) shift register was successfully implemented using Verilog in Quartus Prime. The functionality was validated using the truth table. The shift register correctly shifted the input data one bit at a time through the flip-flops on each clock pulse. The outputs q0, q1, q2, and q3 were observed to propagate the input data as expected, confirming the correct operation of the shift register.
