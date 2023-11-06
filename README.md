# EXP-04-IMPLEMENTATION OF HALF SUBTRACTOR AND FULL SUBTRACTOR CIRCUIT

## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## EQUIPMENTS REQUIRED:
1. Hardware – PCs, Cyclone II , USB flasher
2. Software – Quartus prime
 
## THEORY:
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.
Half Subtractor Full Subtractor
### Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![image](https://github.com/ChandrasekarS22008273/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119643845/01ae302f-9127-42ff-88c4-7f0751975d3b)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

### Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![image](https://github.com/ChandrasekarS22008273/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119643845/66315a0b-b8d5-49f6-8318-dba4e494511d)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## PROCEDURE:
1. Connect the supply (+5V) to the circuit
2. Switch ON the main switch
3. If the output is 1, then the led glows.



## PROGRAM:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: CHANDRASEKAR S
RegisterNumber: 212222230025

1. Program to design a half subtractor:

module ex4(a,b,diff,borr);
input a,b;
output diff,borr;
assign diff=(a^b);
assign borr=((~a)&b);
endmodule 

2. Program to design a full subtractor:

module ex41(a,b,bin,diff,borr);
input a,b,bin;
output diff,borr;
assign diff=a^b^bin;
assign borr=((~a)&b)|(b&bin)|((~a)&bin);
endmodule 
```

## TRUTH TABLE:
### HALF SUBTRACTOR
![image](https://github.com/ChandrasekarS22008273/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119643845/5df616cb-1743-4ccd-9131-6fe5c582aa49)


### FULL SUBTRACTOR
![image](https://github.com/ChandrasekarS22008273/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119643845/c84f6e56-f1fd-4437-bf3a-345fd7bf455f)


## RTL REALIZATION:
### HALF SUBTRACTOR
![image](https://github.com/ChandrasekarS22008273/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119643845/8efbc6f1-6e14-460f-8285-3daccd10340c)

### FULL SUBTRACTOR
![image](https://github.com/ChandrasekarS22008273/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119643845/78992fda-f96a-464d-aa0d-5521cdc6eb6c)


## OUTPUT WAVEFORM:
### HALF SUBTRACTOR
![image](https://github.com/ChandrasekarS22008273/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119643845/4bc2ab09-5802-4264-a223-23c420cad42c)

### FULL SUBTRACTOR
![image](https://github.com/ChandrasekarS22008273/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119643845/0f29e562-41ba-4b26-bcaa-9f2544d1145f)

## RESULT:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
