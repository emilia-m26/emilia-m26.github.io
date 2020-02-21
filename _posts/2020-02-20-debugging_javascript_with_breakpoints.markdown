---
layout: post
title:      "Debugging Javascript with Breakpoints"
date:       2020-02-20 22:13:01 -0500
permalink:  debugging_javascript_with_breakpoints
---


![](https://i.ibb.co/sJRWbh0/Screen-Shot-2020-02-20-at-9-02-19-PM.png)


Debugging has never been so enjoyable, until I learned about breakpoints.  During one of our lectures on the Rails/Javascript module, our instructor (Nancy, which by the way is absolutely awesome!), showed a little tidbit that I had no idea I'd enjoy so much: debugging with breakpoints.

To access this magical tool, you would want to get into your Chrome Dev Tools (on Mac the shortcut would be cmd+opt+J which would open your console).  Once the console opens you can select different tabs.  To use breakpoints you would select the Source tab.  You would then click on your index.js file (or whichever .js file it is that you want to debug in).  Your view would like the screen above.  The green arrows are where I selected to break (or pause).  For debugging, this tool is amazing!

When you select the area you want to debug and position the breakpoints with the arrows, you can then select whatever action you are testing.  In my example, I was looking into my displayDeck function.  This function was built to display the cards within a given deck.  I clicked on the link for one of the decks and what you would see is similar to the screenshot below.  At the top of the screen you would see a "Paused in Debugger" with choices to step-into or step-over.  

* Step-into: The code inside the onClick() function will be executed line by line as you click on the button - so with each click you step-into another line of code.

* Step-over: The code inside the onClick() function is skipped and the execution stops since there are no more lines of code once the function is finished.

![](https://i.ibb.co/rbyxQxv/Screen-Shot-2020-02-20-at-9-00-58-PM.png)

When we set certain lines with the arrows, or the breakpoints, this is called a 'line-of-code breakpoint.'

This is easily done by clicking on the numbers on the side. The color of that number changes and this indicates that the breakpoint is set.

What I enjoyed the most with debugging using the brakpoints is that we can easily indentiy what is stored in the variables at that specific moment.  Reviewing the first screenshot as an example, you can see that on line 95, id is showing as 3.  While in this example it seems very simple, it really can save you tons of time.  I used this magical tool to debug JS when I i was unsure of where a function failed to do what I assumed it would.  I was able to pinpoint rather quickly where the data was not persisting and then go into my code to fix the issue.

Debugging in Javascript with brakpoints truly is a lifesaver and it would benefit you to become used to this tool provided by the Chrome Dev Tools.


☆ Emilia ☆


