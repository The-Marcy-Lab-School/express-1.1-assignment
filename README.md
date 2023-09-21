# express-1.1-assignment

> Note: To complete this assignment, you must be using VS Code locally. Here are instructions for setting up on a [Mac](https://github.com/The-Marcy-Lab-School/local-environment-setup-mac) and on [Windows](https://github.com/The-Marcy-Lab-School/local-environment-setup-wsl). If you need help, please speak with your instructor. 

## Overview

In this assignment, you will create and deploy a simple backend server using the [Express](https://expressjs.com/) framework. At the end of this assignment, you will deploy your server on [render.com](https://render.com/), enabling anyone on the internet to access it!

This assignment has three milestones:
1. Create a server application that can serve a basic website.
2. Deploy that server using a service like Render
3. Implement Create, Read, Update, and Delete endpoints that modify data stored in the server's memory.

Let's get started!

## Milestone 1: Create a Server Application

In this first step, you will create a server application using Express! To do this, you will need to do the following:
1. Create a new Github repository on your account.
2. Clone that repository to your local development environment. 
3. Create an `index.js` file that starts a server listening on port `8080` (or another port of your choosing).
4. Create an `index.html` file with content of your choosing!
5. Create an endpoint such that when a client sends a GET request to `"/"`, your server sends the `index.html` file in response.
6. Test out your server by running the `index.js` file and heading over to http://localhost:8080. You should see your website.
7. Once it is working, push your code up to your Github repo!

> 💡 Note: If you want to add CSS or a JS script to your website, you will need to add them directly to your `index.html` file. If you would like to use separate files, see the bonus section!

Submit the link to your repository to your instructor for feedback.

## Milestone 2: Deploy the server

Way to go! You have a working server, but it only runs on `localhost`. Time to deploy!
1. Head over to render.com
2. Create an account using your Github account. If you make your account any other way, you will need to link your Github account later on.
3. From the **dashboard** on render, click on the <kbd>New +</kbd> button and select **Web Service**.
4. Select **Build and deploy from a Git repository**
5. Find the repository you made in step 1 and click **Connect**
6. Give your service a new name (Note: this name will become a part of your server's given URL)
7. The rest of the settings you should be able to leave as default as long as you've followed the steps above. Select the **Free Instance Type** and click <kbd>Create Web Service</kbd>!
8. The deployment process will take a few minutes, but once it is done you will be given a URL for your server like this: https://basic-express-website.onrender.com/

Submit the link to your deployed server to your instructor for feedback.

## Milestone 3: Implement Data Endpoints

Congrats! Your server now provides access to a website, but it can do so much more! Servers typically provide access to data and allow clients the ability to modify that data. In this step, you will add in-memory data to your server that the client can read and add to.

1. In your `index.js` file, you should:
  - Have an in-memory object with at least one property that is an array. The array can be anything, like a list of friends, favorite colors, or phone numbers.
  - Use the `express.json()` middleware to parse JSON from incoming request bodies
  - An endpoint for getting the in-memory object
  - An endpoint for posting a new value to the array in your in-memory object. This endpoint should send back the updated object.

2. In your `index.html` file, you should:
  - Have a button that will get data from your server when clicked. The data received should be rendered to the screen.
  - Have a form with an input and a button. When the form is submitted, the value of the input will be sent via a POST request to the server. The response should be rendered to the screen.

3. Test out the functionality of your server on `localhost` before pushing your completed code up to your repository. This will automatically trigger your deployed server to re-deploy.
4. Test out the functionality of your deployed server.

Submit the link to your deployed server to your instructor for feedback.

## Bonus!

If you want your website to have the HTML, CSS, and JS files separated, take a look at the `express.static()` middleware. This will allow you to put all of your "static assets" (the HTML, CSS, and JS) into a folder that your server can send to the client when a GET request is made to `"/"`.

https://expressjs.com/en/starter/static-files.html

# Celebrate!

![](https://media.tenor.com/Oj2nKJiZSU4AAAAC/celebration-will-smith.gif)
