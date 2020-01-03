---
layout: post
title:      "Debugging with Lucky"
date:       2020-01-03 15:11:07 +0000
permalink:  debugging_with_lucky
---


> It is a painful thing to look at your own trouble and know that you yourself, and no one else, has made it. 
> ~ Sophocles


When we first embark on the Flatiron Journey, one of the biggest things to get used to is the red letters.  I don't know about you guys but whenever I had failing tests, and saw the dreaded red letters, I panicked.  After getting through the first module and having what I felt was an intense project review, I decided to take the reviewer's advice on finding the ways that work best for me to solve issues.  We all know by now that reading the error messages help us a lot and reading the specs file will give us hints of what the tests expect from us.  However, when you run into errors while creating your projects from scratch, there is a bit more than reading specs that is involved.

One consistent piece of advice that was given from the reviewer, my cohort lead, and my research on Google was: explain the code to someone else.  Personally, that helped when I paired with classmates but what if no one was available? Who would want to listen to me babbling about my code?  I was reading The Pragmatic Programmer around the same time and looked into the debugging topic.  I learned about Rubber Duck debugging.  At first I found it a bit silly, to be honest.  Talking to a rubber duck!?!? How could that possibly help me? But I figured, let's give it a go and see what happens.

I'd like to introduce you to Lucky, the Bugbuster.

![](https://i.ebayimg.com/images/g/TZMAAOSwiMFbZOEl/s-l300.jpg)

Lucky has become an integral part of the debugging process for me.  He listens patiently, smiles through the toughest moments, and somehow always has an answer for me. Speaking to Lucky about my coding dilemmas allows me to pull away from my frustrations and take a moment to really think things through.

A few steps I follow while debugging with Lucky are:
1. Don't Panic! It is a normal cycle when creating for things to work, then to break, and then we have to debug. We need to practice turning off the defenses we use when things "go wrong".  As stated in The Pragmatic Programmer - "Embrace the fact that debugging is just problem solving, and attack it as such". (And if you are slightly panicked then vent to your rubber duck buddy, you will feel much better).
2. Read the Error Message! - Don't only read over it quickly and assume you know what it is. Really read it and understand where the error is.
2. What is the problem I am having? - Try to detail what the issue is.  Don't get stuck in "it just doesn't work". Go futher into detail by asking the right questions.
3. What am I expecting my code to do?
4. What is my code actually doing? Once I know what my expectations are and what the reality is, I can compare both and go to the next question.
5. What is responsible for that functionality? (model? view? controller?)
6. Don't assume anything! The worst thing we can do is read over a line of code and assume it is doing what we want it to do.  Maybe the line of code on its own works well, but in interaction with other code it may be misfiring.  Don't assume it works, prove it works. And in the case that the code is misfiring because of its interaction with other functionalities, then you have saved yourself alot of trouble.



So... If you haven't tried it yet, get your self a rubber duck buddy and see how great it is!  You won't regret it. 


☆ Emilia ☆
