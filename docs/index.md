# IXDS Web Class


## Mon 29-08-2016 - Session 3

<!--What is a function?? Explanation of functions. Whiteboarding functions-->
    
* Clone [special demonstration repository](https://github.com/josephfinlayson/learning-to-ajax) (working together). 
    * Write some HTML & CSS
        * Make it look a bit better
        * Create an image
        * Create a description
      
    * Write some javascript to create interactivity       
        * When you click the button log to the console
        * When you click the button log the input
        * Create a button that when click triggers the request to the guardian
        * Create an input when clicked searches the guardian for particular info
        
<!--* Set Computers up:
    * [NVM](https://github.com/creationix/nvm) 

* If we have extra time
    * [Meteor getting started](https://www.meteor.com/tutorials/blaze/creating-an-app)
    * What is an array??? Explanation of arrays. Whiteboarding arrays-->


#### Homework:

* Clone [special demonstration repository](https://github.com/josephfinlayson/learning-to-ajax) and open index.html in the browser, and the folder in sublime text. Look at `main.js` and `my-styles.css`
* Using guardian data, add more of it to the HTML page by modifying addArticleToPage function, (use the body field, and the trail text especially) 
for example, add a new line that says: `$('.main').append('<div>' + article.body + '</div>')` on line 15

* Do the [CSS exercises](https://www.codecademy.com/learn/make-a-website)
* Make the webpage look like a real article, that you see on the guardian. If you need extra divs to make it easier to style, you can write more complex jQuery to nest certain styles

```javascript

    $('.main').append(
    '<div class="my-article"> ' +
        '<h2 class="my-title">' + article.webTitle + '</h2>' +
        '<p>'+ article.body + '</p>' +
     '</div>')

```

* Add the styles to `my-styles.css`
* Extra credit: Read first 2 chapters of [Eloquent JavaScript](http://eloquentjavascript.net), and do exercises


## Mon 22-08-2016 - Session 2
In this session we will focus on jQuery

* Go over homework and any difficulties with the homework

#### Homework:

* [Command line familiarity lesson](https://www.codecademy.com/en/courses/learn-the-command-line/lessons/navigation/exercises/your-first-command?action=resume)
* [Tutorial for Git Commands](https://try.github.io/levels/1/challenges/1)
* [Introduction to JQuery (Unit 1 - 5 lessons)](https://www.codecademy.com/learn/jquery)
* [JavaScript exercises](https://www.codecademy.com/learn/javascript) 1-3 inclusive
 
 In this homework you might find the following particularly tricky:

* [complicated CSS selectors](https://www.codecademy.com/courses/web-beginner-en-GfjC6/0/3?curriculum_id=50a3fad8c7a770b5fd0007a1#)
* [what the hell is `this`?](https://www.codecademy.com/en/courses/web-beginner-en-GfjC6/1/5?curriculum_id=50a3fad8c7a770b5fd0007a1). Also talk abot `arguments`
* [Pay attention to CSS](https://www.codecademy.com/en/courses/web-beginner-en-v6phg/1/2?curriculum_id=50a3fad8c7a770b5fd0007a1)

Let me know if you have any difficulty!

## Mon 15-08-2016 - Session 1
In this session we will

* Introduction to each other
* Go over homework and any difficulties with the homework
* Set Computers up ---
    * Sign up and login to [GitHub](https://github.com/)
    * [Install Command Line tools on OSX](http://osxdaily.com/2014/02/12/install-command-line-tools-mac-os-x/) 
    * [Creating a secure key to access github](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/) -> select your operating system to see full details. (20 minutes)
* Learn how to use
    * the command line to 
        * create a directory called `www` 
        * create an `index.html` in the directory
        * Edit it using sublime text
    * Talk about HTML/JS/CSS - how they fit together
    * Git
        * Clone website, and add name to [here](https://github.com/josephfinlayson/coding_school_at_IXDS/blob/master/docs/lesson-1-website/index.html). 
    * Project ideas discssion
    * Lesson over

#### Homework:

* Launch sublime text from the terminal - for Mac users - might be good to ask someone at work to help :)
    * [launch sublime text from command line](http://olivierlacan.com/posts/launch-sublime-text-3-from-the-command-line/) for OSX computers
        `sudo ln -s /opt/sublime_text/sublime_text /usr/local/bin/subl` for linux computers

* Think about a project idea, add it to [here](https://github.com/josephfinlayson/coding_school_at_IXDS/blob/master/docs/lesson-1-website/index.html).  
* Read: [command line is scary](https://www.codecademy.com/blog/72)
* Do: 
    * [Command line familiarity lesson](https://www.codecademy.com/en/courses/learn-the-command-line/lessons/navigation/exercises/your-first-command?action=resume)
    * [Tutorial for Git Commands](https://try.github.io/levels/1/challenges/1)
    * [Introduction to JQuery (Unit 1 - 5 lessons)](https://www.codecademy.com/learn/jquery)

* Optional, if you think you might find git too hard, try using a client like [Git Kraken](https://www.gitkraken.com/) (crossplatform, looks new and fancy - watch the tutorial video, it helps!) [sourcetree](https://www.sourcetreeapp.com/) (old school, mac only)




## Session 0 - email
I'm really looking forward to having you in my class next Monday, and us working together learning how the code. You will learn how to build websites in HTML and CSS, and JavaScript over 3 months.

What's important is that the course will have a homework component, learning programming languages is like learning any language, you need to practice more than once a week to pick it up. This email contains three tasks that I would like you to do before the first lesson so that we all start on the same page, and for Ammar * 2, and Khaled, to refresh their memories

Tasks - please do before Monday 15th:

1. Download and install sublime text https://www.sublimetext.com/3 (10 minutes)
2. Download and install google chrome https://www.google.com/chrome/browser/desktop/  (10 minutes)
3. Complete the following courses on code academy (2 hours)

Website: https://www.codecademy.com/learn/web
What to study:
Unit 1: Introduction to HTML
Lesson: HTML Basics
Lesson: Build Your Own Webpage

Website: https://www.codecademy.com/learn/make-a-website
What to study:
Unit 1: Site Structure
Lesson: Site Structure

Let me know if you have any trouble / problems doing these tasks!


