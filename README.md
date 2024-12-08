# VHDL Integer Overflow Bug

This repository demonstrates a common, yet subtle, bug in VHDL code: integer overflow in a simple counter.  The `counter` entity uses an integer type with a limited range (0 to 15). When the counter reaches 15, incrementing it causes an overflow. This leads to unexpected behavior without proper error handling.

The `bug.vhdl` file contains the buggy code.  The `bugSolution.vhdl` file demonstrates a solution that prevents this overflow.

## How to Reproduce

1. Synthesize and simulate `bug.vhdl`.  Observe the counter's behavior when it reaches its maximum value.
2. Synthesize and simulate `bugSolution.vhdl` to see the corrected behavior.

## Solution

The solution involves checking for the maximum value before incrementing.  This prevents the overflow and maintains predictable behavior.
