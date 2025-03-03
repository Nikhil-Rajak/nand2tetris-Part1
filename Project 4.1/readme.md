Multiplication Program (Mult.asm)

Overview

This program performs multiplication of two numbers stored in RAM[0] (R0) and RAM[1] (R1) using repeated addition. The result is stored in RAM[2] (R2). The implementation follows the Hack Assembly language and is designed for the Hack computer, as described in "The Elements of Computing Systems" by Nisan and Schocken.

Algorithm

The program follows these steps:

Load the value of R1 (RAM[1]) into a counter variable i.

Initialize R2 (RAM[2]) to 0.

Loop until i becomes 0:

Add the value of R0 (RAM[0]) to R2 (RAM[2]).

Decrease i by 1.

When i reaches 0, the loop terminates, and the final result remains in R2 (RAM[2]).

Code Explanation

(START): Label marking the beginning of the program.

@R1 D=M @i M=D: Load the value of R1 into i.

@R2 M=0: Initialize R2 to 0.

(LOOP): Loop label.

If i is 0, jump to (END).

Add R0 to R2.

Decrease i by 1.

Jump back to (LOOP) if i is not 0.

(END): Infinite loop to halt the program.

Limitations

This implementation assumes that both R0 and R1 are non-negative integers.

It does not handle cases where R0 or R1 is negative.

Multiplication is implemented using repeated addition, making it inefficient for large numbers.

Usage

Load the program into the Hack assembler.

Set values in R0 and R1 before running the program.

Run the program.

Read the result from R2.
