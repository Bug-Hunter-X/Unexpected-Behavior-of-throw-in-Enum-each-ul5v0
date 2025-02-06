# Elixir Enum.each with throw: Unexpected Behavior

This repository demonstrates an unexpected behavior of using `throw` inside `Enum.each` in Elixir. The `IO.puts("Next")` statement after the conditional `if` and `throw` will execute even after `throw` is called.

## Bug Report

When using `throw` to stop the `Enum.each` loop, subsequent code within the anonymous function still executes before the exception is raised. This can lead to unexpected program behavior that can be difficult to debug.

## Reproduction

1. Clone this repository.
2. Run the `bug.exs` file.
3. Observe the output. You'll notice that "Next" is printed even after `throw` is called.