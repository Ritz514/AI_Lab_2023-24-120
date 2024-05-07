# Ex.No: 7  Logic Programming –  Logic Circuit Design
### DATE: 23-03-2024                                                                           
### REGISTER NUMBER : 212221040120
### AIM: 
To write a logic program to design a circuit like half adder and half subtractor.
###  Algorithm:
1. Start the Program
2. Design a AND gate logic if both inputs are 1 then output is 1.
3. Design a OR gate logic if any one of input is 1 then output is 1.
4. Design a XOR gate logic if both inputs are different then output is 1.
5. Design a NOT gate logic if input is 0 then output is 1.
6. Design a half adder and half subtractor using the rules.
7. Test the logic.
8. Stop the program.

### Program:
xor(0,1,1).
xor(0,0,0).
xor(1,0,1).
xor(1,1,0).
and(1,1,1).
and(0,0,0).
and(0,1,0).
and(1,0,0).
not(0,1).
not(1,0).
or(0,1,1).
or(1,0,1).
or(0,0,0).
or(1,1,1).
halfadder(A,B,Sum,Carry):-
    xor(A,B,Sum),
    and(A,B,Carry).
halfsubtractor(A,B,Diff,Carry):-
    xor(A,B,Diff),
    not(A,C),
    and(C,B,Carry).
fulladder(A,B,Cin,S,Cout):-
    xor(A,B,X),
    xor(X,Cin,S),
    and(X,Cin,Y),
    and(A,B,Z),
    or(Y,Z,Cout).










### Output:


![316254164-011aee51-6e27-4dfe-8d20-09670866a43e](https://github.com/Ritz514/AI_Lab_2023-24-120/assets/142646304/f3f61f6f-4ac4-4e18-9b06-3b3b41297eb9)

![316254251-0c0edf41-6d7d-475a-8a2b-f6efa65408ed](https://github.com/Ritz514/AI_Lab_2023-24-120/assets/142646304/acbfd7d4-9b51-4193-93![316254316-150fe1d5-0f8c-4d8a-a1a1-2c8f6627a7e9](https://github.com/Ritz514/AI_Lab_2023-24-120/assets/142646304/7772423a-cb23-484f-801b-a5efd6e82e58)
40-7fffc6e26d7c)


### Result:
Thus the truth table of circuit verified sucessfully.
