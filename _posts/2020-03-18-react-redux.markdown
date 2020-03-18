---
layout: post
title:      "React-Redux and Displaying Videos"
date:       2020-03-18 00:02:54 -0400
permalink:  react-redux
---


While setting up the plans for my final project, I decided I wanted to display videos.  My project is called "explore."  The idea is to give a place where you can explore different countries and their cultures, specifically their language, food, art, and dance.  I wanted to use videos to display this information.

I looked up an npm packages for react and ran into Video-React.  I quickly skimmed through the information and decided to use it once I arrived at displaying the videos, of course leaving the displaying of the video and its testing until all other parts of the project were completed.

As with any part of a project that you feel will be a "piece of cake", this turned out to be the one error I was unable to figure out.  A completely novel error for me and confused on how to approach it.  I began with making sure I imported the Player component correctly and making sure all information was correct. The issue wasn't displaying information because the topics for each country would show on the country's show page.  

Everything displayed, expect for the video.  I would receive an error (see below) referring to "SameSite" attribute being set to "none", and that the information I was trying to retrieve had been blocked.  More specifically, my videos were blocked.

![](https://heroku-blog-files.s3.amazonaws.com/posts/1580746311-Screen%20Shot%202019-12-17%20at%204.44.39%20PM.png)


After several attempts at Googling for help and not being successful.  I decided to take another approach.  Maybe I could use "iframe" to display the video instead of using Video-React.  Needless to say, I ran into another error while attempting to use this approach: the video still wasn't displaying but now the error stating that x-Frame-Options does not allow cross origin and it needed to be set to 'same origin'.

![](https://canvas.unl.edu/courses/1/files/325464/download?verifier=gbJ3zQI784UzTWveDhfVXpGCIFjeoE9BJQ7JqvBF&wrap=1)

At this point I felt  stuck and reached out for help.  Luckily, my help was intrigued by the issue and was able to get me through it. (Thank you!) We installed another browser to see if we received similar errors, Googled both errors and attempted to fix each error through Video-React and also using iFrame.  We were unable to do so.

What was happening was that when the servers were communicating, it was not liking the cross-server comminication.  We checked the CORS set up and it was correct.  It confused us both on what could fix the situation, until he was able to decipher what was truly going on - the headers were not being set to allow the cross-site communication. 

After testing various solutions found through stackoverflow and other resources, there was one more thing to try before deciding to download the videos... use a different npm package for displaying the video.  And so I installed ReactPlayer and used the documentation to set up video display and *Voila! *It worked.  No more cross-site issues, no more X-Frame-Options error, and a perfectly displayed video and previously planned.




☆ Emilia ☆

