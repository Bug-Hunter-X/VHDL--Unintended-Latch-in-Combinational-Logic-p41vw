# VHDL Unintended Latch Bug
This repository demonstrates a common error in VHDL: an unintended latch created by missing signal assignments in a process.

## Bug Description
The VHDL code in `bug.vhdl` contains a process that intends to assign the input `data_in` to the output `data_out`. However, due to a missing assignment in the process's `else` case, a latch is created. This unintended latch can cause unexpected behavior and incorrect output.

## Bug Solution
The solution is provided in `bugSolution.vhdl`. This version explicitly assigns a value to `data_out` in all cases to avoid the unintended latch.

## How to Reproduce
1. Simulate the `bug.vhdl` code. Observe that the `data_out` signal does not update predictably.
2. Simulate the `bugSolution.vhdl` code. Observe that the `data_out` signal now updates correctly.