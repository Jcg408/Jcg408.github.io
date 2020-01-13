---
layout: post
title:      "LSP - Liskov Substitution Principle"
date:       2020-01-13 02:16:57 +0000
permalink:  lsp_-_liskov_substitution_principle
---


The Liskov Substitution Principle is one of the five principles known as the SOLID principles. As one of the principles it naturally builds upon and complements the other four principles. This principle is a guide for coding with abstraction and polymorphism.
 
The principle states ***‘If S is a subtype of T, then objects of type T may be replaced with objects of type S (i.e. an object of type T may be substituted with any object of a subtype S) without altering any of the desirable properties of the program (correctness, task performed, etc.).’***
 
I don’t know about you, but when I first read this I imagined a conference room filled with intellectual, stuffy looking people in white lab coats, having a serious debate with algebraic equations on a large chalkboard. What in the world are they saying? After reading through this 3 times word by word I finally got the gist of what it meant…. I think. Let’s see if I can put it a different way:
 
*When a module is a base class (T)  then the objects of the base class can be replaced with objects of the subclass (S) without affecting the functionality of the program.*
 
Let’s say you have a class, Flower, with a subclass, Rose, which inherits from Flower. Wherever you use the Flower class, you should be able to use Rose objects on the Flower class, without any adverse affect to the program.
 
( If Mary’s mother bought a nice new car, and Mary’s car broke down and was in the shop, then Mary can borrow her Mother’s car without her even knowing about it. Shhh … dont tell! )
 
 ```
//Base class parent of Rose
class Flower {
    constructor(name) {
        this.name = name;
    }
    bloom() {
        console.log(this.name + ' is in bloom');
    }
}
 
// subclass Rose inherits from Parent class Flower
class Rose extends Flower {
   thorn() {
       console.log('This rose has thorns')
   }
}
const rosa = new Rose("Rosamundi")
console.log(rosa.bloom()) // object used in Flower class
console.log(rosa.thorn()) // object used in Rose class
 ```
As you can see this principle is an extension of the Open Close Principle which promotes extending the base class to subclasses without changing the behavior.

A benefit is a simplicity of the base class which has no need to know what is happening in the subclasses. The subclasses handle their own machinations and have access to the base class. This promotes code reusability
and  a class  hierarchy which is easier to understand.
 

