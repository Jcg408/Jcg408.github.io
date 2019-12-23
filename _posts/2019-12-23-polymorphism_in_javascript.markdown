---
layout: post
title:      "Polymorphism in JavaScript"
date:       2019-12-23 11:57:17 -0500
permalink:  polymorphism_in_javascript
---



Polymorphism - From the greek poly - “multi, many” and morpho - “shape, form”. 

The term is used in biology and zoology to designate different gene traits within a given species. To be classified as such, morphs must occupy the same habitat at the same time. 

Why did I choose polymorphism for the topic of this blog? Well, it’s the holiday season and I am looking at different shades of Poinsettias. Although it is most common to see red plants, there are variations such as white, pink and even red and white variegated. They are all the same plant but have genetic traits that differ. 

This brings me to polymorphism in object oriented programming. It is not exactly the same but the concept has been adapted to mean the ability to create an object that has more than one form or as MDN puts it: `the ability of multiple object types to implement the same functionality`. Let’s look at this a little bit more using JavaScript. 

JavaScript, as you know, is not a typical object oriented language. Classical object-oriented languages have interfaces,  JavaScript uses subclasses which are created by inheritance. By using constructor functions we are able to create ‘classes’ and have ‘subclasses’ inherit methods and properties from the parent class.

In the following, there is a class Garden which sets a name variable and a plant method which is available to instances of the class. Hosta and fern both have access to the plant method. 

`class Garden{
    constructor(name){
	this.name=name;
    }
    plant(){
    	console.log(this.name + ‘ is a plant.’)
    }
}
let hosta = new Plant(‘Hosta’);
let fern = new Plant(‘Fern’);
hosta.plant();
fern.plant();
`
Now lets add another class which inherits from the Garden class. This will make the Garden class the parent and the subclass will have access to methods and properties of the parent. 

`class Garden{
    constructor(name){
	this.name=name;
    }
    plant(){
    	console.log(this.name + ‘ is a plant.’)
    }
}
let hosta = new Plant(‘Hosta’);
let fern = new Plant(‘Fern’);

hosta.plant();	//Hosta is a plant.
fern.plant();	//Fern is a plant.

class Flower extends Garden{
	plant(){
	    console.log(this.name + ‘ is a flower and a plant.);
}
let gardenia = new Flower(‘Gardenia’);
let rose = new Flower(‘Rose’);

gardenia.plant(); 	// Gardenia is a flower and a plant.
rose.plant();       	// Rose is a flower and a plant
hosta.plant();     	// Hosta is a plant.
fern.plant();		// Fern is a plant.
`
Notice how the plant method for Flower overrides the plant method for Garden. However, if we were to comment out the plant method in Flower, inheritance will move to the parent class.

`class Flower extends Garden{
	//plant(){
	//    console.log(this.name + ‘ is a flower and a plant.’)
//}
}
let gardenia = new Flower(‘Gardenia’);
let rose = new Flower(‘Rose’);

gardenia.plant();	//Gardenia is a plant.
rose.plant();		//Rose is a plant.
hosta.plant();		//Hosta is a plant.
fern.plant();		//Fern is a plant.
`
 We can also return both methods by adding a call to the parent method in the child method.

`class Flower extends Garden{
	plant() {
    super.plant();	   
    console.log(this.name + ‘ is a flower and a plant.’);
           }

let gardenia = new Flower(‘Gardenia’);
let rose = new Flower(‘Rose’);

gardenia.plant();	//Gardenia is a plant.
			//Gardenia is a flower and a plant.
rose.plant();		//Rose is a plant.
			//Rose is a flower and a plant.
`
These are good examples of JavaScript inheritance and polymorphism. The properties and methods of the subclass may be shape the objects in a different way but the objects are still children of the parent class. Just like people are the same but with different traits and characteristics, objects may behave differently and exhibit different characteristics, but they are still belong to the same superclass.

