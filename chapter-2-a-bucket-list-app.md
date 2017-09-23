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

To start working on our application we need to update the index view of our application. Typically labeled `index.html` this file is commonly used as the first webpage you see when you visit a web site. Now we need to find the index file, luckily our project structure is built to be easy to work with by using simple logic. The index file can be found in there views folder as `fsbc-chapter1/views/index.html`, since the index file is a file we `view` then its located in the `views` folder to find the index. (The `fsbc-chapter1/views/index.html` notation is called a path. Paths are used to show where files are located. The final name in a path with an extensions ending like `.html` is a file. Every name followed by a `/` is a folder or directory on the computer.) Double click the file to open it for editing in atom. In front of you is a bare bones example for a web page. HTML is a markup language used to `markup` a file in a manner that a web browser like Chrome, the only relevant web browser on the earth, can read your file and return a web page. The HTML language is made up of tags that you wrap around content. Some tags are used to markup information for the final end user, then there are other tags that are used only for Chrome to read that are called `meta` tags. Every web needs a `<!DOCTYPE html>` which tells the browser what version of HTML to use, here we are specifing HTML5. The whole page is then wrapped in `<html>...</html>` tags to denote we are working with an html document. Notice how our content is in between the opening and closing tags. After we create the html document we need two divide our web page using the `head` and `body` tags. The `head` tag is another meta tag. Here we specify behaviors we want the Chrome to obey. The `title` tag is used to tell chrome what name to put at the top of the browser or on a tab. Open the browser to verify they say the same things. The `body` tag is responsible for the actual content you see in a web page. When you are on a website, every section, image, or link is found within the body tag. When we first opened how web page we saw the message 'Hello World!' which is right there wrapped in `p` tags. The `p` tag stands for paragraph. Many if not all HTML tags are named logically so its easy for you to remember what they do. The tags are used to give the page semantic meaning so that when you read the code you know what the page will look like in your head. A `p` tags means you can expect a long string of text. A `img` tag means you will see an image on the page. 

Ok if you haven't done so already go visit the hackernews site (https://news.ycombinator.com/). We are going to build a much better version for this ugly website. I mean come on we are in 2017, and we're still building websites as with not beautiful colors and effects. The final product can be found at https://vue-hn.now.sh/top/1. Yes, when we are done we are going to have built something you can have pride in when showing your friends and family. To begin the building process let's take a moment to analyze the webpage and identify the key html tags of the website. As a software engineer you need view software not as a final product but rather as the sum of a bunch of smaller working components. On this site we see a long list or a table so we can assume we'll use `table` or `ul` (unordered list) tags. We also see a bunch of links so we will need to use `a` (anchor) tags to create links. In the top I see a navigation bar with link to different page on the site therefore we will need to use `nav` and `a` tags. These small components are responsible for most of the so we now have a good idea of how to start creating our hackernews clone. Software engineering is about thinking how software is created and used. When you get a job as a software engineer you will realize most of you're time will be spent thinking what is the best way to accomplish something and what will be the implications of my choices. All these thoughts will happen before you even write down in piece of code.

The purpose of hackernews is to link to interesting article over the web therefore our first task will be to add links to the page. 




>>> Active Thoughts Todo
- [x] analyze hackernews and breakdown components
- [] build a single hacker news link in html
- [] add multiple links manually
- [] switch to templating and loop through the collection
- [] add a form so you can post the links from the site and not the source code

>>> Future Thoughts
- [] Heartbreaker / I'm quitting app

>>> Resources
- [the chapter project] https://vue-hn.now.sh/top/1
- [template language] ejs documentation
    - https://scotch.io/tutorials/use-ejs-to-template-your-node-application
- [washu as a guide] https://classes.engineering.wustl.edu/cse330/index.php/Module_1
- [ror tutorial as guide] https://www.railstutorial.org/book/beginning#sec-the_hello_application




