---
layout: post
title:      "React-Redux and Displaying Videos"
date:       2020-03-18 00:02:54 -0400
permalink:  react-redux
---


While setting up the plans for my final project, I decided I wanted to display videos.  My project is called "explore."  The idea is to give a place where you can explore different countries and their cultures, specifically their language, food, art, and dance.  I wanted to use videos to display this information.

I looked up an npm packages for react and ran into Video-React.  I quickly skimmed through the information and decided to use it once I arrived at displaying the videos, of course leaving the displaying of the video and its testing until all other parts of the project were completed.

As with any part of a project that you feel will be a "piece of cake", this turned out to be the one error I was unable to figure out.  A completely novel error for me and confused on how to approach it.  I reached out for help and we were eventually able to fix it.

The topics for each country would show  on the Country's show page, expect for the video.  I would receive an error (see below) referring to "SameSite" attribute being set to "none", and that the information I was trying to retrieve had been blocked.  More specifically, my videos were blocked.

![](https://heroku-blog-files.s3.amazonaws.com/posts/1580746311-Screen%20Shot%202019-12-17%20at%204.44.39%20PM.png)



