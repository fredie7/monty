```
 ____  _             _         ___
/ ___|| |_ __ _  ___| | __    / _ \ _   _  ___ _   _  ___
\___ \| __/ _` |/ __| |/ /   | | | | | | |/ _ \ | | |/ _ \
 ___) | || (_| | (__|   < _  | |_| | |_| |  __/ |_| |  __/_
|____/ \__\__,_|\___|_|\_( )  \__\_\\__,_|\___|\__,_|\___( )
                         |/                              |/
 _____ ___ _____ ___     _     ___ _____ ___
|  ___|_ _|  ___/ _ \   | |   |_ _|  ___/ _ \
| |_   | || |_ | | | |  | |    | || |_ | | | |
|  _|  | ||  _|| |_| |  | |___ | ||  _|| |_| |
|_|   |___|_|   \___( ) |_____|___|_|   \___/
                    |/

```
# Stacks, Queues and Monty
  
The Monty lanaguage is a scripting language that is first compiled into Monty byte codes (Just like Python). It relies on a unique stack, with specific instructions to manipulate it. The goal of this project is to create an interpreter for Monty ByteCodes files.
  
## Usage  
Clone this repository and compile the files with:
```
$ gcc -Wall -Werror -Wextra -pedantic *.c -o monty
```  
To run the program, type: 
```
$ monty <file.m>
```
## Monty byte code files    
Files containing Monty byte codes usually have the .m extension. There is not more than one instruction per line. There can be any number of spaces before or after the opcode and its argument:  
```
$ cat -e bytecodes/000.m
push 0$
push 1$
  push 2$
                   pall    $
push 3$
pall$
$ monty bytecodes/000.m
3
2
1
0
2
1
0
$
```
## Monty opcode  
|Opcode|Description|
|------|-----------|
|push|Push an element onto the stack|
|pall|Print all the values on the stack, starting from the top|
|pint|Print the value at the top of the stack|
|pop|Remove the top element of the stack|
|swap|Swap the top two elements of the stack|
|add|Add the top two elements of the stack|
|nop|Doesn't do anything|
|sub|Subtract the top element of the stack from the second element of the stack|
|div|Divide the second element of the stack by the top element of the stack|
|mul|Multiply the second element of the stack with the top element of the stack| 
|mod|Compute the modulus of the second element of the stack by the top element of the stack|
|pchar|Print the ASCII equivalent of the number at the top of the stack|
|pstr|Print the ASCII equivalent of the numbers stored in each element in the stack, starting from the top|
|rotl|Rotate the top element of the stack to the bottom of the stack|
|rotr|Rotate the bottom element of the stack to the top of the stack|
|queue|Switch mode to queue: the top of the stack becomes the front of the queue|
|stack|Switch mode to stack: the top of the queue becomes the top of the stack|

## Author
* [Matthew Utti]
