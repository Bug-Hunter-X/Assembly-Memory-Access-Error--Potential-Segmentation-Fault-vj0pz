# Assembly Memory Access Bug

This repository demonstrates a common error in assembly programming: out-of-bounds memory access.

The `bug.asm` file contains assembly code that calculates a memory address and attempts to read from it.  This calculation is prone to errors, potentially causing a segmentation fault if the calculated address falls outside of the allocated memory region.

The `bugSolution.asm` file provides a corrected version of the code, incorporating bounds checking to prevent out-of-bounds memory access.

## Potential causes of this bug:

* Incorrect calculation of memory offset
* Uninitialized or corrupted register values
* Failure to check array bounds before access

## How to reproduce the bug:

1. Assemble `bug.asm` using your preferred assembler (NASM, MASM, etc.).
2. Link and run the resulting executable.
3. Observe the segmentation fault (or other unexpected behavior) when the program attempts to access memory outside of the allocated space.

## How the solution addresses the bug:

The solution adds explicit bounds checking to the memory access operation.  This ensures that the calculated address is always within the limits of allocated memory before attempting to access it.