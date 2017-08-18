# Chapter 0: Setup a development environment
The core components of writing web applications are an operating system and the terminal.

## What is a development environment?
To start your journey as a programmer you are going to need the right tools. These tools will allow you to run programs that perform the tasks you want completed. The first and most important tool is your computer.

A computer is made of many parts. All these parts fall into one of two categories: hardware or software. The hardware of the computer are the physical parts that make the computer do things. Some notable parts are called the CPU, Memory also known as RAM, motherboard, and display, what you look into when you use the computer. At the most basic level, a computer operates by reading a series of 0's and 1's and then flipping switches on the computer to create certain results based on the binary information the program provided. These pieces work to form the basic building blocks of a modern computer.

Software is a set of program files that contain the logic or set of instructions, that are to be run by the user (either you or the copmuter itself). The instructions are passed down to the physical hardware where the command is executed. The execution of these programs output a series of 0's and 1's that tell the physical hardware what switches to flip in order to make the computer give a specific output. 


## Windows Only: Install Linux
For windows users we are going to need to run a different operating system called linux on our computers. Linux is a free software. 

Lets download the a version of the linux operating systems called `Ubuntu` from this [page](https://www.ubuntu.com/downloads/desktop). You will see a `ubuntu.16.X.X-desktop-amdXX.iso` file somewhere in your downloads folder. We're going to use this in just a bit.



  
Download the virtualization software [Virtualbox](https://virtualbox.org/wiki/Downloads). Virtualbox allows us to run different operating system that are different from the ones we are currently using in a virtual environment. If this doesn't make sense now you'll understand as soon as the installation of Linux is finished. Run the Virtualbox installation program with all the default options. 


Click the new button, on the drop down choose `Linux` and `Ubuntu (XX-bit)`. The default bits on your computer wil be automatically detected. 

![new-vm-image-1](https://cdn.rawgit.com/nodox/fsbc-images/feat-dev/virtualbox-linux-installation/finals/final-p0-virtualbox-step1.png)

Notes: 
- Canvas layer: 1200x1000 (wxh) final size
- Figure layer: 1000x755*

![new-vm-image-1](https://cdn.rawgit.com/nodox/fsbc-images/feat-dev/virtualbox-linux-installation/finals/final-p0-virtualbox-step2.png)


Now will we see a second?




If not, visit this [Windows FAQ page](https://support.microsoft.com/en-us/help/15056/windows-7-32-64-bit-faq) to determine the number of bits on your CPU. 


Once created, click the ubuntu and then click settings up top. Go to `storage`, under `Controller: IDE` choose the empty CD slot. On the `Optical Drive`, choose the little CD picture and located the ubuntu.iso file we just downloaded. Start the Press ok and launch the ubuntu OS.


If you are confused please see this [tutorial](https://askubuntu.com/questions/710608/how-do-i-install-ubuntu-on-virtualbox-on-mac-os-x-el-capitan). Install ubuntu following the default options. 


When you are done and see the desktop, right click and press `Open Terminal`.


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








