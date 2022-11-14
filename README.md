# Push_swap

Sort a random list of integers using the smallest number of moves, 2 stacks and a limited set of operations.


You start with two empty stacks: a and b. You are given a random list of integers via command line arguments.


Only these moves are allowed:

- sa : swap a - swap the first 2 elements at the top of stack a. Do nothing if there is only one or no elements).
- sb : swap b - swap the first 2 elements at the top of stack b. Do nothing if there is only one or no elements).
- ss : sa and sb at the same time.
- pa : push a - take the first element at the top of b and put it at the top of a. Do nothing if b is empty.
- pb : push b - take the first element at the top of a and put it at the top of b. Do nothing if a is empty.
- ra : rotate a - shift up all elements of stack a by 1. The first element becomes the last one.
- rb : rotate b - shift up all elements of stack b by 1. The first element becomes the last one.
- rr : ra and rb at the same time.
- rra : reverse rotate a - shift down all elements of stack a by 1. The last element becomes the first one.
- rrb : reverse rotate b - shift down all elements of stack b by 1. The last element becomes the first one.
- rrr : rra and rrb at the same time.

At the end, stack b must empty empty and all integers must be in stack a, sorted in ascending order.

-----------------
The Project
Create two programs: checker and push_swap.

The checker program reads a random list of integers from the stdin, stores them, and checks to see if they are sorted.

The push_swap program calculates the moves to sort the integers – pushing, popping, swapping and rotating them between stack a and stack b – and displays those directions on the stdout.

You can pipe push_swap into checker, and checker will verify that push_swap's instructions were successful.

Both programs must mandatorily parse input for errors, including empty strings, no parameters, non-numeric parameters, duplicates, and invalid/non-existent instructions.

-> Push_Swap must conform to the 42 Norm.

Using normal libc functions is strictly forbidden. Students are however, allowed to use: write, read, malloc, free, exit. It must not have any memory leaks. Errors must be handled carefully.

In no way can it quit in an unexpected manner (segmentation fault, bus error, double free, etc).
