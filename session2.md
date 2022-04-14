# Session 2 Notes


This session, we covered various aspects of Visual Studio Code, with a brief look at some Python code at the end of class. Below, I'll be writing up notes about the topics we talked about, as well as some extra research material you might find helpful.
For this week's terms, you'll want to consult the glossary, which has been updated with secttions for both VS Code, as well as the few Python concepts that were covered.

## Miscellaneous Odds and Ends

* Discord: As of this week, the course has a Discord server. Have a look at the Discord page, reachable from the main page, to learn more.
* Inaccessible link texts: A few of you have noticed my sneakily inserted inaccessible link texts like "Here" or "this link". They are there for a reason; it's a practice we unfortunately come across quite a bit more often than we should in documentation on all sorts of topics, so it's good to get into the habit of reading the surrounding sentence where these are concerned. I don't like it any more than anybody else, but this is a sandbox where we can teach ourselves these habits to lower the threshold for using mainstream resources with as little friction as we can.
* Structure of the class: I consider the sessions an introduction, the notes a way to learn more, and the assignments as well as your own questions and research the way to cement what you've learned. In that sense, it's actually pretty similar to a college course. Just ...without the deadlines, grouchy teachers and missing accessible materials, that is.
Having said that, no question is a stupid question and every skill level is meant to succeed here. So please make yourself be heard if you get stuck, that's what we are here for.


## Visual Studio Code
### Just what is this thing?

