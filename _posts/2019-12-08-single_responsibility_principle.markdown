---
layout: post
title:      "Single Responsibility Principle"
date:       2019-12-08 16:11:10 +0000
permalink:  single_responsibility_principle
---

The world can be a cluttered, confusing space. The brain responds to chaos by trying to keep up with it. We don’t want to miss anything so we grab everything, even’t if we don’t need or want it. Because our minds are constantly processing new information and we feel the need to act on it right away,  people often try to accomplish too many things at the same time. Note - the word ‘trying’ because it is not easy to handle more than one thing at a time without something suffering.

This can lead to some fatal life errors. How many times have you heard stories of accidents that could have been avoided if only that person were taking care of one thing at a time? People falling into open manholes or getting hit by buses because they walk and text on the phone. Driving cars into houses or over bridges while putting on makeup (Really?! - get a grip, girlfriend!). Why can’t we do one thing and then proceed to the next? These are some extreme cases, and generally there are some simple tasks which can be handled with split focus, but it is best to work on one thing at a time. Unless you are a circus clown unicyclist juggler. 

So, where am I leading to with these thoughts? Imagine looking at someone’s code and you don’t know what it was built for. You try tracing where the functions or methods lead and it has no rhyme or reason. It’s a wonder it would work at all because it seems to be all over the place with too many responsibilities.

It kind of reminds me of the junk drawer I have in the dining room. You know -  that drawer where you put all the things you really don’t know what to do with. Eventually the drawer has a hodgepodge of items that don’t relate to each other. Then, when you are searching for something, and you stick your hand in the drawer, you cut your finger on something else that has no business being in that drawer. I know - I am digressing.

Single Responsibility Principle

The first letter of the SOLID acronym for design principles stands for Single Responsibility Principle. These principles are meant to make software development more flexible, understandable and maintainable. The principles are a subset of many principles promoted by software engineer Robert Martin.

`The single responsibility principle is a computer programming principle that states that every module, class, or function should have responsibility over a single part of the functionality provided by the software, and that responsibility should be entirely encapsulated by the class, module or function. All its services should be narrowly aligned with that responsibility. `

In other words - Do one thing and do it well! If the purpose of the function or method is to make cupcakes, then that should be the single responsibility of the function/method. Not people who eat cupcakes; not stores that sell cupcakes. You may then encapsulate that functionality with other functions/methods that apply to it in a class, module or function. 

The benefits of following this principle are evident. Suppose you want to know which stores are selling the cupcakes. If it’s a tangled mess of code, you may be searching through how cupcakes are made to find where the stores are. That doesn’t make any sense!  How does a cupcake know what store is selling it? Wouldn’t you prefer to have a dedicated place for stores that sell cupcakes?


Where there is muddy code, figuring out what parts can be reused is nearly impossible. Following the threads can be a nightmare. This leads to code duplication and the destruction of DRY coding principle. I, for one, don’t like to repeat myself. Could you imagine a novel that is so convoluted that it has to repeat the plots and reintroduce the characters throughout the story? How long and confusing would that book be? Who would buy that book?

There is a saying I often need to remember : “Chop the woodpile in front of you.” Don’t get distracted by the other peripheral things around you. If you have a job or task in front of you at that moment, that should be your concern. This may not be easy in everyday life because there are so many distractions and enticements. However, it is totally doable and preferable with code.

