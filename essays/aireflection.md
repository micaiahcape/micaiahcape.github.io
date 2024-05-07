---
layout: essay
type: essay
title: "Artificially Intelligent"
# All dates must be YYYY-MM-DD format!
date: 2024-05-07
published: true
labels:
  - AI
---
### I. Introduction

AI is all around us. In fact, it seems impossible to browse the Internet nowadays without coming across articles discussing the implications of AI in our society. Some articles may be research papers sharing a AI based method to predict cancer based on any tumors identified in images. Other articles may take a slightly more dystopian approach, highlighting that AI will replace a lot of jobs (including software engineers) and competitions for such jobs will increase drastically. One can agree or disagree with these articles, but one thing is for sure; AI is here to stay.

Thus, incorporating AI into education is such a crucial thing to do. Students should be trained on how to use AI ethically, as it is a powerful tool when it is used properly. Furthermore, it is likely that once students graduate, they will be working alongside AI as part of their jobs. Some jobs may even place usage of AI as a requirement, just like having familiarity of certain operating systems is a requirement for some jobs. Specifically for software engineering, AI can be used to automate the tedious part of the coding process (e.g. setting up a simple node.js server, write cumbersome code like sorting algorithms, etc…) Therefore, programmers can take advantage of this to accelerate the software development process. Although there are specific AI tools that can help with this, such as ChatGPT or Microsoft Copilot, I personally did not use AI tools in 314.

### II. Personal Experience with AI:
I have used AI in class this semester in the following areas:

1.	Experience WODs e.g. E18

I have not used AI for the experience WODs as I found the screencasts sufficient. When I got stuck, my first instinct was to watch the screencasts and compare the code in the video to my code. When I found what was wrong with my code, I usually understood why that mistake was occurring, and I did not need AI to help me clarify the reasons why.

2.	In-class Practice WODs

I also did not use AI for the in-class practice WOD as I wanted to simulate a real WOD experience. I also wanted to test myself to see how much I knew for the actual WOD. On top of that, the WODs seemed to build on top of each other (e.g. functional programming, Morning Brew, etc…) so I would always have some code that I could reference. This would help me out sufficiently enough so I did not use AI.

3.	In-class WODs	

For the same reasons mentioned above, I did not use AI; However, I did make sure to have AI as a “last resort” tool; meaning if I was on a time crunch and most likely could not finish the WOD, I would resort to using ChatGPT. However, given the very specific instructions in the WODs, I figured that it would not deliver the best answers, and I continued to reference my previous WODs / assignments as mentioned above.

4.	Essays

I was very tempted to use AI for some essays; however I stayed away from that as I wanted some essays to have a personal touch; a personal narrative / experience included in them that AI cannot generate. This would help my essay be unique (which I was trying to strive for) and not just include the cookie-cutter AI generated garble.

5.	Final project

I also did not use AI for the final project, as I had some experience developing in Meteor.js. I also watched most of the screencasts on how Meteor.js works, as well as the specific templates that are provided (react template, and form template). I also found the Digits WODs to be extraordinarily helpful in developing my final application, so it was very rare that I got stuck while developing. When I did get stuck, I figured a few `console.log()` statements would be faster to debug than to paste a giant chunk of code into ChatGPT, explain what other files it interacts with, and wait for an answer. This proved to be correct. 

I did hit two major roadblocks during this final project, but I chose to get help the traditional way – by looking at StackOverflow and reading the Meteor documentation. This was so that I can learn as I “unstuck” myself instead of copy/pasting code from ChatGPT. On top of that, these code fragments were highly specific, so I trusted the documentation from the official sites than what ChatGPT spits out.

6.	Learning a concept / tutorial

No AI used here as well; most of the learning took place through hands-on assignments outside of class. Whether it was developing the Digits application or designing a mockup using Bootstrap, I was constantly learning as I was typing. These assignments were clear enough that I didn’t need AI to help me. When I got stuck, I would check online for answers or documentation, as I’d trust them more than what AI spits out (similar to what was mentioned above).

7.	Answering a question in class or in Discord

No AI used while answering a question either in person or digitally; I tried to rely on my memory and my personal experience with what we were learning. I also didn’t answer many questions on Discord, so this question isn’t as applicable.

8.	Asking or answering a smart-question

As mentioned above, I did not reply to a single smart-question. There was one smart question I asked about committing environment variables in plaintext to GitHub for the final project. I did not ask AI this question, as that was the last thing on my mind. Curious, I just asked ChatGPT this question as I was writing this essay, and this is what it spit out:

Prompt: 
```can you commit environment variables in plaintext to github. If not, how will users access the application when they clone it?```

