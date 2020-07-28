# Refactoring & functional programming

## What is functional programming?

Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.

## Pure functions

- It returns the same result if given the same arguments (it is also referred as deterministic).
- It does not cause any observable side effects.

Pure functions are stable, consistent, and predictable. Given the same parameters, pure functions will always return the same result. We don’t need to think of situations when the same parameter has different results — because it will never happen.

## Immutability

Unchanging over time or unable to be changed.

When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.

pure functions + immutable data = referential transparency

## Refactoring JavaScript for Performance and Readability 

Refactoring means updating the source code without changing the behaviour of the application. Refactoring helps you keep your 
code solid, dry, and easy to maintain.

### When Should You Refactor Your Code?

A great time to refactor your code is when you are working with something that you need to write over and over again. This isn’t the only time that you can refactor your code, however, it’s extremely common to run into things that are repetitive.

### The Basics of Refactoring Your Code
To refactor your code, you can basically go through a fairly simple 3 step process. If you implement this into your coding habits, you will notice fairly quickly that your code will start to look much more professional and tidy. The image below shows the typical 3 step process that you should go through when refactoring your code.

![img](https://miro.medium.com/max/512/1*Xdo4SwpW5ztpjG7ObLB0TA.png)

### How Can You Guarantee Behavior Doesn’t Change?

The shorter answer, for us, is using tests and version control.

### TESTING JAVASCRIPT ITSELF

If you are testing extremely specific implementation details, you will at some point no longer be testing your program, but rather the environment itself. We’ll go over testing in detail later, but for now, you can run this either in a node console or by saving it to a file and running node file_name.js. That said, it’s not critical to do so at this point.




