# Deploying the Website

Awesome! Now that you have completed the core functionality of our Valentines Day project, now its ready to be sent out to the world and more specifically, you _special someone_. 

You have a few options here, you can either host the website on your own server or use a cloud service like AWS, Azure, or Google Cloud. But that may be a bit overkill for this project. 

## GitHub Pages

Instead, we can use a service like GitHub Pages to host our website. GitHub Pages is a static site hosting service that takes HTML, CSS, and JavaScript files straight from a repository on GitHub, and runs the files through a build process before serving them up. If you already have a GitHub account, you can use GitHub Pages to host a website for free. 

Here's how to do it:

1. Create a new repository on GitHub.
2. Push your code to the repository.
3. Go to the repository settings and scroll down to the GitHub Pages section.
4. Select the `main` branch as the source and click save.
5. After a few minutes, your website will be live at `https://<username>.github.io/<repository-name>`.

## Netlify  

Another option is to use Netlify. Netlify is a cloud computing company that offers hosting and serverless backend services for web applications and static websites. It's a great option for hosting static websites and it's free to use.

Here's how to do it:

1. Go to the Netlify website and sign up for an account.
2. Click on the "New site from Git" button.
3. Connect your GitHub account and select the repository you want to deploy.
4. Click "Deploy site".
5. After a few minutes, your website will be live at `https://<random-name>.netlify.app`.

