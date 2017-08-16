# Chapter 1: A live application
Our goal for this chapter is to deploy a simple application that has the words *Hello World* on a white web page. As we work our way through creating our application we will answer the question of *What is coding?* create a development environment where you can code, create a web application, and deploy our application to a public website you can show anybody on the web.

* get raw github urls for images [here](https://rawgit.com/)









## Deploy our first application
To start coding we are going to need a development environment. The purpose of a development environment is to develop programs. There are other environments that are used to test applications or see how they will behave once they are deployed live, these are commonly called test and production.

### Setting up our development environment
Our development environment will be created using a tool called Docker. Docker is a software tool that allows us to contain our application in an operating environment that is different from our personal computer. Why do we want to do this? When you  deploy an application you will need to upload it to a server. A server is responsible for _serving_ your application to anybody on the web that visits the URL of that app. These servers also have their own operating system and they primarily use different variations of Linux. To avoid nasty errors because our personal computer environment is not the same as the server, we try to make our personal environment identical to the server environment. 

Since every computer has its own personality and different set of settings then we can avoid the headache of having to fix errors in our application caused by the different settings on both computers. As you begin to create applications you will often run into a scenario where the application runs fine on your computer but not on the server, Docker solves that problem.

### Download Docker
Docker is a publicly available. Navigate to the docker website, find the community edition and install the latest version of docker. [Follow this link to the downloads page.](https://www.docker.com/community-edition) Choose the package that fits your computer. Older versions of Mac or Windows might require you to download [docker toolbox](https://docs.docker.com/toolbox), if this is the case you'll recieve a popup window in the docker installation program. Run the installation program and start up docker. You should see the small whale icon in your tool bar.

### Github and Git
Our first application will be a premade application stored in the cloud. **Github** is a web application used to store our the code of our applications in cloud storage. If the computer we use to develop becomes unuseable and needs to be replaced we can rest easy knowing our application files are safely stored in another location. Github also gives us the power of version control. Version control is a way to visualize the different states of your applications.

To create different application states we use a tool called **Git**. When we finish fixing a bug or creating a new application features, we use Git to create a snapshot of the current application state. Once created, the snapshot is saved to Github where we can easily view the different versions of our application. This would be the equivalent to writing a long paper and saving your work along the way. Once the work is in a state that you are satisfied with, you create a backup and push the document to a remote cloud service like Google drive, iCloud or Dropbox.

Create an account with [Github](https://github.com) (or [Bitbucket](https://bitbucket.org/) since its free). We will use our account to get a copy of the sample application we will be deploying. Once you are done install [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) on your computer so we can access Github from the terminal.





#### Get a sample application
Open a new terminal session, change to the base directory.

```
$ cd
$ git clone https://github.com/nodox/fsbc-chapter1.git
```

This command says to move our current directory to the lowest level and clone and application. Using Finder you should see a folder titled `fsbc-chapter1` on the root level of you computer. We are going to extend this simple prebuilt application and later deploy it. Change directories to be at the root of your application folder and build the operating system image with docker. Be sure to start the docker process if its not started.

```
$ cd fsbc-chapter1
$ docker build -t fsbc/chapter1 .
```

Once the build is complete run the application.

```
$ docker run -p 3005:3005 fsbc/chapter1
```

Open your favorite web browser and visit `localhost:3005`. You will see a white page with the words 'Hello World!'. You've just created your first application! Press `CTRL + C` on your keyboard to end the local server.

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

***

**Disclaimer: This book is a work-in-progress.**

**Please give feedback on your experience using this [survey link](https://www.surveymonkey.com/r/JY27M3J). Any feedback helps make a better book for you. Thank you!**

**If you haven't joined the mailing list to be the first notified of new chapters then sign up using this [form link](http://eepurl.com/cW_Xjr)**

