# Ben Eater's 8-bit Computer Assembly Compiler

A code assembler for Ben Eater's 8-bit computer, written in Python.

This was not made by or at the request of Ben Eater, purely fan made by me.  You will still need to program an Arduino or Raspberry Pi to import the compiled file onto the RAM.

More info at https://eater.net/8bit

### Basic Example
Here is an example from the Conditional Jump Instructions video.

```
start:
  OUT
  ADD $F
  JC continue
  JMP start

continue:
  SUB $F
  OUT
  JZ start
  JMP continue
  
  .org 15
  .word 1
```

To compile it simply type:

```
python compiler.py name_of_file.txt -o out_file.bin
```
