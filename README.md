# Elixir List Modification During Enum.each

This example demonstrates the unexpected behavior when attempting to modify a list while iterating using `Enum.each`.  Directly modifying the list within the `Enum.each` callback does not modify the original list. This is a common source of confusion for programmers coming from other languages.

The solution explores alternative methods such as using `Enum.filter` or `Enum.reduce` to achieve the desired list modification.

## How to reproduce the bug
1. Copy the code from `bug.exs`.
2. Run the code using an Elixir shell (`iex -S mix`).
3. Observe the output. You'll see that the list remains unchanged despite the attempt to remove elements within the loop.