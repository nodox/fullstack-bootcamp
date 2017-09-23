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

The purpose of hackernews is to provide links to interesting article over the web. Our first task will be to add a list of links to the page. As we mentioned earlier we are going to use a couple of HTML tags to create a few links in `views/index.html`.

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Title of the document</title>
  </head>
  <body>
    <div>
      <ul>
        <li><a href="https://google.com">The first link is to Google!</a></li>
        <li><a href="https://duckduckgo.com">Here is a second link: DuckDuckGo doesn't track searches</a></li>
        <li><a href="https://microsoft.com">Link number 3: Is Microsoft even relevant?</a></li>
        <li>This is not a link</li>
      </ul>
    </div>
  </body>
</html>


```

Save the file. In your terminal make sure you are in the root of the project. Type `node bin/www` to start your server. Go to your browser and visit `localhost:3000`. You should see 4 list items: three are clickable and the 4th on is not. Let's go back into the code. As you can see we added four new tags `<div>`, `<ul>`, `<li>` and `<a>`. The `<div>` tag is used to create division in our web page. These tags can accept plain text in them but they are commonly used to create divisions on the page with other tags inside of them. The divisions means we can target this small collections of tags for styling and animation (we will get to this in due time). Next we need to create the list of link tags that is where the `<ul>` and `<li>` tags come into play. The unorded list (`<ul>`) tag is responsible so creating an unordered list. To create list items you need to use `<li>` tags. (I hope you have realized how logical HTML was created to be.) In the `<li>` tag we can add text or additional tags to create more complex markup element that can have their own styles. Since we want to have a list of links we are going to introduce an anchor tag. The anchor tage (`<a>`) is used by specifying the location you want the person to go to once they click on the link. In between the opening and closing `<a>` tags is where you specify what text we want the user to see. You can see that each link goes to a different site on the web but we are responsible for telling the user something about the link they are about to click. The next component we needed was a navigation bar. We are going to use the navbar to show our logo, as well as the top links and new link however right now they will be links that lead to nowhere, we will create new pages for those links shortly. Notice that each of these elements gave an opening and closing tag and in between these tags is where you can add tags or other HTML tags to create compound HTML components. 

Save your changes in the file, and restart the server (go to terminal, press `CTRL-C` to close the session, and then run `node bin/www`. If you go to the browser and refresh the page you will see a list of links. The first three items are links that can go to different locations on the web.  The last item is not a link to demonstrate the different ways we can use our HTML elements. Now we need a navigation bar. Can you guess what tag we are going to use? You right, we gonna use a `<nav>` tag. Since we want to navigate to different part os our site we are going to use `a` tags as well. 

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Title of the document</title>
  </head>
  <body>
    <nav>
      <a href="">Top</a>
      <a href="">New</a>
    </nav>
    <div>
      <ul>
        <li><a href="https://google.com">The first link is to Google!</a></li>
        <li><a href="https://duckduckgo.com">Here is a second link: DuckDuckGo doesn't track searches</a></li>
        <li><a href="https://microsoft.com">Link number 3: Is Microsoft even relevant?</a></li>
        <li>This is not a link</li>
      </ul>
    </div>
  </body>
</html>

```

Save your file, restart your server and refresh google chrome. You will now see two links sitting next to each other. Sweet! The navbar seems to have a list of links, could we have used a unordered list tag with list items? Yes! We could absolutely do that as well. The way you implement these concept is completely in your control. What you will notice is that some tags have their own default styles. The unordered list shows each item added in a vertical list. The navbar links start exactly as the far left of the page and add each link directly next to each other left to right. If you wanted the same behavior for each tag then you would have to override the default styles using CSS (we all be using CSS to make our website beautiful).

Ok before we move forward. I got to confess I'm lazy (as are most programmers, and you will be too). I noticed that anytime we make a changes to our file and want to see the changes we have to restart the browser and refresh the browser. Thats mad work. Since we're software developers can we find a better way to do this? The answer is yes, and you guessed it we're going to use a tool that someone else created since they encountered the same problem. We are going to use a tool called `nodemon`. This cool little invention listens watches for use to save the file. Everytime we save the file the tool restart our server. Then all we have to do is refresh the browser. While its doesn't automate every development step to see new changes this is a good first step in building an automated workflow that allows us develope features much faster. Let's download our tool from the terminal. Open and new tab to download nodemon.

```
$ sudo npm install -g nodemon
``

Our command downloads and install `nodemon` from a website called `npm` that stores a bunch of developer made tools. The `-g` and options are called flags. Flags are used to specify how you want the results to be treated, almost every terminal command can accept a flag. In our case these flags specify that we want the nodemon package to be avaliable globally meaning that we can use nodemon any where in our computer which is helpful if we have multiple projects the require node servers. Now we can close out our server (if it's running) and run `nodemon bin/www` and anytime we save the file the server will automatically restart. Let's try it out. Start nodemon, delete the list item that is not a link, save the file and then refresh the browser. The browser will no longer have the 4th list item. You can see that you didn't have to restart the server because `nodemon` will be listening for changes. You can keep nodemon running while you are coding features and then shut it off once you are done coding (which should be nevver because now that you know how to code the world is your playground).



>>> Active Thoughts Todo
- [x] analyze hackernews and breakdown components
- [x] build a single hacker news link in html
- [x] add multiple links manually
- [x] introduce nodemon dev tool
- [] add users?
- [] switch to templating and loop through the collection
- [] add a form so you can post the links from the site and not the source code

>>> Writing workflow
 - develop and write?
 - develop with commits, then write off commits?
 - use commit messages and vim to write the book? Benefits is that the changes are directly highlighted so you have a better understanding of exactly what changes you introduced. (might be the best idea so that things stay in sync)

>>> Future Thoughts
- [] Heartbreaker / I'm quitting app

>>> Resources
- [the chapter project] https://vue-hn.now.sh/top/1
- [template language] ejs documentation
    - https://scotch.io/tutorials/use-ejs-to-template-your-node-application
- [washu as a guide] https://classes.engineering.wustl.edu/cse330/index.php/Module_1
- [ror tutorial as guide] https://www.railstutorial.org/book/beginning#sec-the_hello_application
- [the nerd ranch book for ios dev]




