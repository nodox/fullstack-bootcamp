# Chapter 1: Launching your first application
Our goal for this chapter is to deploy a simple application that has the words *Hello World* on a while web page. As we work our way through creating our application we will setup finally answer your question of *What is coding?*, create a development environment where you can code, explore our first simple programming languages: HTML and CSS. Finally we will end the chapter by putting or deploying our application to a public website you can show anybody on the web. Let's get started.

## What is coding?
*What is coding?* Coding is the act of writing a bunch of commands in a text file and then giving it to the computer for the computer to perform those commands. The commands you write on the text file is called code. When you are opening files, creating folders, downloading ebooks or doing anything with our computer we are coding. However we aren't considered coders because the actions we performed have already been written for us. We are merely interacting with the code, that was written by someone else, and the computers or the persons code is responding to all the actions we are performing on the computer. 

## Getting to know your tools
To start you're journey as a coder or programmer you are going to need the right tools. There tools will allow you to run programs that perform the tasks you want completed. The first and most important tool is your computer.

### The computer and operating system
A computer is made of many parts. All these parts are parts can fall into one of two categories: hardware or software. The hardware of the computer are the physical parts that make the computer do things. Some notable parts are called the CPU, Memory also known as RAM, motherboard, and display, what you look into when you use the computer. These piece work to form the basic building blocks of a modern computer. Each piece has a set of instructions that can be called to perform a certain task but the hardware does not issue these tasks they only execute the task when they receive an order. 

Software is a set of program files that contain the logic or set of instructions, that are to be run by the user (either you or the copmuter itself). The instructions are passed down to the physical hardware where the command is executed to give a result. 

### What is the command line?
The command line is an application that allows us to interact with the computer by typing commands with our keyboard. When we type those commands and press enter, the computer works to complete the command. Every thing we do with a mouse can be done using terminal commands. The terminal however is sometimes better than using a mouse or what we see in front of use because it gives us more control over the computer. On Mac the command line application is called Terminal.

You can think of the terminal as driving an stick shift car. When driving stick you get more control of the car but you need to understand how the car works to make sure you are shifting correctly not breaking a gear in your car. The same concept applies with the terminal. With more control means we can issue better commands but we need to make sure we don't issue commands that can harm the computer. 

The terminal has many tools that are not normally useable when we use the computer with our mouse. Here is a fun exercise, do you remember what day of the week you were born? If you do you have great memory! If you are like the rest of us you might not remember however with the terminal you can find the answer in seconds. Open up your terminal and type

```
$ cal 1993
```

This commands lets us see what the calendar looks like for the year 1993. Instantly we can find the day we were born. Even if you don't learn how to code professionally learning even how to use the terminal for very simple things can make you extremely productive in your daily life. **Note: add more content about terminal commands, other fun exercises.**

### Setting up our development environment
To start coding we are going to need a development environment. The purpose of a development environment is to develop code. There are other environments that are used to test applications or see how they will behave once they are deployed live, these are commonly called test and production.

Our development environment will be created using a tool called Docker. Docker is a software tool that allows us to container our application in an operating environmnet that is different from our personal computer. Why do we want to do this? When you finally deploy an application you will need to deploy it to a server. The server is responsible for _serving_ your application to anybody on the web that visits the URL of that app. These servers also have there own opertation systems and they primarily use different variations of Linux. To avoid nasty errors because our personal computer environment  is not the same, we try to make our personal environment identical to the server environment. 

Since every computer has its own personality and different set of settings then we can avoid the headache of having to errors in our application caused by the different settings on both computers. As you begin to create applications you will often run into a scenario where the application runs fine on your computer but not on the server. This can be avoided by using Docker.

#### Download Docker
Docker is a publicly available software tool. Navigate to docker website, find the community edition and install the latest version of docker. [Follow this link to the downloads page.](https://www.docker.com/community-edition) Choose the package that fits our computer. Once installed start up docker. You should see the small whale icon in your tool bar.

#### Github and Git
Github is a web application used to store our applications code on the cloud. If the computer we use to develop becomes unuseable and needs to be replaced we can rest easy knowing our application files are safetly stored in another location. Github also gives us the power of version control. Version control is a way to visualize the different states of your applications. To create different application states we use a tool called Git. When we finish fixing a bug or creating a new application features, we use Git to create a snapshot of the current application state. Once the snapshot is created the snapshot is pushed to Github where we can easily view the different versions of our application. This would be the equivalent to writing a long paper and saving your work along the way. Once the work is in a state that you are satisfied with you create a backup and push the document to a remote place like Google drive, iCloud or Dropbox.

*Create an account with Github* (or Bitbucket since its free). We will use our account to get a copy of the sample application we will be deploying for our friends to see.




#### Get a sample application
Now that we have Docker running we need an application to develop. 

Instead of starting from scratch we are going to extend a simple application prebuilt for deployment. 







-----------




## What is a web page?
* Talk about the DOM and components of a web page
A web page is a document prepared to be read by a web browser so it can display the content of the page on the web. 


## What is HTML?
A website is made up of a page or formally known as a document. To put information a website you need to 
markup the page with a markup language, thats where HTML comes into play. **What is html?** 

The `div` is the most common element on the page and its used to divide the page. The division helps us markup the page differently based on what we want to achieve. 

## What is CSS ?
Markup is great but its so plain. What if we wanted to style the page with different colors so its not so plain? Or what if we wanted to style the actual markup elements, thats were CSS comes in. **What is CSS? Why called CSS?**. CSS is a design language used to describe how HTML elements are displayed to end users however they are being viewed (mobile, desktop, paper or other media).

## What is Javascript?
We've added the HTML elements and styled it with CSS. But our website looks real plain. I wonder if we can make it more lively. And the answer to that question is yes we can if we use Javascript. Javascript the the most popular web language today. Javascript is responsible for the way things interact on the web page. When you click a button, see a popup, or moving element then you are watching javascript code doing things to the web page. Let's make our page do something more interesting. We added the time we updated the website in markup but its been a while since, let's add a timer on our web page so we can see our page update live. To use javascript we are going to use a script element to run code. **What is a script?** Copy the following script just before the ending body tag.

...

Now reload the page. Our webpage now has a live timer. Sweet! There is so much you can do with javascript as a programming language. 


## What is a programming language?
HTML and CSS are light versions of programming language becuase they are so simple in their design. They server primarily as a presentation layer for the content you want to describe. Javascript is the first major programming language we are going to cover. We are learning a new language we have to learn a few fundamental concepts once you learn these ideas you will be able to any programming language out there. 

The reasons is because these languages all revolve around talking with a computer what we say to the computer has to be that same with each language but how we say it can be written in many ways as long as the fundmanetals are there. Take a moment to complete the [tutorial here](https://www.w3schools.com/js/default.asp) to understand the syntax of javascript.

**Note: Write the book as a giant reference manual? Would be too long a book to talk about programming fundamentals such as variables and loops.**