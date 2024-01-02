# Developed by: mukesh kumar S
# Register Number: 212223240099

# EXP-03 Implementation-of-Half-Adder-and-Full-Adder-circuit

## Aim:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime
 
## Procedure:

Connect the supply (+5V) to the circuit

Switch ON the main switch

If the output is 1, then the led glows.

## Theory:
Adders are digital circuits that carry out addition of numbers.

### Half Adder:
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

#### Figure -01 HALF ADDER:
![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

### Full Adder:
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

#### Figure -02 FULL ADDER: 
![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

## Program:
Program to design a half and full adder circuit and verify its truth table in quartus using Verilog programming.
````
module half_adder(A,B,C,S);
input A,B;
output S,C;
assign c=A&B;
assign S=A^B;
endmodule

module FullAdder(a,b,carryin,sum,carryout);
input a,b,carryin;
output sum,carryout;
wire x,p,q,r;
xor(x,b,carryin);
xor(sum,x,a);
and(p,a,b);
and(q,b,carryin);
and(r,a,carryin);
or(carryout,p,q,r);
endmodule
````

## Output:
### Logic symbol & Truthtable:
#### Half Adder:
![291240788-11615dbf-2ba8-4e05-9fd9-334496a9e29f](https://github.com/RoopakCS/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139228922/b7726a5e-76e8-4ccb-a0c9-a96e09cd739b)
#### Full Adder:
![image](https://github.com/RoopakCS/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139228922/6350eef8-0284-423e-97a2-573b79d608f8)

### RTL realization:
#### Half Adder:
![half_adder](https://github.com/RoopakCS/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139228922/4a9d2719-adf4-436c-b10f-c99d97a4181f)
#### Full Adder:
![FullAdder](https://github.com/RoopakCS/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139228922/49e5eaf0-9b8e-4b41-b028-4cf8fc1ca481)

### Timing diagram:
#### Half Adder:
![Half Adder Waveform](https://github.com/RoopakCS/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139228922/42c8ff56-e7e1-4a45-b988-30e2b1a5ebb6)
#### Full Adder:
![FullAdder Waveform](https://github.com/RoopakCS/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139228922/02796a7d-0d74-44e3-989b-f7a95bf59032)

# Result:
Thus the given logic functions are implemented and their operations are verified using verilog programming.
