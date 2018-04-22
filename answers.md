#Lab 02: Tools and Context

1. When this code is run in Node, e.g. node index.js, what are the two stages of execution for this file called, and which order do they happen in?

- Compilation phase and then Execution phase

2. Write an explanation, using as much space as you need, relating to how the first stage of execution for this file operates.

For example, identify the high level steps in a line by line overview and then define what each of those steps are accomplishing.

- First the code is scanned to find var foo and function bar() during the compilation phase. Then var foo and function bar() are hoisted to the top of the code to proceed with the execution phase.

3. Write an explanation, using as much space as you need, relating to how the second stage of execution for this file operates.

For example, identify the high level steps in a line by line overview and then define what each of those steps are accomplishing.

- When code is executed, the variables are then assigned their respected values, starting with var foo taking the function bar(), var foo taking in the function baz(). 

4. During the second stage of execution how many scopes have been registered by the engine?
Which segments of the code do they belong to?
Please identify any variables/refs and which scope each belongs to?

- There are three different scopes: global scope which is the entire code itself, bar scope which has a reassigned foo and it's own instance of baz, and the baz scope which has it's own scope of foo and bam.

5. When line 13 invokes the baz function, which foo will be assigned a value of bam? More specifically, bam will be assigned to the foo in ??? scope. Give a brief description in your own words to support your conclusion.

- The baz function's foo will not be reassigned because no argument was called with that particular foo.

6. Which scope, if any, will the variable bam on line 11 be registered to when the first stage of execution occurs on this file? Provide a brief description in your own words to support your conclusion.

- That particular bam is in the scope of baz but is not a variable nor does it have a legitamte value to be considered as such, therefore it remains in place.

7. For each line, 16 through 19, what is the return value for each?

bar(); - reference error, cannot find variable bam

foo; - returns 'bar'

bam; - reference error, cannot find variable bam

baz(); reference error, cannot find function baz