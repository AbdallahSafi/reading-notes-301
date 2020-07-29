### Call stack
* mechanism for an interpreter to keep track of its place in a script that calls multiple functions
  * script calls a function, the interpreter adds it to the call stack and then carrying out the function.
  * function are added to the call stack further up, and run where their calls are reached.
  * unction is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.
#### Understanding the JavaScript call stack:
* is a single-threaded interpreter comprising of a heap and a single call stack.
* used for function invocation. Since the call stack is single
* function execution,from top to bottom. It means the call stack is synchronous.
* In Asynchronous JavaScript, we have a callback function, an event loop, and a task queue. 
* a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function 
* It is single-threaded. Meaning it can only do one thing at a time
* Code execution is synchronous.
* A function invocation creates a stack frame that occupies a temporary memory.
* It works as a LIFO — Last In, First Out data structure.
#### JavaScript error messages && debugging
* Types of error messages:
  * Reference errors:This is also a common thing when using const and let, they are hoisted like var and function but there is a time between the hoisting and being declared.
  * Syntax errors:when you have something that cannot be parsed in terms of syntax.
  * Range errors:invalid length (negative length).
* debugging
  * console.log() the variables you want to check.
  * using chrome developer tools.


