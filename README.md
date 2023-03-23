#  C - Stacks, Queues - LIFO, FIFO.
----------

## The Monty language

`Monty 0.98` is a scripting language that is similar to Python in its syntax and semantics. It is designed to be easy to learn and use, with a focus on readability and simplicity. Monty code is first compiled into Monty byte codes, which are then executed by a virtual machine.

## More information on the Monty language

> * Monty programs are typically saved with a .monty file (`.m`) extension. Most of the industry uses this standard but it is not required by the specification of the language. The syntax of Monty is similar to that of Python, with a few differences. For example, Monty uses `:=` instead of `=` for `variable assignment`, and uses `// ` for `integer division` instead of `/ `.

Example (`file.m`):
                
                $ cat file.m
                # Pushing element to the stack
                push 0
                push 1
                push 2
                # Printing all elements
                pall
                push 3
                push 4
                pop
                # Rotating the stack to the bottom
                rotr
                pall
                rotl
                # Setting FIFO
                queue
                push 5
                # Setting LIFO
                stack
                push 5
                $
 

## Syntax

* Monty uses indentation to indicate blocks of code, similar to Python
* Comments begin with a `#` character and continue until the end of the line
* Variables are assigned using the ':=' operator, e.g. `x := 5`
* Arithmetic operations use the usual symbols, e.g. `+`, `-`, `*`, `/`, `//`, `**`

## Data Types
* Monty supports `integers`, `floats`, `strings`, and `lists`
* Lists are created using square brackets and can contain any type of data, e.g. [`1, 2, "hello"`]

## Control Structures

* Monty has `if/else` statements for conditional branching
* Loops are implemented using `while` and `for` statements
* Monty also supports the `break` and `continue` keywords to control loop execution

## Functions

* Monty allows for the definition of user-defined functions using the `def` keyword
* Functions can take arguments and return values using the `return` keyword
* Recursive functions are supported

## Input/Output

* Monty has built-in functions for printing to the console (`print`) and reading input from the user (`input`)

## Coroutines

* Monty supports coroutines, which allow for cooperative multitasking
* Coroutines are defined using the `coroutine` keyword and use the `yield` keyword to pause and resume execution

## General Requirements for the Project

* The Monty interpreter in this project was compiled using the C programming language
* All files are compiled on `Ubuntu 20.04 LTS` using gcc
* All codes use the `Betty` style. 
* The prototypes of all functions are included the header file called `monty.h`

## Bytecode Compilation

* Monty code is compiled into Monty byte code, which is then executed by a virtual machine
* The Monty byte code consists of a sequence of instructions, each with an opcode and operand
* The Monty virtual machine interprets the byte code and executes the corresponding instructions

## Usage
In this project: all codes are compiled by using:
           
           $ gcc -Wall -Werror -Wextra -pedantic *.c -o monty
           $

> All outputs must be printed on `stdout`

> All error messages must be printed on `stderr`

The rundown of the interpreter is the following:
           
           $ ./monty [filename]
           $

To run the interpreter:

           $ ./monty file.m
           2
           1
           0
           0
           3
           2
           1
           $

## Features (Opcodes)

`Monty` executes the following opcodes:
