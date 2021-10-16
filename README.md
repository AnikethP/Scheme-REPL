# Scheme-REPL

## Description:

A read–eval–print loop (REPL), also termed an interactive toplevel or language shell, is a simple interactive computer programming environment that takes single user inputs, executes them, and returns the result to the user. This project utilizes a read-eval-print loop to parse user input in the scheme language and evaluate it internally using Python.



## Implementation Overview:

Read: This step parses user input (a string of Scheme code) into the interpreter's internal Python representation of Scheme expressions (e.g. Pairs).
Lexical analysis occurs in scheme_tokens.py. This function returns a Buffer (from buffer.py) of tokens.
Syntactic analysis happens in scheme_reader.py, in the scheme_read and read_tail functions. Together, these mutually recursive functions parse Scheme tokens into the interpreter's internal Python representation of Scheme expressions.

Eval: This step evaluates Scheme expressions (represented in Python) to obtain values. Code for this step is in the main scheme.py file.

Print: This step prints the __str__ representation of the obtained value.

Loop: The logic for the loop is handled by the read_eval_print_loop function in scheme.py. 

File | Description
------------ | -------------
scheme.py | implements the REPL and a evaluator for Scheme expressions
scheme_reader.py | implements the reader for Scheme input. The Pair class and nil definition can be found here.
scheme_tokens.py | implements the tokenizer for Scheme input
scheme_builtins.py | implements built-in Scheme procedures in Python
buffer.py |implements the Buffer class, used in scheme_reader.py
ucb.py | utility functions for use in 61A projects

## Running the interpreter:

To start an interactive Scheme interpreter session, type:
```
python3 scheme.py
```