Output (trimmed): 
``` Provide Documentation: Include clear documentation in your repository's README file or in a separate document explaining how users can set up their environment variables.
Configuration Management: If your application is deployed to a server or a cloud platform, such as Heroku or AWS, you can often set environment variables directly in their respective dashboards or CLI tools.````

This gave me an idea to share the environment variable amongst my team members and not commit it to plaintext to GitHub. In fact, when a team member pulls from the repository, they are responsible for editing the environment variable locally, so the application works during development. Once the site is deployed on digital ocean, we will manually set the environment variables, as ChatGPT suggested.

9.	Coding example e.g. “give an example of using Underscore .pluck”

No AI was used to generate examples. For the JavaScript portions of the course, I simply looked back at FreeCodeCamp assignments, or looked up the documentation on MDN or W3Schools. For the web development portions of the course, I had previous experience in HTML, CSS, and JS (frontend and backend), so I relied on minimal examples (most of which were from my previous personal projects). Again, I trusted code pulled from the official documentation rather than AI generating it.

10.	Explaining code

I was able to explain code by demonstrating what happened locally on my device, so no AI was used to explain. Most of the time, I’d have my final project locally running, so if any team members had a question, I could explain by opening up the site and showing what a certain button / function / dropdown does.

11.	Writing code

Although AI can be used to write code efficiently and quickly, not using AI was my personal preference as I really enjoy the process of writing code. Typing away at my keyboard and seeing all the parentheses, braces and brackets open and close is extremely satisfying. If I used AI to write code, I’d be copy and pasting for the most part, which would take away the enjoyment of typing at the keys and seeing a beautiful UI start being generated. In fact, if I had to use ChatGPT to code the final project, I would not have added the two unique features we had (image uploading, automated email system) as I would have gotten bored of the project.

12.	Documenting code

My code had little to no documentation; the little documentation that I had was in the form of comments on top of functions or for loops. These comments consisted of me just elaborating what my own code does for future reference, and I did not need AI to help me to do that.

13.	Quality assurance 

QA can be split up in two for this class – ESlint and TestCafe. Because Intellij had a builtin ESlint checker, I did not have to use AI to check for source of eslint errors. When a cryptic ESlint error message came out that I couldn’t fix (very rare), I’d simply put an ESlint silencing comment above the error message, which would prevent the IDE from complaining. I did not do much in terms of TestCafe (my other teammates took care of that during the final project), so my use of AI for that was none as well.

14.	Other uses in ICS 314 not listed above

N/A


### III. Impact on Learning and Understanding:

I did not use AI at all during this class except one time when I used it out of curiosity for a smart question. So, AI did not have any effect on my learning or understanding of software engineering principles. However, I can see it being an instrumental tool for other students who may be falling behind. In general, AI may be the way to go when asking a very specific question that can’t really be searched on Google.  (e.g. Why is it in line 53 of this code, there is a callback? What does the callback do?)

### IV. Practical Applications:

There are a lot of practical applications of AI outside ICS 314. For example, there has been a scientific [article](https://doi.org/10.3390/s21030748) that trained a neural network to identify malignant colon cancer cells, benign colon cancer cells, malignant lung cancer cells, or benign lung cancer cells. Testing this model yielded a 96.38% accuracy rate, a number superior to previously done studies. 

### V. Challenges and Opportunities:

Because I did not use AI for any of the coding components during the course, I did not encounter any challenges directly. I think a big part of integrating AI into software engineering education is students being able to trust the code that AI spits out. This was a challenge for me, as I trusted official documentation more than what AI generated. I was scared that I would have to take the extra step to debug what AI generated, if it threw an error. Perhaps warning students about the potential inaccuracies of AI may be a first step into integrating AI into SWE education.

### VI. Comparative Analysis:

Looking at the inevitable, AI would be here to stay with software engineers. Thus, from a career standpoint, AI based approaches to teach software engineering will be much more practical, as some jobs may even require AI to use. However, traditional teaching methods may provide a more comprehensive overview of the software engineering process, and students will develop a more robust understanding of the small details of the language, which may make them more technically capable.

### VII. Future Considerations:

Some areas for improvement for AI may include addressing issues such as digital copyright. For example, as AI gets more advanced in the future, someone may ask a highly specific prompt such as “create a Netflix clone that works exactly like it” or “create an Uber clone” etc… 

### VIII. Conclusion:

AI has its strengths and weaknesses; however it is here to stay. It is important for software engineers to use AI to boost their productivity and to adapt to a changing job market; however SWEs should know the limitations that AI can have and that relying on official documentation from the site may be better when writing code. The same limitations can also apply to students learning about software engineering, as well as instructors using AI to help teach.
