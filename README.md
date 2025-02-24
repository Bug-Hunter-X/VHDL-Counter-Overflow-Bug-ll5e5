# VHDL Counter Overflow Bug

This repository demonstrates a common bug in VHDL code: an integer counter that can overflow.  The `buggy_counter.vhdl` file contains the erroneous code, while `fixed_counter.vhdl` provides a corrected version.

The bug occurs because the counter increments without any check for the upper bound of its range. This means that when the counter reaches its maximum value (15 in this case), the next increment will cause an overflow. The behavior after the overflow is unpredictable and depends on the simulator and synthesis tool.

The solution involves adding a check to prevent the counter from exceeding the upper bound.