---
layout: post
title:      "Ruby: Benefit of Modules"
date:       2019-12-15 21:48:29 -0500
permalink:  ruby_benefit_of_modules
---

 
Although modules may seem similar to classes, there are very distinct differences. Classes may instantiate objects. Modules can't instantiate objects. Whereas classes can create and instantiate objects,  Modules are concerned with behavior and characteristics of objects. 

Modules are a way of grouping together methods, classes, and constants. Modules give you two major benefits:
1.     Modules provide a namespace and prevent name clashes.
2.     Modules implement the mixin facility.

A namespace is a container which bundles logically related objects together. Because the namespace is encapsulated, modules allow classes with the same names to co-exist. 

Mixin functionality allows sharing common methods across multiple classes or modules. A mixin is basically just a module that is included in a class. When you use a module in a class, the class will have access to the methods of the module.

Mixins are great to  share functionality between classes. Instead of repeating the same code in different classes, you can place the code in a module and then include it into each class that requires it.

Using modules also promotes good design principles. The reusability of code prevents the repetition of code throughout classes and  bundling related code in a common place handles separation of concerns, single responsibility and encapsulation. This helps to keep the classes more concise and clean.