[Visual Studio Code](https://code.visualstudio.com) is an open-source code editor\* made by Microsoft. It shares a name with [Microsoft Visual Studio](https://visualstudio.com), which is an Integrated Development Environment or IDE\* for short.
Whereas Visual Studio has existed for about 25 years, VS Code is more of a new kid on the block that took the internet by storm over the last 8 or so years. So how do they differ?


We can draw a parallel to a couple other similar Davids and Goliaths out there to make a comparison. At its most basic form, VS Code would be to Visual Studio what Notepad is to Microsoft Word, Reaper\* to ProTools\* etc.


That is to say, Visual Studio gives you thousands of features in an enormously large package that let you do a whole lot of different things, from building desktop applications to websites to mobile applications. The program is quite heavy, has a serious learning curve and needs at times dozens of gigabytes of storage. While it is mostly accessible, I would recommend using JAWS with it at this time, as NVDA tends to lag pretty heavily even on powerful hardware.


Visual Studio Code, in comparison, is just an editor. You can edit text with it, in fact, I am writing these notes in it right now. But it's versatility comes in when it's paired with extensions, which are essentially bits of extra functionality you can add to the program as you need them. This way, when you add new features, you know where they came from and have a far easier time learning how to best use them.


Another difference between these two is the method with which they were built. Visual Studio, the big one, is a native application written for , initially, Windows, and it's only a few years that a Mac version has existed and is being actively developed. I don't think the two versions have reached feature perity\* yet.


Visual Studio Code, on the other hand, is written using a technology called [Electron](https://electronjs.org), which is a technology that allows you to write cross-platform\* applications using languages normally used for web development: HTML, CSS and JavaScript.

This is a tool a lot of modern applications (Spotify, Discord, Skype, Slack etc.) use to write the majority of their application once, and run it on Mac OS, Windows, Linux and the web, saving a huge amount of costs and time.


Conversely, it allows projects on the web to make use of code used in Electron-based applications with relatively few modifications. The editor component of VS Code, for example, is called [Monaco Editor](https://microsoft.github.io/monaco-editor/) and is used in quite a few other applications, primarily ones on the web. We'll encounter a few in the coding resources section below.


I could describe what the VS Code interface looks like in my own words, but [a fellow screen reader user has done a fantastic job doing this already](https://lifeinsixdots.com/visual-studio-code-with-a-screen-reader/). This person goes by LifeInSixDots on various social media, and I highly recommend keeping an eye on their blog, as the content they create is top-notch.


See what I just did? I embedded a third-party article into these notes, and by doing so, I am taking a risk. The article might go down, it might change, but for the moment it suits my needs beautifully, so I'm adding it to my project, crediting the original author. I asked them for permission to include links to their efforts in these notes beforehand.


This is very similar to how projects , particularly open-source ones, will stand on the shoulders of giants and include prebuilt components into their application, focusing on the parts that make their project unique. While that can be good for us, for example in the case of the Monaco Editor mentioned above, it can also be a problem if an author uses a component that is inaccessible. We now have to hunt down the person who made the component, rather than the creator of the app, to try to get them to make it accessible, which in turn might benefit other projects that use that same component if the author were to do so. This is very much a double-edged sword.


For this class, you were meant to install both Visual Studio Code, as well as the Python Interpreter. If you've done that, all that is currently missing from allowing you to use Python in VS Code is the so-called Python Extension, which leads me to one of VS Code's core strenghths.


### Extensions


Much like a browser you can install add-ons into in order to teach it new tricks, VS Code lets you install extensions in order to augment its functionality. By doing this, you can make it work with different programming languages, frameworks and other such things. You can also make it do things that don't necessarily have anything to do with Coding. I, for example, use a VS Code extension called [dendron](https://dendron.so) for my notetaking solution for all sorts of things. It's , to me at least, very pleasant to use. Other examples are integrations with Spotify or Discord, extensions to work with Git and GitHub, and the list gets larger and more varied every single day.


The big question is of course, do we need any extensions to make VS Code work well with screen readers. The answer is no, not really, not on Windows, in any case. On the Mac, I recommend picking up the extension "Indent Report" by Oriol Gomez, which lets you hear sound effects based on your indentation level. This is important to be aware of, and the new audio cues feature does not cover this yet.


On the screen reader side, you will want to enable indentation reporting if it supports it. In NVDA, this is in "Document Formatting" and in JAWS, this can be done from the Sound Scheme manager, which I am pretty sure the previous article already eluded to. Again on the NVDA side, there is [a VS Code NVDA add-on](https://www.nvda-addons.org/addon.php?id=128) which helps a bit with keeping the chatter down, as well as a few other fixes. Unfortunately, this addon hasn't seen an update in some time, so it's future is somewhat uncertain at this moment.


Setting your screen reader up for coding is a somewhat personal thing; I for example have speech dictionary entries to shorten punctuation symbols somewhat but others hate this approach. I can really only say: go forth and experiment.


### Setting up VS Code for Python Development


There is another article by LifeInSixDots that goes over this, but it deviates from our path somewhat so I will write my own. If this article were to be on GitHub, I could decide to fork the repository and give my own spin on the content while still crediting the author, just to look back at last week's material. :)


We've learned a thing or two about VS Code from the lecture and the article linked above, so with that knowledge, let's see if we can't get VS Code and Python to talk to one another.


1. Open Vs Code, it doesn't matter what file is open.
2. Once you're in the editor, press shift+ctrl+x to bring up the Extensions view.
3. In the search field, type "Python" without the quotes.
4. Pressing tab at this point will take you into a list of results. Do so, press down arrow to highlight "Python 2022.2" from Microsoft. Please note, future readers, that this number may have changed.
5. Pressing tab again takes you to an Install button. Give it a whack.
6. Wait for your screen reader to tell you installation was finished, then close VS Code entirely, making sure all its windows are closed.
7. Open VS Code up again and create a new file, hello.py. You can do this either from the commandline by using "code hello.py", or by opening it from the start menu and saving the resulting new file as hello.py.
8. At this point, you may or may not get a message about Python not knowing where your interpreter is. We'll fix that next.
9. Hit f1, and without deleting the > sign that is already there, type "select int".  An autocompletion list will open with "Python: Select Interpreter" highlighted. This is an autocomplete list that filters as you type. Please note that you will not be able to arrow left and right to revisit your input at this point.
10. Press enter on this option. A new list will open with several options in it.  select the option that points to the Python installation you installed for this class. Usually, at this point, there would only be one option here that has an actual path (e.g. c:\python) in it. Hit it.


At this point, you will be all set. If you were to now type "imp" in the editor, autosuggestions will pop up with you can accept with enter and dismiss with escape. Please note that your cursor does not move when these come up; you're still in the editor typing and the list filters as you type, you just can't see what you're typing directly until the list is dismissed one way or another.

## Python
### About the examples in the lecture


The error audio cues you hear on the recording will, at this point, not trigger for you if you do the exact same thing I did. This is because we have not yet set up linting\*, something we will cover next week, as it involves a python mechanism called pip\* that we have not covered in class yet.
The code I was playing with in the editor was the following:

```Python
import os
import time
```


What exactly these lines do is something we will cover in class next week as wwell.


### REPL: Read, Evaluate, Print, Loop


The REPL is an invaluable tool when learning Python, but also to test new code line by line before you add it to a working program. It can allow you to essentially play in a sandboxed environment and inspect what any line of code you're intending to use will do. It does this according to the following flow:

- Read: Python will read the line of code you entered.
- Evaluate: Python will run the line you entered.
- Print: Python will output the result of the line you entered, if there is anything to output.
- Loop: Python goes back to the start of the flow and waits for a new line from you.


To enter the REPL, you can run "python" from the commandline, without any further arguments or switches. You will get some output, followed by a line prompting for a line of code. This prompt looks like ">>>".
The code I was noodling with in class is the following. Please note that anything following a number sign (#) is a comment, a note to you, not a piece of Python code.

```Python
"hello" # Make a string\* with the word hello in it, and immediately discard it again
my_string = "Hello" # create a variable\* with the string "Hello" in it. This outputs nothing.
my_string # Ask Python for the value of my_string. This will print hello, as my_string is now the way for us to refer to the string "hello"
len(my_string) # the len function\* returns\* the length of the piece of data you give it. In this case, we give it the string hello, which is 5 characters long. Therefore, this line outputs 5.
my_string*30 # the * here is just like in math, the multiplication symbol. This will print hello 30 times stitched together without spaces. Why do you think there's no spaces?
```


For many of you, this is your first real exposure to programming code. And that is completely ok. You don't have to understand this yet. Throughout the next sessions, we will dive into several more topics, including programming, some more git, as well as how to find and successfully use third-party resources.
And speaking of resources, I did promise you some :)


### Coding Resources


- [FreeCodeCamp](https://freecodecamp.com): If you're looking to learn web development, you can't really do better than this resource, it starts you from absolute zero and takes you all the way to competent if you stick with it through interactive exercises that use the Monaco Editor.
- [Codecademy](https://codecademy.com): Similar to FreeCodeCamp although not all courses are free. As a pro, they have courses on quite a wide variety of topics. They are somewhat pricy though.
- [Educative.io](https://educative.io): A somewhat lesser known course provider that has some pretty good content as well. Uses the Monaco Editor for the interactive parts.
- [Automate the Boring stuff with Python](https://automatetheboringstuff.com): A book on learning Python. Free to read and might give some inspiration on what you could use Python for in your dayjob or daily life.
- [The Odin Project](https://theodinproject.com): Very comprehensive webdev curriculum; covers HTML, CSS, JavaScript and Ruby on Rails
- [HTML dog](https://htmldog.com): Another resource on HTML and friends, less interactive and more text-heavy.
- [Python for You and Me](https://pymbook.readthedocs.io/en/latest/): A free textbook on Python that takes you, when all is said and done, through making a small web application in Flask. Psst: we might cover Flask in the next course!

Check back here from time to time, as I might think of others throughout the week. I will announce if I make significant additions to this one on both Discord and Slido.



## Homework

Create yourself an account on GitHub. Reread the session 1 notes and ask all the questions you have regarding git, as we'll have a brief segment next week revisiting some of the concepts you may have struggled with before.
Experiment with the REPL, and make sure you have your VS Code set up for Python as described above. That, as they say, is all.

