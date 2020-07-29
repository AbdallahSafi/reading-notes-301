## call stack :
    A call stack is a mechanism for an interpreter to keep track of its place in a script that calls multiple function.

    * When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.

    * Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.

    * When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.

    * If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.

        - call stack is synchronous.
        - data structure that uses the Last In, First Out (LIFO).


## stack overflow:
      A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.


## Types of error messages :
     
   1. Reference errors : Happend when you try to use a variable that is not yet declared.

   2. Syntax errors : This occurs when you have something that cannot be parsed in terms of syntax.

   3. Range errors : Try to manipulate an object with some kind of length and give it an invalid length and    this kind of errors will show up.

   4. Type errors : this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible.


## Debugging :
     
   - console.log()
   - Ctrl+o : choose your file to debug, click the line you wanna debug and refresh your page again (F5)
   

