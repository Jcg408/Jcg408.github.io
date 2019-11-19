---
layout: post
title:      "Interview Code Questions"
date:       2019-11-19 05:10:25 +0000
permalink:  interview_code_questions
---


Since I have been spending much of my time preparing for tech interviews, I thought it might be good to share some
of the more common algorithms and code questions that I have been asked. I actually created a library on Github with some of these which is also open for contributions. My language of choice is JavaScript but these may be used in any language.

For this session, I will focus on 5 of the more common string algorithms.

1.  String Reverse - Given a string, reverse the characters. I
 
 Convert the string to an array, then reverse the array, then join it back together as a string. This is an example of chaining methods in JavaScript. 

`const rev = (str) => {
  return str.split(' ').reverse().join(' ')
}`

It may be requested that you dont use built in methods. Here is one way to do it. 

`const rev = (str) => {
    if (str.length) {
		let newStr = ' '
		for(let char of str) {
		  newStr = char + newStr
			}
		}
		return newStr
	}`
	
	2. String Repeat - Given a string and a number, return the string repeated the  specified number of times.
	
	`const repeat = (str, num) => {
	   return str.repeat(num)
		 }
	`

Here is a way without using the built in repeat method
`
const strRepeat = (str, num) => {
    let newStr = '';
    for (let i = 1; i <= num; i++) {
        newStr = newStr + str
    }
    return newStr;
}`

3. Starts With Uppercase - Given a string, check to see if the first letter is uppercase.

`const startsWith = (str) => {
    if (str.charAt(0) === str.charAt(0).toUpperCase()) {
        return true
    } else {
        return false
    }
}`

4. Palindrome -  Given a string, check to see if a it is the same forward as backward. 

`const palindrome = (str) => {
    let string = str.toLowerCase().replace(/[\W\_]/g, "");
    let newString = string.split('').reverse().join('');

    string === newString ? console.log('Palindrome') : console.log('Not a palindrome')
}`

5. String Ending - Given a string and target , check to see if string ending same as target.

`const strEnd = (str, target) => {
    if (str.substr(-target.length) === target) {
        return true;
    }
    return false;
}`

There are many more algorithms but this is a good start on what to expect for string questions.
I will continue to share some of these problems in future blogs and include other data structures.

