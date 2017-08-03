# Deploy our first application


### Setting up our development environment
To start coding we are going to need a development environment. The purpose of a development environment is to develop code. There are other environments that are used to test applications or see how they will behave once they are deployed live, these are commonly called test and production.

Our development environment will be created using a tool called Docker. Docker is a software tool that allows us to container our application in an operating environmnet that is different from our personal computer. Why do we want to do this? When you finally deploy an application you will need to deploy it to a server. The server is responsible for _serving_ your application to anybody on the web that visits the URL of that app. These servers also have there own opertation systems and they primarily use different variations of Linux. To avoid nasty errors because our personal computer environment is not the same, we try to make our personal environment identical to the server environment. 

Since every computer has its own personality and different set of settings then we can avoid the headache of having to errors in our application caused by the different settings on both computers. As you begin to create applications you will often run into a scenario where the application runs fine on your computer but not on the server. This can be avoided by using Docker.

#### Download Docker
Docker is a publicly available software tool. Navigate to docker website, find the community edition and install the latest version of docker. [Follow this link to the downloads page.](https://www.docker.com/community-edition) Choose the package that fits our computer. Once installed start up docker. You should see the small whale icon in your tool bar.

#### Github and Git
Github is a web application used to store our applications code on the cloud. If the computer we use to develop becomes unuseable and needs to be replaced we can rest easy knowing our application files are safetly stored in another location. Github also gives us the power of version control. Version control is a way to visualize the different states of your applications.

To create different application states we use a tool called Git. When we finish fixing a bug or creating a new application features, we use Git to create a snapshot of the current application state. Once the snapshot is created the snapshot is pushed to Github where we can easily view the different versions of our application. This would be the equivalent to writing a long paper and saving your work along the way. Once the work is in a state that you are satisfied with you create a backup and push the document to a remote place like Google drive, iCloud or Dropbox.

*Create an account with Github* (or Bitbucket since its free). We will use our account to get a copy of the sample application we will be deploying for our friends to see. [And install Git on your computer](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).


#### Get a sample application
Open a new terminal session, `cd` to the desktop directory and type

```
$ git clone https://github.com/nodox/fsbc-chapter1.git
```

This command says to move our current directory to Desktop and clone and application. Using Finder you You should see a folder titled `fsbc-chapter1` on the Desktop of you computer. We are going to extend this simple prebuilt application and later deploy it. Start the docker process if its not on already and run the following command.
```
$ docker build -t fsbc/chapter1 .
```

Once the build is complete run

```
$ docker run -p 3005:3005 fsbc/chapter1
```

Open your favorite web browser and visit `localhost:3005`. You will see a white page with the words 'Hello World!'. You've just created your first application! Press `CTRL + C` on your keyboard to end the local server.

Its working on our local computer but people on the web can't see it yet. We need to find a server to host our app or we can find a hosting provider to host our application. Since we don't know how to configure servers yet we are better off using a hosting provider / service.

Heroku is a great hosting service for web applications of different types. [Create a free account using their website](https://www.heroku.com/). Next install the command line interface (CLI) toolbelt for Heroku found [here](https://devcenter.heroku.com/articles/heroku-cli). This toolbelt will allow us to use the command line to push our application from our local computer to Heroku for hosting.

Open a terminal session, and `cd` to the root directory of you project. Use
```
$ heroku login
```
to login into your heroku account from the terminal. Now create a new heroku application.

```
$ heroku create
```
The name of your new application will be listed as `https://NAME.herokuapp.com` in the terminal. Now let's push or deploy our application to heroku.

```
$ git push heroku master
```
Now open your browser and visit `https://NAME.herokuapp.com` and you will see the message *Hello World* in your browser.
Anyone with an internet connection can now see your app when they visit your URL. Congratulations you've deployed your first application!

In the next chapter we are going to learn HTML and CSS to add more features to our simple application.
