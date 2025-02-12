# Part 3: Adding user interaction

Now it is time to set the foundation for the interactive bits for your website. In this section, we will: Set the messages someone gets when they click no, and what will happen when your special someone clicks either yes or no.

### Yes Button Actions :) 

When the user hits the yes button, we want 3 things to happen.
1. Change the GIF
2. Change the main text
3. Remove the buttons from the screen. 


We want to write a function that is triggered when the user clicks on the yes button.

```javascript
yesButton.addEventListener("click", () => {
    // Insert Tasks Here!
});
```
When the user hits yes we only have to remove and set variables to new values. 

To remove the buttons, we set the style property of both buttons to “none”. 

To change the GIF and the main text, we just set the variables responsible for this to the new message and GIF link we want to display (`gif.src` for the new GIF Link, `mainText.textContent` for the new message). Make sure these are all in strings!

Your finished product should look like this:
```javascript
yesButton.addEventListener("click", () => {
    yesButton.style.display = "none";
    noButton.style.display = "none";
    gif.src = "https://media.tenor.com/TEC6z0acIbUAAAAj/cute-bears-love.gif";
    mainText.textContent = "yay! i knew you would say yes! <3";
});

```

### Adding Fun Interactions for the "No" Button

Now that we’ve set up a fun and heartwarming reaction for when someone clicks "Yes", let’s make saying "No" a little harder! 😂

Instead of simply letting your special someone click "No", we’ll add a fun challenge:

1. First, the "No" button moves away whenever the mouse gets too close.
2. After n attempts, we give up and trigger a "sad" function


### Making the "No" Button Run Away
To add an interactive "No" button escape mechanism, we need to:

Track the mouse hover event on the "No" button.
Move the button to a random position when the user gets too close.

```javascript
noButton.addEventListener("mouseover", () => {
    let randomX = Math.random() * (window.innerWidth - noButton.clientWidth);
    let randomY = Math.random() * (window.innerHeight - noButton.clientHeight);

    noButton.style.position = "absolute";
    noButton.style.left = `${randomX}px`;
    noButton.style.top = `${randomY}px`;
});

```

### Counting Failed Attempts
Next, we’ll track how many times the user tries to hover over "No". If they fail n times, we’ll trigger a  reaction.

```javascript

let noHoverCount = 0; 

noButton.addEventListener("mouseover", () => {
    let randomX = Math.random() * (window.innerWidth - noButton.clientWidth);
    let randomY = Math.random() * (window.innerHeight - noButton.clientHeight);

    noButton.style.position = "absolute";
    noButton.style.left = `${randomX}px`;
    noButton.style.top = `${randomY}px`;

    noHoverCount++; 

    if (noHoverCount >= 5) {
        triggerSadFunction();
    }
});

```

### Write the sad Function

In the unfortunate case your crush doesn't want to be your valentines, we want to remove the buttons and change the gif.
Similar to our yesButton function but with a sad gif


```javascript
    // Insert Tasks Here!
```

Congrats! The foundation for the website is now set, let's see how we can deploy this site and send it to your special someone ;) 