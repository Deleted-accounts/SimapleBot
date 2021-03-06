# SimapleBot

### This bot was created to teach my friends how to deploy a telegram bot on the [heroku](https://heroku.com)

#### So let's get started

- First of all be sure that [heroku CLI](https://devcenter.heroku.com/articles/heroku-cli#download-and-install) and [git](https://git-scm.com/downloads) are installed on your computer

- Now create a new account in [heroku](https://id.heroku.com/signup/login)
- open a terminal and write ```heroku login```
- create a new app usuing the follwing command ```heroku create <your-app-name>```

- Change the Stack for the App using Heroku CLI:
```
heroku stack:set container --app <your-app-name>
```
- clone this repo:
```
git clone https://github.com/Deleted-accounts/SimapleBot
cd SimapleBot
```
- now edit the [config.py](https://github.com/Deleted-accounts/SimapleBot/blob/main/config.py) file
- Initialise the project files as a Git Repository, push the Repo to 'Heroku Git' and build the Docker Image:
```
git init
git add .
git commit -m "initial commit"
heroku git:remote --app <your-app-name>
git push heroku master
```


- If the Docker Image Build succeeds, then, your push to the remote repository will succeed, otherwise, your push to the remote repository is rejected as the Docker Image Build fails.

## Run/Terminate the bot

You can run/terminate the bot by allocating/deallocating dynos to the app.

- To Run:
```
heroku ps:scale worker=1 --app <your-app-name>
```
- To Terminate:
```
heroku ps:scale worker=0 --app <your-app-name>
```
- To Check Status:
```
heroku ps --app <your-app-name>
```
- To Tail App Logs:
```
heroku logs --tail --app <your-app-name>
```


if you have an errors or questions you can ask me here: [Telegram](https://t.me/Successfully_deleted)
