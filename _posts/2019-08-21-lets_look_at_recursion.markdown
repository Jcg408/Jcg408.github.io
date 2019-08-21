---
layout: post
title:      "Let's Look at Recursion"
date:       2019-08-21 22:02:08 +0000
permalink:  lets_look_at_recursion
---

***Recursion*** -  

A computer programming technique involving the use of a procedure, subroutine, function, or algorithm that calls itself one or more times until a specified condition is met, at which time the rest of each repetition is processed from the last one called to the first.  (Miriam-Webster)


Recursive procedures have 2 main parts:

     1) Base condition - when the condition is satisfied, the recursion loop stops.

     2) Recursive function action - calls the recursive function repeatedly until it hits base condition.


Let’s take a look at the popular factorial algorithm in recursion


```
const factorial = (num) => {
	     if (num === 0) {
           	return 1;          		
			}
  	 return num*(factorial(num-1));    
};                  
```

Short and sweet! It only has 2 main parts - the base condition - which is the if conditional,  and the recursive action -  which is the recursion calling the function again. 

Imagine spending the day inspecting lots of code, your eyes are glazing over, and then you come across this! Wow - it’s clear and succinct! 

This makes the code easier to debug because there are less lines of code to handle. It also seems easier on the eyes. However, there are drawbacks to this structure.

Let's take a look at this same algorithm using a while loop instead of recursion.

```

	const factorial = (num) => {
	     let n = num;
		   if(num ===0 || num ===1) {
			      return 1;
		  }
		  while (n > 1) {
			     num --;
			     n = n*num;
     }
     return n;
};
```

This non recursive structure has a bit more code. Not a lot but,  where there is more code, there is a greater risk of errors. It may not seem like a big deal but it only takes 1 typo or to miss 1 character to have a problem. 

I know! You’re thinking “Heck, this ain’t nothin!  I’ve seen code blocks with 50 lines!”  Exactly my point. Where there are more lines of code, there is more room for bugs.

So, what are the advantages and disadvantages of recursion?

**Advantages**:  Clean quick coding. Easy to debug and generally easier to understand. 

**Disadvantages** - Possibility of stack overflow. Depending on the number of recursive steps, this could be a very inefficient procedure. Recursion uses function stacks - last in first out. A recursive action depends on the completion of the stack on top of it before it can be completed. If you have 4000 initial actions, it will take double that to complete the process.  

For some very complex problems, recursion may be the most clear and effective solution. But if the problem is not complex and the input not so large, perhaps it would be best to stick with a while or for loop to complete the task. 





