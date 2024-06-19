The Monty language is a programming language designed to bridge the gap between scripting and programming languages


It is intended to be easy to use like a scripting language while offering the capabilities and structure of a programming language. Monty is used with a specific interpreter that reads Monty bytecode files and executes commands accordingly, managing data structures like stacks and queues (LIFO and FIFO).

##                                                               RESOURCES
* https://stackoverflow.com/questions/1433204/how-do-i-use-extern-to-share-variables-between-source-files
* https://data-flair.training/blogs/stacks-and-queues-in-c/
* https://www.edureka.co/blog/queue-in-c/
* https://www.digitalocean.com/community/tutorials/stack-in-c

## Technologies
* Interpreter was written with C 
* Tested on Ubuntu 14.04 LTS

## Usage
 Compile all files:

```bash
$ gcc -Wall -Werror -Wextra -pedantic *.c -o monty
$
```

















 
 


 Run the interpreter:

```bash

$ ./monty [file name].m
2
1
0
2
1
$
```
* output is printed on stdout
* Any error message is printed on stderr



## OpCode
`Monty features and executes these opcodes`:

| Opcode | Description |
| -------- | ----------- |
| `add` | Adds the top two elements of the stack |
| `sub` | Subtracts the top element of the stack from the second top element of the stack | 
| `push` | Pushes an element to the stack |
| `pall` | Prints all the values on the stack |
| `pint` | Prints the value at the top of the stack |
| `pop` | Removes the top element of the stack |
| `swap` | Swaps the top two elements of the stack |
| `queue` | Sets the format of the data to a queue (FIFO) |
| `stack` | Sets the format of the data to a stack (LIFO) |
| `mul` | Multiplies the second top element of the stack with the top element of the stack |
| `div` | Divides the second top element of the stack by the top element of the stack |
| `mod` | Computes the rest of the division of the second top element of the stack by the top element of the stack |
| `pchar` | Prints the char at the top of the stack |
| `pstr` | Prints the string starting at the top of the stack |
| `rotl` | Rotates the stack to the top |
| `rotr` | Rotates the stack to the bottom |
| `nop` | Doesn't do anything |

## Examples
```
anoona@ubuntu:~/monty$ cat -e bytecodes/000.m
push 0$
push 1$
push 2$
  push 3$
                   pall    $
push 4$
    push 5    $
      push    6        $
pall$
anoona@ubuntu:~/monty$
```
Monty byte code files can contain blank lines (empty or made of spaces only, and any additional text after the opcode or its required argument is not taken into account:
```
anoona@ubuntu:~/monty$ cat -e bytecodes/001.m
push 0 Push 0 onto the stack$
push 1 Push 1 onto the stack$
$
push 2$
  push 3$
                   pall    $
$
$
                           $
push 4$
$
    push 5    $
      push    6        $
$
pall This is the end of our program. Monty is awesome!$
anoona@ubuntu:~/monty$
```

## Author
* Anoona Sithole
