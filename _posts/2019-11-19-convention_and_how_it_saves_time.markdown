---
layout: post
title:      "Convention and How It Saves Time"
date:       2019-11-19 22:46:57 +0000
permalink:  convention_and_how_it_saves_time
---


![](https://static.javatpoint.com/tutorial/software-engineering/images/software-engineering-coding2.png)

We have heard it time and again... Conventions, Guidelines, and Coding Best Practices.  There are different reasons to follow conventions in programming.  

Some of the reasons being the following: 
* Uniform appearance even if written by different engineers
* Reduces complexity and  allows for easier error detection
* Increases efficiency of programmers
* Improves readability and maintainability

Some of the conventions we have learned about are:
* Indentation
* Use of inline comments
* Limited use of globals
* Naming for local and global variables to be meaningful and understandable
* Format of naming for files (controllers, models, views, etc.)

Specifically, I'd like to focus on one specific convention as I work on my Rails Portfolio Project: naming conventions for the User models. My project is to track travel goals for a user.  I decided to name my User model as Traveler, as it made more sense to me in that manner.  It doesn't necessarily stray completely off the beaten path of naming conventions so it does not seem to be a big deal.  There are a few things I learned when looking for assistance or for gems to use for my project. 

One thing that is immediately apparent is lmost all blogs, Stack Overflow responses, and any other Googled information will usually be written for the User model.  This makes sense as the User model tends to be universal. This is not a very difficult situation as, for the most part, you could replace Traveler for User and you could still manage to use the information found.

Another situation I ran into was most gems are built on the User model.  All of the documentation is based on this naming convention assumption.  Again, this is a small detail but it does eventually cause some confusion.  For example,  I used the Devise gem for the authentication of my Rails project.  When using their built-in methods, there were times where I typed what I read from the How-To's.  Meaning, I typed in *current_user*  or *user_signed_in? *  This may not seem like a big deal, but when you have several files to go through it becomes a bit of a drag to find the methods to change the names over to *current_traveler* or *traveler_signed_in?*.

You also have to be extremely cautious when using tutorials or follow-along instructions for any assistance.  I was using a tutorial to complete my authentication requirement through a third-party provider.  I chose to user OmniAuth GitHub.  I reached out to a classmate to see if we could pair as I was stuck on completing my OmniAuth requirement and I could not understand why, as I followed the tutorial step-by-step.  I kept getting an error I'd never seen and all the Googling I did could not find the error for me.  I'd tried absolutely everything on my own. 

While pairing with my classmate, he was unable to find anything that triggered a reason to believe I had completed the setup incorrectly.  I had not commited it to Github yet, so I discarded the changes and began again.  This time my classmate stayed on with me and we went step-by-step (as I have a terrible habit of missing commas and he makes sure I don't do that -- Haha!).  We completed the instructions a second time and ran the Rails server.  To our disappointment, I ran into the same strange error.  Again, we checked file names, routes, and everything we could possibly think of that would create an error with that specific path.  We talked it out for about 2 hours, before it hit me... When you use OmniAuth, you are given a unique Client ID and Client Secret to set in the Devise gem for your specific app.  In that form, before receiving the needed ID and Secret, you have to set an Authorization Callback URL.  An Authorization Callback URL I copied directly from the tutorial that I was following and could not possibly be incorrect as it worked for my classmate and everyone else that used it.

...Except that my classmate's User model was named User and mine... well, mine was Traveler.

Conventions definitely save time and effort!

☆ Emilia ☆
