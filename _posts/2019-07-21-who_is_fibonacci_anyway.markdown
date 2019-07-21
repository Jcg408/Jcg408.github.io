---
layout: post
title:      "Who is Fibonacci anyway? "
date:       2019-07-21 17:03:16 -0400
permalink:  who_is_fibonacci_anyway
---

The Fibonacci sequence is one of the most popular and most debated computer algorithms. It is also one of the most used in the software engineering coding interview. Why is this? When are we really going to use this algorithm, especially since it has been solved many ways and in many different programming languages?

I did not have the chance to take computer science courses in college. I was a performing arts major and didn't come to this illustrious field of software engineering until much later in my life. Waaaayyy  later! So, when I completed the Flatiron Software Engineering Course and started prepping for job search, I was presented with some of the standard CS questions which really stumped me. The Fibonacci sequence being one of them. 

Did you know that Leonardo Bonacci,the mathematician, popularized the Hindu-Arabic numeral system in the middle ages? He wrote a book, Liber Abaci, that became quite popular and showed the conversion of Roman numbers to the Hindu-arabic numeral system.

Did you know that in the same book he tackled and solved a mathematical problem of  populating rabbits (yes, I said rabbits!) which led him to the Fibonacci sequence? I assume there was a population explosion which caught his attention.

Although he introduced it to the west, the number sequence was already known by Indian mathematicians centuries earlier.

In the sequence each number is the sum of the number and the number prior. So if the sequence starts at 0, it would go as follows:

             0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55 .... and so on.

So, if you need to find the Nth element in the sequence we could use a simple for loop like this: 

        const fb = (element) => {
				    let start = 0, next = 1, sum = 1;
						
						for (let i= 2; i <= element; i++) {
						    sum = start + next;
								start = next;
								next = sum;
					 }
					 return sum;
			};

 fb(9);  
 
 The 9th element in the Fibonacci sequence is 34. The first loop returns 1 andthe function re-loops until it reaches element count.

Now, I don't have a background in CS but I found this helpful in understanding how the algorithm could be useful in
programming. We can forecast the number of rabbits in an epic rabbit population explosion! Just kidding! I'm sure it has something to do with recursive patterns.
						 
