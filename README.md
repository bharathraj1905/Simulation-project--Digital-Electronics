# TITTLE
## design and simulate a 7 bit parity generator using verilog
# THEORY
So today we will see an application of XOR Gate, which is parity generation. A parity bit is used for the purpose of detecting errors during the transmission of binary information. A parity bit is an extra bit included with the binary message to make the number of ones either even or odd. An error is detected if the checked parity doesn’t correspond with the one transmitted.
The circuit that generates the parity bit is called parity generator. So with this explanation, let us design an even  parity generator. Here is the truth table of an even parity generator.
# LOGIC DIAGRAM
![WhatsApp Image 2023-06-18 at 10 47 05 AM](https://github.com/bharathraj1905/Simulation-project--Digital-Electronics/assets/121490575/45f9ceae-54ea-430c-a2ba-04acf5333c36)

# NETLIST DIAGRAM

![WhatsApp Image 2023-06-18 at 10 47 05 AM](https://github.com/bharathraj1905/Simulation-project--Digital-Electronics/assets/121490575/45f9ceae-54ea-430c-a2ba-04acf5333c36)

# TIMING DIAGRAM

![WhatsApp Image 2023-06-18 at 10 51 09 AM](https://github.com/bharathraj1905/Simulation-project--Digital-Electronics/assets/121490575/7d1cddfe-092e-467d-b833-bbf313b34236)


# PROGRAM
module parity (a, y); 
input [6:0]a; 
output y; 
wire w, w2, w3, w4, w5;
xor(w1, a[6], a[5]);
xor(w2, w1, a[4]);
xor(w3, w2,a[3]);
xor(w4, w3,a[2]);
xor(w5,w4,a[1]);
xor(y,w5,a[0]);
endmodule
# REFERENCE
https://youtu.be/c8qAti1zBVQ
