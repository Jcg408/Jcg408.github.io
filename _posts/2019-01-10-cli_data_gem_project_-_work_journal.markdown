---
layout: post
title:      "CLI Data Gem Project - Work Journal"
date:       2019-01-10 21:32:32 +0000
permalink:  cli_data_gem_project_-_work_journal
---


As promised, the CLI Data Gem Project tested my knowledge and patience. It was the first time in all of the labs and assignments that I was responsible for putting all the pieces together and creating an application that worked. All of  the other assignments mainly focused on 1-2 concepts,  but this project requires a bit of everything that we learned in Ruby.

I decided to keep a journal for this project. I wanted to keep track of progress and obstacles along the way. This was also a cathartic way of thinking through steps and issues. So here is my work journal :


Day 1 - Due to schedule conflicts between study groups (which always seem to happen before they are posted), and my life I have to pretty much work on a lot of this alone. To get started I watched the CLI gem walkthrough video with Avi at least 4 times and used that as a guide for the process. I  studied the previous scraper labs and collaborating labs and of course Google, Google and more Google for a clearer picture of what to do. Scary stuff but I started...

Day 2 -  I used Avi's advice on making a note file with project requirements and wants. It was hard making a decision on what website to use but I wanted to stay simple and choose a site which had the information all on one page. I knew I needed to be able to understand what I was doing with the code instead of being distracted by the subject matter,  and I knew I would need a drink after all this so I decided cocktails would be the way to go! I started by "trying" to put the directory architecture together. 

Day 5 - After navigating through the directory architecture which totally confounded me (Is there a standard way to set up a file directory including what to put in a bin, lib, etc. which works for beginners?). I tried to look at previous files directory structure, other students structure and Avi's structure. In the end I went with Avi's structure because after playing with it for 2 days, I had to make a decision. I then started on building out the class files and mapping out the scraper class to start.... Just finished working on the get_data method in scraper. Was having a heck of a time splitting the text and getting exactly what I need. The html has <p> redundantly throughout the file so isolating a certain <p>was tricky. However after a bit of research, I learned how to use p ~p, and p>p and .children. 

Day 6 - I feel like I made good progress yesterday by getting the menu to work. Today the goal is to get the description and recipe content in the selection method. Happy New Year!

Day 8 - Yesterday I ended up in circles with the description method. As I awoke I realized I need to use separation of concerns in my classes in orrder for this to work. I was trying to access a method from the CLI class when I should probably keep all my data scraping and manipulation in the Scraper class. I'm up bright and early to get going on this!

Day 9 -  I got the application working. Want to add method that gives user choice to stay or exit. I Attended an Open Office for the CLI project and got very good feedback on my code. However, I need to fix the call method which causes the application to scrape more than once. I was also advised to create another class/file to act as an intermediary between the Scraper.rb and the CLI.rb. I will look into those next.

Day 11 -  After 4 different attemps of reworking the project - I had a consultation on the project because I was really frustrated and I was going around in circles. Thankfully, the consultation was a godsend. I had a much clearer vision of what the process was supposed to be and I was able to focus in on what needed to change rather than hodgepodge, willy nilly stabs in the dark. I am now back on track. I see the light at the end of the tunnel.

Day 12 -  Grâce à Dieu! I am finished (for now). I have the code working, I paid attention to separation of concerns - which class does what job, I believe I am only scraping once, and it is not overcoded or redundant. Obviously, this is my perspective. We will have to see what the reviewer tells me. All in all I realize that althought I still had to research and beat my brains quite a bit, I learned more than I thought I did. It was very scary to start a project without the safety net of the instructors and use of Learn tests, but I believe I am more confident in coding.






