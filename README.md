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
In the `Examples` section you can see some usage examples

## File Index
|File name              |Description                         |
|-----------------------|------------------------------------|
|[_printf](https://github.com/Doouh/printf/blob/master/_printf.c)|- `_printf`: Our main function and the first one that is executed when using our program, which contains a structure with all the allowed formats and initializes a list with the arguments passed as parameters.<br>- `iterator`: Function that iterates the entire line of text that the user wants to print and depending on the format found, print the text or call one of our functions.|
|[_putchar](https://github.com/Doouh/printf/blob/master/_putchar.c)|- `_putchar`: Function that writes the character passed as argument to stdout|
|[additionalFunctions](https://github.com/Doouh/printf/blob/master/additionalFunctions.c)|- `print_number`: Prints by character a negative or positive number passed as parameter.<br>- `get_octal`: Converts a number passed by parameter to octal base and prints it.<br>- `get_hex`: Converts a number passed by parameter to hex base and prints it.<br>- `get_bin`: Converts a number passed by parameter to binary base and prints it.|
|[functions_0](https://github.com/Doouh/printf/blob/master/functions_0.c)|- `p_c`: Receive a character and print it using `_putchar`.<br>- `p_s`: Receive a string and print it using `_putchar`.<br>- `p_p`: Print the percentage symbol.<br>- `p_d`: Print a decimal number using the `print_number` function.<br>- `p_i`: Print a decimal number using the `print_number` function.|
|[functions_1](https://github.com/Doouh/printf/blob/master/functions_1.c)|- `p_u`: Receive an unsigned number and print it using the `print_number` function.<br>- `p_o`: Receive an unsigned number and print it as octal using the `get_octal` function.<br>- `p_x`: Receive an unsigned number and print it as a lowercase hexadecimal using the `get_hex` function.<br>- `p_X`: Receive an unsigned number and print it as a uppercase hexadecimal using the `get_hex` function.<br>- `p_b`: Receive an unsigned number and print it as binary using the `get_bin` function.|
|[functions_2](https://github.com/Doouh/printf/blob/master/functions_2.c)|- `p_S`: Receive a string and print it using `_putchar`, special characters will be printed in hexadecimal using `get_hex`.<br>- `p_r`: Receive a string and print it reversed using `_putchar`.<br>- `p_a`: Receive an address in memory and print it using `_putchar` and `get_hex`.|
|[holberton](https://github.com/Doouh/printf/blob/master/holberton.h)|This file is the header of our entire program, it contains the prototypes of all the functions described in this index and the structure used to call the functions.|


### EXAMPLES
* Some examples of using printf and its console output.

 - _printf("%%");
 - > %
 - _printf("%s", "Hello, world!");
 - > Hello, world!
 - _printf("La %s %c%C para %s%c%c%c%s robot.\n", "política", 'e', 's', "marionetas", '.', 32, 45, "Mr");
 - > La política es para marionetas. -Mr robot.

## Authors

* **Camilo Andrés Isaza** - *Initial work* - [PurpleBooth](https://github.com/andresmelek)
* **Kevin Adrian Giraldo** - *Initial work* - [PurpleBooth](https://github.com/Doouh)
