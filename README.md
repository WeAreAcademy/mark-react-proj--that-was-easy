---
module: react-spa

level: 1

methods:
  - team
  - pair
  - solo

tags:
  - wip
---

# That was easy!

<a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png" /></a>

> This is part of Academy's [technical curriculum for **The Mark**](https://github.com/WeAreAcademy/curriculum-mark). All parts of that curriculum, including this project, are licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a>.

We're now going to start to add interactivity into our **React** apps, using event listeners. 

## Learning Outcomes

- Use event listeners
- Practice using map to create JSX elements
- Pass anonymous arrow functions and function references into event listeners
- Set up state within an app and change the state using event listeners

## Exercise 1: "Easy" button

> 🎯 **Success criterion:** A button which alerts the user when clicked

So far, we used React to display information in the browser, but how do we get it to respond to the users actions? This is where event listeners come in. 

Create a new React app in TypeScript. Taking inspiration from the stationary classic ["that was easy" red button](https://www.youtube.com/watch?v=3YmMNpbFjp0) create a button in the centre of the screen. Label it "easy" and use `onClick` in order to show an [alert box](https://www.w3schools.com/js/js_popup.asp) when it is clicked. The alert box should tell the user `that was easy`. Use an anonymous arrow function as the event listener.

Take ten mins to experiment with the look of the button: 
- How similar to the button from the video can you make it appear?
- Can you make it round?
- Can you change its appearance when it is hovered over? (using only css)

## Exercise 2:

> 🎯 **Success criterion:** Multiple buttons which each alert the user about diffierent levels of "easiness"

### Exercise 2a: More button options

Create an array of buttons options such as: `["easy", "ok", "difficult", "too difficult"]`.
For each element in the array, render a button, labelled accordingly. When each is clicked it should alert the user with `that was [option]` where the option is the relevant word. 

### Exercise 2b: Passing a function into the event listener

Adapt your existing solution in order to define a function which takes a single parameter and creates an alert box saying `that was [parameter]`. Now pass this function to each button.

### Exercise 2c: A button component

If you haven't already, then make a button component and reuse this child component for all of the buttons. 

### Exercise 2d: Customising the buttons further

Change the appearance of the buttons so that each button has its own colour - for example I may consider a traffic light system where green is more positive and red more negative, but feel free to be creative here.

## Exercise 3: Using `useState`

> 🎯 **Success criterion:** the state of the buttons changes after one is clicked

At the parent level, declare a new state variable for whether or not a button has been clicked. This should start as `false`. When a button is clicked then this should change to `true`. 

You can log this variable to the console in order to check that it is changing as expected.

Pass this variable into the child components and use it to change the class name on the buttons. Change something about the appearance of the buttons based off of it.

## Exercise 4: Calling a higher order click handler

> 🎯 **Success criterion:** toggle the buttons' state with every click

So far, when a button has been clicked the appearance of all the buttons will change and cannot be changed back unless you initialise the state again (by refreshing the page). Now, make it so that each time you click a button the state flips and the appearance changes (change between true and false on every click). 

Hint: to do this you will need to make a click handler function in the parent which changes the state, and pass this click handler function down to the children components where it can be called. Note that state is always managed by the lower common ancestor and so will be managed by the parent here in order for all of the children to be given access to it. 

## Exercise 5: Click counter

> 🎯 **Success criterion:** a click counter which shows the number of times any buttons have been clicked

Add a click counter which counts the number of times the user has clicked button cumulatively. This can be shown however you please.

## Exercise 6: Inidividual click counters

> 🎯 **Success criterion:** click counter for every button separately

Add a click counter for each button. It should now be visible how many times the user has clicked all buttons cumulatively as well as each button individually.

## Exercise 7: The most clicked option

> 🎯 **Success criterion:** show the user which option they have clicked the most times

Give the user feedback on which option is their favourite. Add a crown to the button which has been clicked the most times or any other visual indication. 

Consider how it should look before the user has clicked any buttons too.