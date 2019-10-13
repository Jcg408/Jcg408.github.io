---
layout: post
title:      "Practice Makes Perfect"
date:       2019-10-13 23:44:42 +0000
permalink:  practice_makes_perfect
---


Prior to switching careers I was a performing artist. A triple threat performer - singer, dancer, actor. So, I understand all to well the importance of practice. In order to feel comfortable expressing the art you have to let it in your system and know all the moves, lines and notes.

So, how is it I have the hardest time practicing code challenges for interviews. For the life of me, I don't understand why some interviewers want to torture me  with inane, ridiculous, mind blowing problems. But they do and if I am to get a job I have to come to grips with the fact and try to get comfortable working on them. As it stands now, I am comfortable working on understandable short functional algorithms. You want me to reverse a string? No problem. You want me to subdivide an array? Ok, You want a recursive factorial, yes I understand. These functions make sense to me because they actually do things which may be needed and they are explanatory without a dramatic backstory and 20 million constraints.

This is an example of a code challenge that fries my brain. Although, this may seem like fun to some programmers, I detest these type of problems. This is where the practicing begins. I have to try every day to get some progress through a problem. I may not solve it in 1 day but I have to practice - every day.

```
You are given two non-empty arrays A and B consisting of N integers. Arrays A and B represent N voracious fish in a river, ordered downstream along the flow of the river.

The fish are numbered from 0 to N − 1. If P and Q are two fish and P < Q, then fish P is initially upstream of fish Q. Initially, each fish has a unique position.

Fish number P is represented by A[P] and B[P]. Array A contains the sizes of the fish. All its elements are unique. Array B contains the directions of the fish. It contains only 0s and/or 1s, where:

0 represents a fish flowing upstream,
1 represents a fish flowing downstream.
If two fish move in opposite directions and there are no other (living) fish between them, they will eventually meet each other. Then only one fish can stay alive − the larger fish eats the smaller one. More precisely, we say that two fish P and Q meet each other when P < Q, B[P] = 1 and B[Q] = 0, and there are no living fish between them. After they meet:

If A[P] > A[Q] then P eats Q, and P will still be flowing downstream,
If A[Q] > A[P] then Q eats P, and Q will still be flowing upstream.
We assume that all the fish are flowing at the same speed. That is, fish moving in the same direction never meet. The goal is to calculate the number of fish that will stay alive.

For example, consider arrays A and B such that:

  A[0] = 4    B[0] = 0
  A[1] = 3    B[1] = 1
  A[2] = 2    B[2] = 0
  A[3] = 1    B[3] = 0
  A[4] = 5    B[4] = 0
Initially all the fish are alive and all except fish number 1 are moving upstream. Fish number 1 meets fish number 2 and eats it, then it meets fish number 3 and eats it too. Finally, it meets fish number 4 and is eaten by it. The remaining two fish, number 0 and 4, never meet and therefore stay alive.

Write a function:

function solution(A, B);

that, given two non-empty arrays A and B consisting of N integers, returns the number of fish that will stay alive.

For example, given the arrays shown above, the function should return 2, as explained above.

Write an efficient algorithm for the following assumptions:

N is an integer within the range [1..100,000];
each element of array A is an integer within the range [0..1,000,000,000];
each element of array B is an integer that can have one of the following values: 0, 1;
the elements of A are all distinct.
```
Just looking at this makes my brain hurt. I can't get past the first few paragraphs before I am confused.

It seems this is the way that hiring for software engineers is done. Yet, I have met several Senior Programmers and Engineers who have tried some of these tests and they couldn't solve them either. That helps ...... a little.
