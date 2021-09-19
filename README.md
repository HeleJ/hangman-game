# HANGMAN game

This game ws built as part of the learning material for Code Institute's Fullstack Web Developer program (5P) Portfolio Project.

Portfolio Project Three: Python - Code Institute - Deadline 24th September 2021

Hangman is an old school favorite, a word game where the goal is simply to find the missing word or words Python terminal game, which runs in the Code Institute mock terminal on Heroku.

You can check out the live game [here](https://hangman-game1x.herokuapp.com/)

![my-page](controllers/assets/images/my-app-image.png)

# How to play

* If you know how to play the game you can start game, otherwise you can read about how to play the game.

* You will have to make a choice what category to select

* You will be presented with a number of blank spaces representing the missing letters you need to find.

* Use the keyboard to guess a letter (I recommend starting with vowels).

* If your chosen letter exists in the answer, then all places in the answer where that letter appear will be revealed.

* After you've revealed several letters, you may be able to guess what the answer is and fill bit more easy in the remaining letters.

* Every time you guess a letter wrong you loose a life and the hangman begins to appear, piece by piece.

* To win you need to solve the puzzle before the hangman dies.

# Features

### Exsisting Features (with functions)

![game start](controllers/assets/images/heroku-start-game.png)

![game-start](controllers/assets/images/heroku-start-welcome.png)

   * Display greeting , ASCKII art, user input for name 
      * def display_greeting()

![game rules](controllers/assets/images/game-rules.png)
 
   * Ask the player either display the rules or go for game
      * def display_rules()
   * Display rules
      * def rules_txt()

![game categories](controllers/assets/images/heroku-category.png)

   * Display categories
   * User input for selecting category  
      * def category_select()

![letters joice](controllers/assets/images/heroku-incorrect-right-letter.png)

![end image](controllers/assets/images/heroku-end-lost.png)

   * Ask the player to enter letters one at the time
   * if player entered letter what is right for randomly selected word,
      the letter will be displayed insted of "_" underscore
   * if player enetering the letter what is not in the word, hangman image starts 
      develop
   * player getting note when doubble selected the same letter  
      * def select_question()   
      * def hangman()
      * def display_guess_message()
      * def display_alredy_used()

![hurray](controllers/assets/images/heroku-end-winning.png)   

   * If user quessed all letters, display ASCII image - Hurray!  
      * def hangman()

![game over](controllers/assets/images/game-over.png)  
   * end of game displac image ASCII art 
   * ask from player whould he likes to play again or exit game using keybord or Run Programm button above
   * user input what joice he made  
      * def game_over()
      * def replay()

### IMAGES   

Are greated using [ASCII art](http://patorjk.com/software/taag)

![hangman greeting](controllers/assets/images/hangman-image.png)

![hurray](controllers/assets/images/hurray-image.png)

![game over](controllers/assets/images/game-over-image.png)

Visual [hangman stages](https://enhancer298.net/2020/07/10/hangman1/)

![hangman stages](controllers/assets/images/hangman.png)



### Future Features

* Hangman game is old, old game and the word at current childrens play list can be odd. Taking consideration mental health and suitside issues. So for that reason I would give different visualisation option where you can select build a snowman or melting snowman.

* more categorys to select

* bigger list of words. Special file to accomodate that.

* for a language lerning purpose was be good to hear this word sound.

* the letters can be displayed for selection

* different difficulty levels 

# Data Model

The flowchart below summarises the data flow in this program.
![Flowchart](controllers/assets/) Pilt sisse

# Technology

*  This game was created with:

    * [Gitpod](https://www.gitpod.io/) used to develop project and organise version control 

    * [Github](https://github.com) used to host repository
       
    * [Heroku](https://id.heroku.com/login) used to deploy my application

* [Lucid](https://lucid.app/users/login#/login) used to create the flowchart for the project.

* [Grammarly](https://app.grammarly.com/) used to fix the thousands of grammar errors across the project.

* The Code Institute's GitHub full template for Python is used in order for the program to display properly in the deployed site on Heroku.

* [random](https://docs.python.org/3/library/random.html) to randomize anagram

* [time](https://docs.python.org/3/library/time.html) to slow down printed statements

* Python 3 - an interpreted high-level general-purpose backend programming language.

# Testing

I have manually tested this project by doing the following: 
* Passed the code through a PEP8 linter and confirmed, there are no problems (find under validator testing)
* Give invalid inputs strings when numbers are expected, out of bound inputs, some inputs twice

![only numbers](controllers/assets/images/only-numbers.png)

* Tested ASCII art printout

![ascii](controllers/assets/images/test-greeting-print.png)

* Tested in my local terminal and the Code Institute Heroku terminal
* [Python tutor](https://pythontutor.com/visualize.html#mode=edit)

![python-tutor](controllers/assets/images/pythontutor-image.png)

* lighthouse

![lighthouse](controllers/assets/images/lighthouse-hangman.png)

## Bugs

### Solved Bugs

## Remaining Bugs

* No bugs remaining

## Validator Testings

* [PEP8](http://pep8online.com/checkresult)
    * No errors were returned from PEP8online.com

![pep8](controllers/assets/images/pep8online.png)    

# Deployment

This project was deployed using Code Institute's mock terminal for Heroku. Please follow the below steps.

## Deployment steps

1. Git add and git commit the changes made

2. Log into [Heroku](https://id.heroku.com/login) or create a new account and log in

3. top right-hand corner click "New" and choose the option Create new app, if you are a new user, the "Create new app" button will appear in the middle of the screen

4. Write app name - it has to be unique, it cannot be the same as this app

5. Choose Region - I am in Europe

6. Click "Create App" The page of your project opens.

7.  Choose "settings" from the menu on the top of the page

8. Go to section "Config Vars" and click button "Reveal Config Vars"

![config vars](controllers/assets/images/config-vars.png)

9. In the field for "KEY" enter "PORT"-  capital letters and value"8000" 

10. Go to section "Build packs" and click "Add build pack"

   * in this new window - click Python and "Save changes" [`heroku/Python`]
   * click "Add build pack" again
   * in this new window - click Node.js and "Save changes" [`heroku/NodeJS`]
   * take care to have those apps in this order: Python first, Node.js second, drag and drop if needed

![buildpacks](controllers/assets/images/buildpacks.png)

11. Next go to "Deploy" in the menu bar on the top

12. Go to section "deployment method", choose "GitHub"

13. New section will appear "Connect to GitHub" - Search for the repository to connect to

14. type the name of your repository and click "search"

15. once Heroku finds your repository - click "connect"

16. Scroll down to the section "Automatic Deploys"

17. Click "Enable automatic deploys" or choose "Deploy branch" and manually deploy

18. Click "Deploy branch"

Once the program runs: you should see the message "the app was sussesfully deployed"

 19. Click the button "View"

# Forking the GitHub repository

By forking the GitHub Repository we make a copy of the original repository on our GitHub account to view and/or make changes without affecting the original repository by using the following steps:

1. Log into [GitHub](https://github.com/) or [create an account](https://github.com/).

2. Locate the GitHub repository. Link can be found [here](https://github.com/HeleJ/hangman-game).

3. At the top of the repository, on the right side of the page, select "Fork".

4. You should now have a copy of the original repository in your GitHub account.

# Making a local clone

1. Locate the GitHub repository. Link can be found [here](https://github.com/HeleJ/hangman-game).

2. Next to the green Gitpod button you will see a button "code" with an arrow pointing down

3. You are given the option to open with GitHub desktop or download zip

4. You can also copy https full link, go to git bash and write git clone and paste the full link

# Credits

* Code Institute for the deployment terminal

* To greate game I got help [from](http://inventwithpython.com/invent4thed/chapter8.html)

* Idea for [flowchart](http://inventwithpython.com/invent4thed/chapter7.html)

* Code Institute - John from Tutor Support

* Code Institute - Kasia, our group leader. Amazing teacher, who gives more than 100% to get us true. Thanks to her Im still studding in this course. Thanks to her Im finishing my third project.


## Creating the Heroku app

When you create the app, you will need to add two buildpacks from the _Settings_ tab. The ordering is as follows:

1. `heroku/python`
2. `heroku/nodejs`

You must then create a _Config Var_ called `PORT`. Set this to `8000`

If you have credentials, such as in the Love Sandwiches project, you must create another _Config Var_ called `CREDS` and paste the JSON into the value field.

Connect your GitHub repository and deploy as normal.

## Constraints

The deployment terminal is set to 80 columns by 24 rows. That means that each line of text needs to be 80 characters or less otherwise it will be wrapped onto a second line.

-----
Happy coding!