# HEROKU

Heroku is a webpage deployment platform that allows users to publish their websites online so people can visit and use them. Heroku uses Node.js as a serverside programming language. Thus, people who want to deploy their websites on Heroku should build their back-end with Node.

Node is a runtime environment that gives JavaScript the ability to work outside web browsers. Developers can write their code in JS, and they will be able to run it on the server.

To use Heroku, we should first install node.js, NPM, and GIT. After we verify their versions, we can install Heroku and log in to our server.

`sudo snap install Heroku --classic`
`Heroku login`

We have to make sure that our project is already setup and a package.json file is exists. When we are ready, we just need to create the project on Heroku using:

`Heroku create <project-name>`

If we did not specify the project name, Heroku would give it a random name. Now, we have the project created and deployed on Heroku, and a git remote name of Heroku is created so we can push to it.

`git push Heroku main`

Here, our website is finally deployed, and we can visit it using the shortcut `Heroku open`

If you want to view your website logs, use this command:

`Heroku logs --tail`

Your application should have the package.json file for Heroku to tell the node environment to install the specified packages inside the file.

If you don't have this file, you can run this command, and it will be added automatically.

`npm init`

If you want to install the packages, run this command to download and install all the dependencies

`npm install`
