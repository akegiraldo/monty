# Monty

## Desciption

Monty 0.98 is a scripting language that is first compiled into Monty byte codes (Just like Python). It relies on a unique stack, with specific instructions to manipulate it. The goal of this project is to create an interpreter for Monty ByteCodes files.

## Installation

1. To use monty you must first access the console and clone the repository with the following command:<br>
`git clone https://github.com/Doouh/monty.git`
2. Once you have the cloned repository, you must access the folder and compile all the files inside it with the following command:<br>
`cd monty`<br>
`gcc -Wall -Werror -Wextra -pedantic *.c -o monty`<br>
3. Now you can use monty passing the path of a file with Monty byte code as an argument to the generated executable:<br>
`monty file_path`<br><br>
In the [Examples](#examples) section you can see some usage examples

## File Index
|File name              |Description                         |
|-----------------------|------------------------------------|
|[additionalFunctions_0](additionalFunctions_0.c)|- `freestack`: Receive a stack per parameter and delete it.<br>- `_isdigit`: It receives a character by parameters and returns 1 or 0 if it is a number or not.|
|[functions_0](functions_0.c)|- `push`: Receives a stack and a number per parameter and adds this as a new node to the stack.<br>- `pall`: It receives a stack per parameter and prints all the values it has stored.<br>- `pint`: Receive a stack per parameter and print the value of the first node.<br>- `nop`: It receives a stack per parameter and does nothing with it.<br>- `swap`: Receive a stack per parameter and swap the first two nodes between them.|
|[functions_1](functions_1.c)|- `pop`: Receive one stack per parameter and remove the first node.<br>- `add`: Receives a stack per parameter adds the values of the first two nodes and removes them, and saves a new node with the sum.<br>- `sub`: Receives a stack per parameter subtracts the values of the first two nodes and removes them, and saves a new node with the subtraction.<br>- `division`: Receives a stack per parameter divides the values of the first two nodes and removes them, and saves a new node with division.<br>- `mul`: Receives a stack per parameter multiplies the values of the first two nodes and removes them, and saves a new node with the multiplication.|
|[functions_2](functions_2.c)|- `mod`: Receives a stack per parameter calculates the modulus between the values of the first two nodes and removes them, and saves a new node with the result.<br>- `pchar`: Receive a stack per parameter, convert the value of the first node into char and print it.<br>- `pstr`: Receive a stack per parameter, convert the value of each node into character and print it.|
|[main](main.c)|- `main`: It's our main function, it receives a file per parameter and starts reading it line by line, for each one of them it verifies by means of the `is_opcode` function if it is one of the preset options.<br>- `parse`: It receives a string per parameter and removes tabs, line breaks and spaces from it, to later check if it is a valid option.<br>- `is_opcode`: It receives a stack per parameter and a string, uses the `parse` function to obtain only valid values from among the string and checks if they are in the list of preset options, if so, calls the respective function according to the chosen option and it passes to this the stack by parameter.<br>- `check_push`: Check if an element passed by parameter is of the necessary format to be saved in the stack, if so, do the push.|
|[monty](monty.h)|This file is the header of our entire program, it contains the prototypes of all the functions described in this index and the structure used to call the functions.|


## Examples
* Some examples of using monty and its console output.

|Example #1             |Example #2             |Example #3             |
|-----------------------|-----------------------|-----------------------|
|\~/monty$ cat -e bytecodes/00.m<br>push 1$<br>push 2$<br>push 3$<br>pall$<br>\~/monty$ ./monty bytecodes/00.m<br>3<br>2<br>1<br><br><br><br><br><br><br><br><br><br>|\~/monty$ cat bytecodes/07.m<br>push 1<br>push 2<br>push 3<br>pall<br>pop<br>pall<br>pop<br>pall<br>pop<br>pall<br>\~/monty$ ./monty bytecodes/07.m<br>3<br>2<br>1<br>2<br>1<br>1|\~/monty$ cat bytecodes/09.m<br>push 1<br>push 2<br>push 3<br>pall<br>swap<br>pall<br>\~/monty$ ./monty bytecodes/09.m<br>3<br>2<br>1<br>2<br>3<br>1<br><br><br><br><br>|

## Authors

* [Camilo Andrés Isaza](https://github.com/andresmelek)
* [Kevin Adrian Giraldo](https://github.com/Doouh)
