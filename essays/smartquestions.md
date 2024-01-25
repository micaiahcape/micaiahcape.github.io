---
layout: essay
type: essay
title: "Infuriating Dumb Questions"
# All dates must be YYYY-MM-DD format!
date: 2024-01-25
published: true
labels:
  - SWE
---

## My personal experiences

As a student office assistant, one of the most annoying things that I come across are “bad emails”. Most emails I read as part of my job are “nonlazy” (e.g. people asking when they can come over to pick up packages, or graduate school applicants clarifying a specific requirement on their application). These “nonlazy emails” have something in common – they are very specific, direct, and is obvious that they have tried to obtain information about the inquiry beforehand. I’m not trying to imply you should email someone only when there is a specific problem, but the sheer number of “lazy” emails I’ve received made me realize that there is a line between “smart questions” in nonlazy emails, and “non smart questions” in lazy emails. For example, many of the “non smart” I received are as follows:
 
> Hi, I am interested to applying to your program. Can you send me the relevant information?

> Hi, my name is (name) and I’m applying to (program). I would like to study at your institution only if you can give me full scholarship.

> Hi, I am transferring to your program via (fellowship). I want to know what kind of degrees you offer and the admission requirements (including materials). Can we set up a zoom call?

In comparison, here is a “smart” question. This is like a breath of fresh air.

> My name is (name) and I’m interested in studying (degree name) at UH Manoa. Regarding (application requirement), I have followed the instructions on your website, filling out the relevant fields. However, when I get to this field, the course I took does not show up. I’ve checked the website, and it says nothing about courses that don’t show up. A screenshot is below. Please let me know what I should do in this case.
(screenshot)

## The application to software engineering

In software engineering, the distinction between “smart” questions and “not smart” questions is equally as important. “Smart” questions are direct and can catch someone’s attention. By being direct and specific, the question can be answered much more quickly, as all the information is already presented. A brief response that is specific to the problem will do, and there is almost no need for “probing” the inquirer for specific details. 

Unfortunately, “not smart” questions can take a very long time to resolve, if one decides to even answer at all. For example, a question like “I ran Meteor. It’s giving me an error saying ‘semver is not a constructor’. What should I do?” would require one to extract more information from the inquirer, such as “What machine are you on?”, “What is the command you used to run?” or “what version of Meteor are you using?” Alternatively, one may painstakingly write a very long answer covering all possibilities, possibly going out of their way to look up all different causes of the error message, and summarizing it for them (if the inquirer is lucky). Either way, asking follow up questions or writing out lengthy answers can be very time-consuming, and from the point of view of a software developer, is a waste of time.

The problem is exacerbated when people ask “not smart” questions when the exact question can be found on Google, or on the software’s documentation. Going back to the three “not smart questions” examples I gave earlier, all three questions can be answered with a quick search to Google or our website. Asking these “not smart” questions comes off as lazy, hasty, and reluctant to go out of their way to try to find a solution. Psychologically, when we have to answer these kinds of questions, we may feel tempted to reply back in the same exact manner – lazily and hastily. In the previous paragraph, I mentioned that if the inquirer is lucky enough that their question is read by someone patient, they may get a proper response (at the expense at the answerer’s time). However, most people, especially in a software development environment, when tight deadlines are everywhere and work is fast-paced, the last thing they want to do is to write a long response to a hastily asked question. Thus, they may not reply back at all, or they would reply back with a hastily worded answer:  “go look it up at (this source)” or “All information is at (source).” In summary, “not smart” hastily worded questions are both a waste of time and energy from the developers’ and inquirer’s perspective, and much more time and energy can be saved on both sides when the question is specific enough, so it is “answerable” without it being too vague. On the other hand, if only “smart” questions are asked, this can greatly improve the response quality. This is especially important in a software engineering environment, where questions about the software are being asked daily, either from customers, developers, or other clients. 

## The phenomenon on Stack Overflow

An example of this phenomenon can be found on StackOverflow. There was a “bad question” found here that got two downvotes (link [here](https://stackoverflow.com/questions/62046304/i-am-trying-to-move-my-character-but-instead-of-that-the-player-wont-move); note that question is edited now). The original unedited question was requesting error-free code to simulate a movement of a character in Pygame, however it was being very vague. Without copying the question verbatim, the user mentioned that they were following a tutorial (without providing a link), and said that “it didn’t work and trying to fix it broke other things” without specifying what didn’t work, what steps they took to fix it, and what other things broke. The question goes on to say “I don’t know what the errors mean” and didn’t even list any errors to begin with. This inquirer was lucky to have an elaborate answer directly in response to their question; and they were lucky not to be torched when the question was linked to a [related topic](https://meta.stackoverflow.com/questions/400643/what-should-i-do-if-i-am-post-banned-but-i-can-not-modify-any-of-my-bad-question). There were even a followup questions in response to this original question, such as “What kinds of errors are you seeing?” or “what broke?”.

There are “smart questions” as well on StackOverflow. One [question](https://stackoverflow.com/questions/8318911/why-does-html-think-chucknorris-is-a-color) asked why “chucknorris” is interpreted as a color in HTML. This is a short question, but it is a “smart question” as it is very direct, simple, and comes with code snippets demonstrating the phenomenon. The answer that they got ended up being very detailed yet concise, with them elaborating that all nonvalid hexadecimal characters are turned into 0s, and HTML splits the resulting string into thirds to correspond to the red, green, and yellow values of the color. After additional processing of the three strings, HTML interprets “chucknorris” as RGB (c0, 00, 00), producing the color red.


