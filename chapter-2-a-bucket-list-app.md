    # Chapter 2: A Hackernews 2.0 App
In this tutorial we are going to build a clone of the popular website Hackernews. Our app  will store a list of interesting articles on the web. We are going to learn two simple programming languages. HTML is used to set the structure of a web page. CSS is used style the web page and make it beautiful for our friends to see. Hackernews is pretty basic as it stands but since we're developers now we can bring the site into the twenthth century. Seriously reddit style website designs are so 1999.

First things first, in order to code we need a text editor. As we discovered earlier coding is nothing more than writing down instructions in a text file for the computer to interpret and execute tasks according to the commands. When you hear the term `text editor` you might make the connection to a program such as Microsoft Word or Pages on Mac. While yes you have the correct idea, you will have the most God awful experience writing code in a text editor that was not built for writing code (The only time you will code in such horrible conditions is when your trapped in a 1998 time loop or during a coding interview, seriously companyies will put you have you code under ridiculous contraist that you won't even encounter in daily work. If you're terrified good, we'll cover how to ace these interviews later in the book!). There are tons of other text editors such as Sublime Text and WebStorm. There are editors that live entirely in the terminal. Vim and Emacs are terminal based editor, fair warning, there is a holy war between these two editor communities so make your choice wisely as you will be grilled next time you go to a conference and tell all you friends you're a Vim addict. When you learn more about your preferred coding styles you can do investigate what editor is right for you. Now that I've sold you on the benefits of using a text editor designed to development, let's install one called Atom.

```
$ sudo add-apt-repository ppa:webupd8team/atom
$ sudo apt-get update
$ sudo apt-get install atom

```

We are now ready to write code. Initially I thought to slowly you introduce you to complex applications but let's be honest life isn't fair so I'm going to throw you right into the deep end and explain things as we go. First things first, we need to create a project structure for our applications. We can either spend a couple weeks trying to figure our what is the most optimized way to build out our project structure while in the process not getting any coding done or do what 99.9% of all other lazy programmers do: let someone else do the hard work and clone their project! Open your terminal application to clone a starter project from github.

```
$ git clone <NAME>
```

Let's explore the directory structure. Notice how the starter template gives a minimal skeleton of all the commonly used files and folders in a web application. If there are files we think are needed than we can create them to customize the project to our needs.

```
Picture of the directory structure or a table
```

To start working on our application we need to update the index view of our application. Typically labeled `index.html` this file is commonly used as the first webpage you see when you visit a web site. Now we need to find the index file, luckily our project structure is built to be easy to work with by using simple logic. The index file can be found in there views folder as `fsbc-chapter1/views/index.html`, since the index file is a file we `view` then its located in the `views` folder to find the index. (The `fsbc-chapter1/views/index.html` notation is called a path. Paths are used to show where files are located. The final name in a path with an extensions ending like `.html` is a file. Every name followed by a `/` is a folder or directory on the computer.)




>>> Active Thoughts
- build a single hacker news link in html
- add multiple links manually
- switch to templating and loop through the collection
- add a form so you can post the links from the site and not the source code





