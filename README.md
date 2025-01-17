# Unexpected Process Termination in Elixir Enum.each

This repository demonstrates an uncommon bug in Elixir related to using `Process.exit` within an `Enum.each` loop.  The issue arises because `Process.exit` terminates the current process immediately, potentially interrupting the iteration before it's fully completed. 

The `bug.ex` file showcases the problem, where the process unexpectedly terminates when it encounters the number 3.  The `bugSolution.ex` demonstrates a safer approach using a different function that handles potential interruptions more gracefully. 

This scenario is important for developers to understand because prematurely terminating processes during iteration can lead to data corruption or inconsistencies in applications where such loops are handling crucial tasks.  This should be avoided to ensure process stability and accurate completion of operations.