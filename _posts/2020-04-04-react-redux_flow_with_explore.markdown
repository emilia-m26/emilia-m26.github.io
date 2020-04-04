---
layout: post
title:      "React-Redux Flow with {explore.}"
date:       2020-04-04 16:36:24 -0400
permalink:  react-redux_flow_with_explore
---


Recently, I completed my final project for the Flatiron School Software Engineering program.  It was created with React-Redux and Rails backend, the project is called {explore.}.  This app was created with the intention of allowing people to learn about different cultures through specific topics such as language, art, dance, and food.  The information is portayed via videos after choosing the specific country you liked to learn more about.  Below is a quick demo video of the app.


<iframe width="560" height="315" src="https://www.youtube.com/embed/kFqCqmA8TYU" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


React can work perfectly fine without Redux.  However, Redux does have some great benefits that immediately appreciated.  In one sentence, Redux is a state management tool.  The state of our application is kept in a store and then any component in our app can access the state that it needs from this store. It also allows for separating logic from presentation, where we have our actions and reducers with Redux and can focus on using React for presentational purposes.

What we are going to focus on with this blog is the flow of data as it works its way through the app.  Specifically, I will be using the CountriesContainer for my app to begin and work our way through the flow from there.  So this journey will begin once we click on "Explore" to see the countries list (resulting in the image below).

![](https://i.ibb.co/7jGGbTs/Screenshot-explore-countries-page.png)

So, what exactly happens when the user click on the "Explore" link? 

