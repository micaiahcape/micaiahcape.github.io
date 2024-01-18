---
layout: essay
type: essay
title: "var essayTitle = 'Still Thinking...';"
# All dates must be YYYY-MM-DD format!
date: 2024-01-17
published: true
labels:
  - JavaScript
---

<img width="200px" class="rounded float-start pe-4" src="[../img/difficulty/degree_difficulty.jpg](https://s3-ap-southeast-1.amazonaws.com/kipalog.com/B4UaJfMCQAE67QB.png_mnu9u7omer)">

*JavaScript: A Summary*

## The 113 exercises

I have known some JavaScript prior to starting this course; enough to add some interactivity to websites. Thus, most of the basic JavaScript taught through FreeCodeCamp (the 113 coding exercises) was pretty simple, and I knew most of it. Towards the end of the 113 exercises, I was able to learn about the `switch` operator and ternary operators, which were operations I knew existed, but I don’t use them frequently. Thus, this assignment was a good refresher on how to use them, and I will try to use them more often. I did a little bit of reading and found out that switch statements can be slightly faster than an if-else chain, and it is more readable.

## The ES6 module

In contrast to the Basic JavaScript module, I ended up learning a lot on the ES6 module. Before starting this assignment, I was personally a bit iffy on a lot of the topics presented in that section (e.g. object restructuring, imports, promises, etc…) I used some of these topics in my projects, however much of these were copied from other websites such as StackOverflow. Thus, I’d use them without having a very good understanding of how they worked. For example, I did not know it was possible to extract properties out of a JavaScript object and assign them to different variables without using dot nor bracket notation. I did an internship at the Hawaii Digital Health Lab last summer as a web developer, and this made me realize that a good fraction of their codebase consisted of ES6 syntax. Another concept I got a good refresher on is `Promises`. I’ve indirectly been exposed to `Promises` when using the `fetch` API or querying in MongoDB, but I did not know what exactly was taking place (e.g. resolving, rejecting, callback functions). Therefore, the ES6 module was very helpful for me, and I hope I can write cleaner, more concise code.

## My opinions on JavaScript
```
console.log("Types!? what is that??");
```
Because JavaScript was the first programming language I learned, I’ve felt that more strictly typed languages like Java or C++ were a pain to work with due to having to specify types. However, after taking 211 and 212, I feel like explicitly declaring types is important; from a software engineering perspective, it may be difficult for another coder to tell what type a certain variable is if it’s type is not declared. Not to mention that personally, I run typeOf on a JavaScript variable more often than I want to, because I often get confused if a variable is a string or number (which can quickly get messy when dealing with concatenations, additions, or subtractions.) Good documentation within the code can help; however this can be limited if a same variable is getting re-assigned to a different type (which requires a comment on every line that does so). Thus, I think from a software engineering perspective that it is better to specify types. On the flip side, the freedom to pass anything (`chars`, `strings`, `ints`, `objects`, `arrays`, nested arrays, etc…) as a parameter without having to set anything up (e.g. in Java, you need to set up a fixed array size) is extremely convenient and is something that JavaScript has that makes me love the language.
