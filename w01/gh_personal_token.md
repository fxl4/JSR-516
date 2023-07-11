# Github Personal Access Token Setup

In 2021, Github went through a large security update. There are a few new steps needed to get full authentication with a github account. Here is a detailed guide on how to generate and use the Personal Access Tokens that Github now requires.

### Step 1 - Creating Our First Repo

- At the top right of your Github page, click the grey Plus sign "+" and select "New Repository". This is how we create our own Github Repo's, and it is something we will be doing throughout the class.

- You will see a few options and prompts. Where it says "Respoitory Name", type in something simple, like "first-repo"

- Set this to Public, and select the box to Initialize with a ReadMe. This will allow us to Clone this repo down to use on our computers (we'll see what this means soon!)

- Do not worry about gitignores and licences, they are not relevent yet

- Once it lights up, click the big green button that says "Create Repository". You will be redirected to your new Github Repo, which we can clone down and work with!

- Towards the top-right of the page, you'll see another big green button that says "Code", with 3 options. We are going to copy that link in a few quick minutes

### Step 2 - Getting a Personal Access Token

- Open up a new tab on your browser and go to your github page.

- Click on your profile picture and go to Settings

- At the bottom of the left hand menu, go to Developer Settings, then Personal Access Tokens, and click 'Tokens'

- Once at the Token page, click "Generate New Token". You will be given a menu of options to choose from.

- Select "No expiration date" from the drop down menu, and click on each checkbox, to give yourself full priviliges for all of your repos and projects. Once you have them all selected, hit "Generate Token".

- You will only have one chance to use this Token, so do not X out or leave this page. If you do, you'll just have to redo the previous Step 2 parts, which should only take a few seconds, but its still easier not to have to.

### Step 3 - Logging in with your PAT

- Return to your original Github tab with the repo you have created, and using that big green button, Clone your repo down into your computer

- We do this by cd'ing into whichever folder we want to work with and entering

```
git clone ~paste url here~
```

into our terminal.

- Once we have the new repo with its readme file cloned to our computer, lets make a minor change in it so we can Push it up, and enter our PAT into the Github input on our terminal

- CD into your directory and create a dummy file, something like

```
touch dummy.txt
```

- Then, lets run our 3 Git commands:

```
git add .

git commit -m"initial commit"

git push origin main
```

- When you enter your Push command, you should receieve a message in your terminal that says something like "Github changed its security options in 2021... please use a Personal Access Token..."

- You'll be asked to enter your Github user name. Enter it there. Remember, this is gitHUB not gitENTERPRISE, so make sure you are using your correct login info when prompted to this screen

- After entering your login, you will be asked to enter a password. Github does NOT want your actual password here, it wants a copy of your Personal Access Token

- Go back to your second Github Tab, where you created the Token, and copy it. Then go into your terminal and paste it in. Remember! Your terminal does not always populate when passwords are added, so if you have pasted it in, but do not see anything, that is alright (we know, this is annoying!)

- Once you paste your PAT in and hit enter, you should see a few lines appear on your terminal with words like "compressing... 100%, deltas...100%" and then it should return to your normal Command Line. You will know it works because it does not give any error messages.

- Once you have made this push and set up your login and PAT congratulations! Your computer is now connected to your Github account and you have all of the power of Github at your commmand (at least until the next security upgrade)
