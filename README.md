# Evaluation-of-arithmetic-expressions (Assembly)
Program that evaluates a postfix arithmetic expression.

The program go through the input string, checking one character at a time. In case of findind a digit, it is saved in ecx register and continues searching for new digits and adding them in ecx (old number * 10 + current digit) until it finds a blank space. Number stored in ecx is pushed on the stack, ecx is reset and then begins the search for the next number. In case of finding one of the following characters: "+", "*", "/", the program will perform the appropiate operation between the last two numbers pushed on stack. When the character "-" is found: if it is followed by a blank space or the string terminator, it performs the subtraction between last two numbers pushed on stack, otherwise, it starts creating a negative number in ecx. When string terminator is found, the program will display the last number saved on the stack.
