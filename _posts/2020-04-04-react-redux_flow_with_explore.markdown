---
layout: post
title:      "React-Redux Flow with {explore.}"
date:       2020-04-04 16:36:24 -0400
permalink:  react-redux_flow_with_explore
---


Recently, I completed my final project for the Flatiron School Software Engineering program.  It was created with React-Redux and Rails backend, the project is called {explore.}.  This app was created with the intention of allowing people to learn about different cultures through specific topics such as language, art, dance, and food.  The information is portayed via videos after choosing the specific country you'd like to learn more about.  Below is a quick demo video of the app.


<iframe width="560" height="315" src="https://www.youtube.com/embed/kFqCqmA8TYU" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


React can work perfectly fine without Redux.  However, Redux does have some great benefits that can be immediately appreciated.  Redux is a state management tool.  The state of our application is kept in a store and then any component in our app can access the state that it needs from this store. It also allows for separating logic from presentation, where we have our actions and reducers with Redux and can focus on using React for presentational purposes.

What we are going to focus on with this blog is the flow of data as it works its way through the app.  Specifically, I will be using the CountriesContainer component of my app to begin, and work my way through the flow from there.  This journey will begin once the user clicks on "Explore" to see the countries list (resulting in the image below).

![](https://i.ibb.co/7jGGbTs/Screenshot-explore-countries-page.png)


When the user interacts with our app, they are triggering the flow of data. They are interacting with the CountriesContainer component (below).  

One of the first things that happens when our React app mounts, in essence also mounting this specific CountriesContainer component, is to connect to the store.  We see this happening in line 40 of this component.  In this method, connect( ) we are connecting the CountriesContainer component to the Redux store.  


![](https://i.ibb.co/W0XTKNx/Countries-Container-component.png)


The next method called in this component is componentDidMount( ). This method signals that the component and its children components have mounted properly and are available for use.  This specific method is perfect for fetch( ) calls.  The componentDidMount method is calling our action creator through this.props.fetchCountries( ) on line 9. This is possible because in our connect( ) we have our mapDispatchToProps (or specifically {fetchCountries}) passed in as an argument. This line leads us to the fetchCountries action (below).

![](https://i.ibb.co/kx1fJQW/fetch-Countries-action.png)


The action creator taps in to the API and returns data.  This is also where we are able to see the beauty of Redux-Thunk in full effect.  Redux-Thunk allows the return of a function inside the action creator and receives dispatch as an argument (as seen in lines 2-8 above).  In doing this, it solves the issue of an action attempting to display data before the fetch is completed.

We then move from the action to the reducer (seen below) once the action is dispatched to the reducer.

![](https://i.ibb.co/TRswXN2/country-Reducer.png)

The purpose of the reducer is to return the updated state.  So in summary, our flow is Action -> Reducer -> Updated State. The reducer (countryReducer.js in this app) is passed as an argument to the store (line 12 in image below).  The store is accessible to the entire app by wrapping the App component with the Provider component.  The Provider component has store as a prop and is passed down to any component in the app that we connect to the store via the connect( ) method.

![](https://i.ibb.co/rH2wb7T/store.png)


State is mapped to the CountriesContainer component through our connect method, which takes mapStateToProps( ) as an argument. The mapStateToProps( ) is also where we define which slice of state needed for the specific component that is connected to the store.  In the CountriesContainer component, we are wanting to access state.countries which is defined to be the value of countries.  The countries information is passed down from CountriesContainer to its child components (Countries component and Country component) as a prop (seen on line 24 of the CountriesContainer component) making it possible for the child components to update and display the data received from the fetch call.

Things to keep in mind with the store.  There can only be one store defined in the app.  The store will hold state for the entire app.  This makes mapStateToProps( ) very important to define correctly because it will allow to select the exact piece of state we want for a specific component.

React-Redux together make a great union for getting the best out of React in using it to focus on the presentational side while using Redux to separate logic and making it easier when needing to debug.  Having a clear flow of how data is passed allows us to better narrow down where the issues are, if any are found.



☆ Emilia ☆






