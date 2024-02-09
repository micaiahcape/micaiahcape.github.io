---
layout: essay
type: essay
title: "Var str =“ ok eslint, how many errors in this line!?” ; "
# All dates must be YYYY-MM-DD format!
date: 2024-02-08
published: true
labels:
  - JavaScript
---

### My experiences (dreadful)
I was first introduced to the ESlint JavaScript coding standards during my summer internship at the Hawaii Digital Health Lab. The GitHub repository I was committing to was running ESlint checks on every commit, and one day it the commit had that dreaded red X button next to it instead of the green checkmark. Curious to see why this happened, I clicked the commit information and was greeted a page with so much red error text that could make a Java stack trace look like nothing. I realized that nothing in the code actually “broke” functionally (i.e. there were no bugs), so I just left it as is. Looking back on it now, this red error text was all the ESlint errors I was producing as I was coding along.

I was made aware of this when my other coworker pointed out and explained to me the ESlint coding standard. I then took on the painful task of fixing the more than 1000 ESlint errors I created. Most of these were fixable by `eslint –fix` however some of them, such as line length, were extremely annoying. Most of the time, I’d get down to 1 or 2 ESlint errors on each file that could not be fixed no matter what I did. Out of desperation, I’d put the ESlint ignore comments before them in a low effort to mask these errors. As a creative person, these ESlint errors felt suffocating. After typing out a simple function, the IDE would have a seizure and vomit out red underlines all over the place, all in an attempt to convince me I was typing in something illegal like a nuke launch code. 

### Coding standards are important.

I think coding standards are important. It is important for a company with a large codebase with many different users to adhere to a certain standard, to maintain code readability and to some extent, code functionality (let and const, for example). By having standards, code always follows consistent patterns such as:
•	There will always be a space between a conditional’s closing parenthesis and it’s opening brace. 
•	Strings will always be in single quote.
•	Single line arrow functions do not have the “return” keyword.
•	Braces will always be on a new line.
•	Statements in braces, such as inline CSS in React, will always have spaces.

Because of this, it is easy to hunt for certain things in the code by taking advantage of these patterns and the “find” function in the IDE. For example, let’s say coding standards forced me to put strings in singlequote. If I wanted to find the string “test1” in the code for any reason, I am assured that when I type in ‘test1’ into the find function, it is guaranteed to have a hit. If there were no standards and I used both double and single quotes in strings, I would have to type 'test1' or "test1" into the find function to find a possible hit. While this is only a small waste of time, the time can add up after searching for something thousands of times. In summary, coding standards improve code readability, and by forcing the code to follow certain syntaxical patterns, helps debugging and identifying problematic lines of code quickly.

