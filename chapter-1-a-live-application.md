# Chapter 1: A live application
Our goal for this chapter is to deploy a simple application that has the words *Hello World* on a white web page. As we work our way through creating our application we will answer the question of *What is coding?* create a development environment where you can code, create a web application, and deploy our application to a public website you can show anybody on the web.

## What is coding?
*What is coding?* Coding is the act of writing a set of commands, or code, into a text file. The commands in file are written to follow a set of rules defined by the specific programming language. The text file is converted to a program by executing each instruction in the file line by line, or the file can be read for errors and then converted all at once to a runnable program. 

These programs are found all over the computer. When you are opening files, creating folders, downloading ebooks or doing anything with our computer we are coding. However we aren't considered coders because we did not write how these programs should behave when they are opened. We interact with the code written by someone else, and the program is responding to all the actions we are performing on the computer. 

## Deploy our first application
To start coding we are going to need a development environment. The purpose of a development environment is to develop programs. There are other environments that are used to test applications or see how they will behave once they are deployed live, these are commonly called test and production.

### Setting up our development environment
Our development environment will be created using a tool called Docker. Docker is a software tool that allows us to contain our application in an operating environment that is different from our personal computer. Why do we want to do this? When you  deploy an application you will need to upload it to a server. A server is responsible for _serving_ your application to anybody on the web that visits the URL of that app. These servers also have their own operating system and they primarily use different variations of Linux. To avoid nasty errors because our personal computer environment is not the same as the server, we try to make our personal environment identical to the server environment. 

Since every computer has its own personality and different set of settings then we can avoid the headache of having to fix errors in our application caused by the different settings on both computers. As you begin to create applications you will often run into a scenario where the application runs fine on your computer but not on the server, Docker solves that problem.

### Get a sample application
Our first application will be a premade application stored in the cloud. **Github** is a web application used to store our the code of our applications in cloud storage. If the computer we use to develop becomes unuseable and needs to be replaced we can rest easy knowing our application files are safely stored in another location. Github also gives us the power of version control. Version control is a way to visualize the different states of your applications. Create an account with [Github](https://github.com) (or [Bitbucket](https://bitbucket.org/) since its free). We will use our account to get a copy of the sample application we will be deploying. 

To create different application states we use a tool called **Git**. When we finish fixing a bug or creating a new application features, we use Git to create a snapshot of the current application state. Once created, the snapshot is saved to Github where we can easily view the different versions of our application. This would be the equivalent to writing a long paper and saving your work along the way. Once the work is in a state that you are satisfied with, you create a backup and push the document to a remote cloud service like Google drive, iCloud or Dropbox. In ther current terminal session (or to create a new terminal session right-click the desktop and select, `Open Terminal`) install Git. 

```
$ sudo apt-get install git-all // might not be necessary
```

Causing errors after git-all install
(https://askubuntu.com/questions/771839/problem-installing-package-git-all)

Type `Y` to any prompts to continue with installation. Now our computer can access Github from the terminal. Change to the base directory, a directory is terminal talk for folder, and clone our new application.

```

$ cd
$ git clone https://github.com/nodox/fsbc-chapter1.git
```

This command says to move our current directory to the lowest level and clone and application. Using Finder you should see a folder titled `fsbc-chapter1` on the root level of you computer. We are going to extend this simple prebuilt application and later deploy it. Change directories to be at the root of your application folder and build the operating system image with docker. 

```
$ cd fsbc-chapter1
$ node bin/www
```

Open your favorite web browser and visit `localhost:3000`. You will see a white page with the words 'Hello World!'. You've just created your first application! Press `CTRL + C` on your keyboard to end the local server.

Its working on our local computer but people on the web can't see it yet. We need to find a server to host our app or we can find a hosting provider to host our application. Since we don't know how to configure servers yet we are better off using a hosting service.

Heroku is a great hosting service for web applications of different types. A provider like Heroku allows us to build and deploy web applications without having to know how to setup servers. [Create a free account using their website](https://www.heroku.com/). Next install the command line interface (CLI) toolbelt for Heroku found [here](https://devcenter.heroku.com/articles/heroku-cli). This toolbelt will allow us to use the command line to push our application from our local computer to Heroku for hosting.

Go back to terminal and login to your Heroku account using the credentials you gave during registration and create a new Heroku application.

```
$ heroku login
$ heroku create
```

The name of your new Heroku application will be listed as `https://NAME.herokuapp.com` in the terminal. Now let's push our application code to heroku.

```
$ git push heroku master
```
Now open your browser and visit `https://NAME.herokuapp.com` and you will see the message *Hello World* in your browser.
Anyone with an internet connection can now see your app when they visit your URL. Congratulations you've deployed your first application!

In the next chapter we are going to learn HTML and CSS to add more features to our simple application.


Next application will be a 
  * chapter2: bucket list HTML/CSS 
  * chapter3: bucket list (TodoMVC examples)



***

**Disclaimer: This book is a work-in-progress.**

**Please give feedback on your experience using this [survey link](https://www.surveymonkey.com/r/JY27M3J). Any feedback helps make a better book for you. Thank you!**

**If you haven't joined the mailing list to be the first notified of new chapters then sign up using this [form link](http://eepurl.com/cW_Xjr)**

