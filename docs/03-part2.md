# Part 2: Creating the landing page

### Setting Up the First View

When users visit our webpage, we want them to first see an introductory message before transitioning to the main content.

To achieve this effect:

1. We will create an intro container that appears first.
2. After a few seconds, it will fade away, revealing the main container.
3. We will use JavaScript timeouts to control this transition.

### Hiding Elements with CSS
We need a way to hide and show containers dynamically. The easiest way is to define a CSS class that makes elements invisible.
Add the following CSS to styles.css. Afterwards, we update our main-container with this class in the HTML file.

```css
.hidden {
  display: none;
}
```
### Creating the into Container

Now, lets go ahead and create the intro container. This container is very similar to the container we created earlier, but with a different id. It will display a message and a gif.

```html
<div id="intro-container">
    <img
        id="gif-container"
        src=message_gif
        alt="Gif of message gif"
    />
      <p>Hi special person, I have a message for you</p>
</div>
```

### Transitioning to the Main Container

Now comes the fun part! We will hide the intro container after a few seconds and show the main container using JavaScript.
We are going to use timeouts to write a function that will wait for sometime, then hides the intro container by setting the display to "none".
Afterwards, it will remove hidden class from our main-container to make it visible.

```javascript

setTimeout(() => {
    document.getElementById("intro-container").style.display = "none";
    document.getElementById("main-container").classList.remove("hidden");
}, 9000);

```

If the transition feels too abrupt, we can introduce a small delay between hiding the intro and showing the main container.
This can be done by using another timeout to delay the second command. Your code should look something like this.

```javascript

setTimeout(() => {
    document.getElementById("intro-container").style.display = "none";
        
    setTimeout(() => {
        document.getElementById("main-container").classList.remove("hidden");
    }, 2000);

}, 9000);

```

### Adding a Typing Effect

To increase excitement, we’ll animate the text so it types out letter by letter, rather than appearing all at once.
We’ll make a reusable function that can type any text dynamically.
Our function is going to take the id of the element we want our text to appear, the text, along with the speed (dela between typing each letter).


```javascript 

function createTypingEffect(elementId, text, speed = 100) {
    const element = document.getElementById(elementId);
    let index = 0;

    function typeNextLetter() {
        if (index < text.length) {
        element.textContent += text.charAt(index);
        index++;
        setTimeout(typeNextLetter, speed);
        }
    }

    typeNextLetter();
}

```

