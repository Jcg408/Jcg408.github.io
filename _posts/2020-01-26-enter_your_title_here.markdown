---
layout: post
title:      "Dependency Injection "
date:       2020-01-26 20:10:14 -0500
permalink:  enter_your_title_here
---


**Scenario**: You are hungry, and you are craving Italian food. You yearn for a fresh Caesar salad, Lasagna al forno, a glass or two of Montepulciano, and the finale - Tiramisu or cheesecake for dessert. Yum! You decide to go to your favorite Italian restaurant. When you arrive, you decide to:

A)  Walk into the kitchen, go into the pantry, get the ingredients for each part of the meal and make the meal
      yourself, take the meal to the restaurant table, go to the bar and get a bottle of wine and pour yourself a glass,
			take it back to the table, sit down and eat your  meal, go back into the kitchen with the dirty dishes and set
			them aside, get your dessert and take it back to the dining table to eat dessert. Take dirty dessert dishes back
			to the kitchen, come back to your table and tell the server that you have finished your meal and you are ready
			to pay your check.

OR -

B) Sit at the table, allow a server to bring a menu with a selection for you to order. You place the order with the
      server, after a period of time your delicious meal with wine is delivered to you at the table. Empty dishes are
			removed by the server or waitstaff and dessert is brought to you. The server presents you with a check and 
			you pay the check. No fuss, no mess.
			
As much as I love to cook, I prefer the second option. Eating out should be convenient, expedient, indulgent and tasty - a special treat. If I wanted to cook, I would stay home and cook. Besides, there are people out there who are fabulous cooks and professional servers. Why should I deny them the pleasure and the paycheck.
I know - you’re hungry now. Sorry, just trying to make an analogy for dependency injection.
 
**Dependency Injection** is the concept of one object supplying dependencies to another object. It is a software design pattern used for achieving loose coupling between objects and their dependencies. If a class needs a dependency it receives the dependency from an outside source rather than creating the dependency itself. This is one of the major principles of clean code in object oriented programming. The purpose of Dependency Injection is to achieve Separation of Concerns in the construction and use of objects. 
The Dependency Injection pattern involves 3 types of classes.

* Client Class: The client class (dependent class) is a class which depends on the service class
* Service Class: The service class (dependency) is a class that provides service to the client class.
* Injector Class: The injector class injects the service class object into the client class.
* 
The following figure illustrates the relationship between these classes:
![Imgur](https://i.imgur.com/trstOZ2.jpg)

The client is not responsible for creating the objects it needs. It has access to the resources that have the dependencies and gets them on request. The class is now free to do what it needs to do.
 
What are the benefits of Dependency injection

* Because dependency Injection doesn’t require any change in code behaviour, it can be applied to legacy code
   for refactoring. This results in a more independent client class which is easier to unit test in isolation. 
	 
* Reducing a components dependencies typically makes it easier to reuse in a different context. Since 
  dependencies are injected, they can be configured externally. This increases the reusability of that component.
	
*  It is  easier to see what dependencies a component has, making the code more readable because you don’t have to look through all the code to see what dependencies you need for a component. They are all visible in the interface.
 
Let’s go back to the restaurant a moment. You decided that you really want to try and make your own meal. You realize very quickly that you are not in your kitchen, and this environment is not as user friendly as you anticipated. You can’t find the lasagna pan, the freezer  is locked and you don’t know where the key is, you cut your finger chopping the garlic, the stove has 10 burners and you had something on the back burner. You reached over the front burner and set your sleeve on fire!. This is a disaster! All because you choose to do something that you didn't need to handle. Now, you have no appetite and you ruined your meal. Guess what! You still have to pay for it!

Dependency Injection to the rescue!! (superhero in a cape image.) Let’s use other classes that can help out by taking the responsibility of creating and serving dependencies, Let’s keep the kitchen (code) clean and safe from accidents. Support the service industry, enjoy being a client and let the professionals do their job.
 
 

