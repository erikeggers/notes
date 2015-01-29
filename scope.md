# Scope
## Context
Context means the context in which code is executing (scope, strict mode, value of `this`)
- Global context
- Function context is created every time a function is executed.

## Scope
Answers the questions "Where do variables live and how does my code find them?"
- Global
- Function

## Hoisting
Variable declarations **but not assignments** are moved to the top of their scope.

Both the declaration and body for function declarations are hoisted.

Only the declaration for function expressions is hoisted.

# `this`
A JavaScript keyword that evaluates to different values in different execution contexts.

- Global and global functions
- Inside methods (even if the function was added to the object later)
- jQuery
