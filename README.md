
# Build a Discord Bot 👾

Have you ever wondered about how Discord bots work? Have you ever 
wanted to build your own custom Discord bot? Don’t miss out on this awesome workshop; 
make sure you're registered at the link in the Discord or at [starhacks.tech](https://www.starhacks.tech/) 💫

Discord is a powerful messaging platform with great chat capabilities originally 
built to serve gaming communities. it has grown to a massive popularity and offers 
a lot of customization and autonomy via bots, custom moderation tools and more, 
which I’ll show you how to work with! in this tutorial I’ll show you how to set 
up a fully customizable Discord bot that can be running on your server in under
 15 minutes. this tutorial is taught using Javascript, but if you are a beginner 
 don’t worry! We’ll walk through it together.

i set this repository up so that anyone can fork or clone it and add their own tokens
and capabilities for their own bot easily, so if you don't want to start from scratch,
fork this repo!
## 🚀 About Me

my name is Rachel, and I am currently in her senior year at New York University, 
majoring in Computer Science and minoring in Game Engineering. my interests include 
web development, game engineering, 3D modeling and AR and VR!

* twitter ([therachelplan](https://twitter.com/therachelplan))
* linkedin ([rachelombok](https://linkedin.com/in/rachelombok))
* discord (racheletc#1212)

## Prerequisites

* a Discord account ([sign up here]())
* NodeJS([`node`](https://nodejs.org/en/download/)) and [`npm`](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) installed
* your favorite IDE 🤩 (VSCode, Notepad++, Webstorm, etc.)
## Workshop Resources
* [Skeleton Base Repo](https://github.com/rachelombok/DiscordBotWorkshop)
* [discord.js Documentation](https://discord.js.org/#/docs/discord.js/stable/general/welcome)
* [discordbots.org](discordbots.org) (premade bot examples)
## Steps

#### 1.) Creating the Discord bot

* Visit the [Discord portal](https://discordapp.com/developers/applications/) and click on new application
* Give your application a unique name and click the Create button 
* On the left panel, click on the **Bot** tab and click on **Add Bot**
* Now our bot is created and we can invite it to our server!

#### 2.) Adding the bot to your server
* On the left panel, navigate to the **OAuth2** panel and select the bot you just created
* Select the needed permissions for your bot (Read Messages/View Channels, Send Messages, Manage Messages, )
* Copy the generated URL link and paste it into your browser
* After pasting it we can add it to our server by selecting it and clicking the authorize button

#### 3.) Creating our Project
* We can create our project directory from the terminal and start coding it!
`mkdir my-bot && cd my-bot`
* Then create the two files that we will work with
`touch index.js && touch config.json`
* run `npm init` and fill out the questions, this will help us keep track of our project information
* Now open your project in your preferred IDE 

#### 4.) DiscordJS basics
* Install these dependencies
`npm install discord.js @discordjs/opus --save`
* Fill our [`config.json`]() file with your command prefix and your bot token. To get the token go back to the Discord portal and copy it from the bot section
* Create your bot with the appropriate functionality you'd like for your app. Use my skeleton from the [`index.js`]() file

#### 5.) Run Locally 📡
* to start your bot, run `node index.js`, you should see the console message 'Ready' if it is up and running.
* type your commands in the channel where the bot has been invited, and make sure the bot behaves as your programmed it to

#### 5.) Pushing to your repository
If you push your repo as is, your secret bot token will be exposed publicly will cause Discord to flag you down and your token will no longer work. To make sure your token stays secure, we need to tell our project to ignore when pushing to our repository. We will also include the `node_modules` folder since that is also not needed for pushing our project

* Create an environment file to host your variables 
`touch .env`, and then add this code block to the file:
```
TOKEN='your-bot-token'
PREFIX='your-prefix'
```
* Create a gitignore file 
`touch .gitignore`
* install the `dotenv` dependency
`npm install dotenv`
* Since your `.env` file was created before the `.gitignore`, it is not yet tracking the file. To do so, untrack the cached files with the two commands:
`git rm --cached .env` and `git rm --cached node_modules`
* if you've already committed these files and are given an error, try adding `-r` to the command:
`git rm -r --cached .env` and `git rm -r --cached node_modules`
* now if you run `git status` in your terminal, it will show all the files that are untracked in your project
* in `index.js`, add `require('dotenv').config();` to the top of the file
* instead of importing the config variables from `config.json` we can now use the `.env` file variables by using `process.env.TOKEN` and `process.env.PREFIX`
* if you are working on a team, you can add the environment variables by going to the **Settings** tab in your repository, navigating to **Environments**, and clicking the **New Environments** button to add the variable secrets
* You can now host your bot on an external service, tutorial links and resources are listed below.
## Other Resources
* [🤖Guide: How to build a Discord music bot](https://www.freecodecamp.org/news/how-to-create-a-music-bot-using-discord-js-4436f5f3f0f8/) - Learn how you can create your own custom music bot for your server from scratch!
* [How to Host Discord Bot on Heroku for free](https://www.techwithtim.net/tutorials/discord-py/hosting-a-discord-bot-for-free/)
* [Definitive Guide for hosting your Discord Bot](https://www.writebots.com/discord-bot-hosting/)
## Conclusion

If you have any questions or feedback, let me know by messaging me in Discord!