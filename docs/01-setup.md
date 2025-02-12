# Setup

Ideally, we are assuming that you have already installed Visual Studio Code and the Live Server extension for VS code. If not, you can download Visual Studio Code from [here](https://code.visualstudio.com/download) and the Live Server extension from [here](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer).


You can run the code directly in your browser using the following CodeSandbox link: (https://codesandbox.io/p/sandbox/gdzlzh?file=%2Fsrc%2Fstyles.css%3A14%2C18). If you don’t have a CodeSandbox account, you’ll need to create one. To edit the code, click the Fork button at the top right of the window to create your own copy and start coding!





# Setting Up on Visual Studio Code

## Installing Visual Studio Code and Live Server
1. Open Visual Studio Code
2. Click on the Extensions icon on the left side of the screen
3. Search for "Live Server" and click on the first result
4. Click on the green "Install" button
5. Once installed, click on the "Reload" button to reload the window

## Creating the Files
1. Create a new folder on your desktop and name it "Valentines Day 2024"
2. Inside the folder, create a new file and name it "index.html" You're going to want to paste the following HTML into the file:
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Emerging Coders Valentines Day Event</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
  </head>
  <body>
    <div class="main-container">
        <!-- TODO: Add the title of the webpage, an image, and a message here -->
    <div class="button-container">
        <!-- TODO: Add the Yes and No buttons here -->
    </div>

    </div>
    <script type="text/javascript" src="index.js"></script>
  </body>
</html>
```
3. Next, create another file and name it "style.css". You can paste these styles into the file (but feel free to change them!): 
```css
body {
  background-color: #de3163;
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  color: white;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  height: 70vh;
}

.main-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

#main-container img {
  display: block;
  margin: 0 auto;
  max-width: 100%;
}

.button-container {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  margin-top: 20px;
  margin-bottom: 10%;
  gap: 15px;
}

.intro-container {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  margin-top: 20px;
  margin-bottom: 10%;
  gap: 15px;
}

#intro-container img {
  display: block;
  margin: 0 auto;
  max-width: 100%;
}

#yes-button {
  background-color: #50ff64;
  color: black;
  border: none;
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  cursor: pointer;
  border-radius: 5px;
}

#no-button {
  background-color: #ff5050;
  color: black;
  border: none;
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  cursor: pointer;
  border-radius: 5px;
}

.hidden {
  display: none;
}
.container {
  text-align: center;
  padding: 20px;
}

```


4. Next, create another file and name it "script.js". For now, you can leave it empty as well. 

This is the basis of the setup. You can add more files if you want, but there are the only files that we need to create for this project. 