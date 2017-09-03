# Chapter 0: Setup a development environment
The core components of writing web applications are an operating system and the terminal.

## What is a development environment?
To start your journey as a programmer you are going to need the right tools. These tools will allow you to run programs that perform the tasks you want completed. The first and most important tool is your computer.

A computer is made of many parts. All these parts fall into one of two categories: hardware or software. The hardware of the computer are the physical parts that make the computer do things. Some notable parts are called the CPU, Memory also known as RAM, motherboard, and display, what you look into when you use the computer. At the most basic level, a computer operates by reading a series of 0's and 1's and then flipping switches on the computer to create certain results based on the binary information the program provided. These pieces work to form the basic building blocks of a modern computer.

Software is a set of program files that contain the logic or set of instructions, that are to be run by the user (either you or the copmuter itself). The instructions are passed down to the physical hardware where the command is executed. The execution of these programs output a series of 0's and 1's that tell the physical hardware what switches to flip in order to make the computer give a specific output. 


## Development Environment Setup
To code we are going to need to run a different operating system called linux on our computers. Linux is a free software. Virtualbox allows us to virtually run operating systems that are different from the ones we are currently using. In this case we are going to use virtualbox to run linux on our computer. If this doesn't make sense now you'll understand when we finish the installation process. Download Virtualbox [here](https://virtualbox.org/wiki/Downloads) and start the application. 


## Setup virtual box with linux
Click the new button to create a virtual operating systems. 
![nvm-step1](https://cdn.rawgit.com/nodox/fsbc-images/feat-dev/virtualbox-linux-installation/finals/final-p0-step1.png)


We need to give a name to our virtual operating system. We are going to call it `Ubuntu` which is the name of a linux version we are going to install. Change the type to Linux, the version section should be automatically detected. Click on `Next` or continue, if you're not using windows.
![nvm-step2](https://cdn.rawgit.com/nodox/fsbc-images/feat-dev/virtualbox-linux-installation/finals/final-p0-step2.png)

Leave the memory size on the default setting. The more memory you give to Ubuntu the faster it will run. However when your run the Ubuntu and try to  work on your normal OS you might notice your computer running slower because your computer is sharing memory with Ubuntu. Click on `Next`.
![nvm-step3](https://cdn.rawgit.com/nodox/fsbc-images/feat-dev/virtualbox-linux-installation/finals/final-p0-step3.png)

Choose `Create a virtual hard disk now` to create the virtual instance of ubuntu. This option allows use to create a version on your computer without haveing to buy a brand new computer with the OS installed. Virtualbox shares the hardware on our computer with Ubuntu. Click `Next`.
![nvm-step4](https://cdn.rawgit.com/nodox/fsbc-images/feat-dev/virtualbox-linux-installation/finals/final-p0-step4.png)

Choose `VDI (Virtual Disk Image)`. We want Virtualbox  to load our operating system from a virtual disk. Click `Next`.
![nvm-step3](https://cdn.rawgit.com/nodox/fsbc-images/feat-dev/virtualbox-linux-installation/finals/final-p0-step5.png)

We want our data to be stored as we need more of therefore we need to select `Dynamically allocated` and click `Next`. 
![nvm-step3](https://cdn.rawgit.com/nodox/fsbc-images/feat-dev/virtualbox-linux-installation/finals/final-p0-step6.png)








on the drop down choose `Linux` and `Ubuntu (XX-bit)`. The default bits on your computer wil be automatically detected. 




Lets download the a version of the linux operating systems called `Ubuntu` from this [page](https://www.ubuntu.com/downloads/desktop). You will see a `ubuntu.16.X.X-desktop-amdXX.iso` file somewhere in your downloads folder. We're going to use this in just a bit.









If not, visit this [Windows FAQ page](https://support.microsoft.com/en-us/help/15056/windows-7-32-64-bit-faq) to determine the number of bits on your CPU. 







## Fun with the terminal
The command line, also know as the terminal, is an application that allows us to interact with the computer by typing commands with our keyboard. When we type those commands and press enter, the computer works to complete the command. Every thing we do with a mouse can be done using commands. The terminal however is sometimes better than using a mouse because it gives us more control over the computer.

You can think of the terminal as driving a stick shift car. When driving stick you get more control of the car but you need to understand how the car works to make sure you are shifting correctly. Incorrect shifting will cause the car to turn off or worse, you could damage the clutch. The same concept applies with the terminal. With more control means we can issue better commands to complete more tasks but we need to make sure we don't issue commands that can harm the computer. 
 
Each operating system calls the command line by different names. On Mac, `Terminal` or `Terminal.app` is an application to access the command line. Terminal comes preinstalled on all Mac computers. To find the terminal program you can search using macOS search or you can follow these steps: `Finder > Applications > Utilities > Terminal.app`. On Windows, the `command prompt` interacts with the command line. However this windows application will not be powerful enough for us to complete our projects so we need to install a better application to access the command line.


The terminal has many tools that are not useable when we use the computer with our mouse. Here is a fun exercise, do you remember what day of the week you were born? If you do you have great memory! If you are like the rest of us you might not remember. However with the terminal you can find the answer in seconds. Open up your terminal and type everything after the `$` sign.

```
$ cal 1993
```

This commands lets us see what the calendar looks like for the year `1993`. Instantly we can find the day we were born. Even if you don't learn how to code professionally, learning even how to use the terminal for very simple tasks can make you extremely productive in your daily life. 

Install terminal or a command line equivalent onto your computer. For PC/Windows users I recommend you use Gitbash or the linus subsystem if you are running windows 10.








