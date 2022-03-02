# Session 1 Notes

In session 1, we went over several different topics that will be summarized below. Where possible, extra resources wwill be provided to learn more about the topics covered.


Among other things, a whole slew of terminology was introduced, which may have been overwhelming for some of you. The Glossary, linked in the top menu, has definitions for terms you may hear a lot, grouped by topic. Terms included in the Glossary are denoted by an asterisk (*) next to their first occurrence in other pages.


## Miscellaneous Admin things
* The class teaches you how to code, but also teaches you how to learn how to code, by covering the tools and techniques you will be expected to be familiar with when looking at mainstream resources, as that is a far more valuable skill.
* Questions are, at least for now, asked on the Slido, linked in the top menu. Neither party will be notified about new content on Slido, so check back in a couple hours, as I check it rather frequently.
* If you need a more direct avenue of communication, you can find ways to contact me in the Contact page linked in the top menu.
* Emails are generally going out regarding preparation instructions for the next session, as well as notifications about the recordings being available. In general, the recordings go up on the APH Youtube channel, in a dedicated playlist for this class.
* Questions during class are best written down for yourself as soon as you have them, as I can only cover so many which means your question might get missed. If that happens, definitely ask it on Slido.
* No prior experience apart from a good grasp of your screen reader's capabilities is assumed. Complete beginners are welcome, and are encouraged to ask all the questions they have while going through the course. Please note that my time is limited, and therefore asking on Slido is a good way to ensure your question gets answered in textual form. Should you need more help than that, shoot me an email and we'll see what we can do.

## Commandline
### Summary

The commandline, also referred to as terminal by some operating systems*, is a text-only way to interact with your computer. In that sense, it's very similar to MUD* games or old-style text adventures.


To open a commandline window on Windows, a quick way to get there is through the Run dialog, which is invoked with the keystroke windows+r. Typing cmd, followed by enter, will bring up the commandline window.


Please note that on Windows, there's several ways to get a commandline window to show up, namely cmd, powershell and the somewhat new Windows Terminal. These are functionally equivalent for our purposes; it does not matter which one you use.
The same goes for Bash*, ZSH* and other such shells* on the mac. They only differ in advanced functionality we won't be touching in this course.


When you enter a command, your computer will look through a series of folders to see if a program with that name can be found. If so, the command is run. If not, you will get an error indicating the command was not found, or not recognized in the case of Windows.
This series of folders is stored in the computer's environment variables* in this case the PATH variable.


If the command is recognized, odds are it's going to need more input to work for you. It may for example need to know what file to operate on. These extra bits of information are referred to as arguments to the command, and will be referred to like this in a command's help output.
Commands may have subcommands when they are particularly involved, which directly follow the main command before anything else. Git, for example, has quite a few of them.


There may also be ways you can influence the command's operation before it runs. You may, for example, want to list all files in a folder, but sorted in reverse chronological order.


In that case, the command you're using can be influenced using a special kind of argument known as a switch, or an option. These generally take the form of either a dash or a slash followed by a letter or word. This concept is very powerful and at times makes doing things from the commandline faster than doing it from a regular GUI* application.


An example of this would be the copy command in Windows. I can type "copy file_1 file_2", where file_1 and file_2 are paths to files on my system. 

The first file is the file I want to copy, the source. The second path is where I'd like to copy the file to, the destination.
At this point, if I was going to overwrite the file in the destination, because the file already exists in that destination folder, I would get a prompt asking me if I want to replace the existing file.


If, instead of "copy file_1 file_2" I were to do "copy /y file_1 file_2", I am preemptively telling it to not even ask and to just go ahead and replace the file if it's encountered.
Now, something for you to think about: apart from convenience, why might I not want that question to come up?

### Reviewing commandline output

Some of you may have noticed that you can't use the up and down arrow keys to review the output of the commands you type. This happens because those keys serve a different purpose in this environment.

The arrow keys let you look at previously entered commands and re-run them, should you want to. To review your output, you will have to use either the JAWS cursor or NVDA's flat review keys. I'm afraid that details on how to do this is somewhat outside the scope of this course; your screen reader has fantastic documentation people put a lot of work into. Go read it :)


### Resources

The commandline is very powerful, but can also be a rabbit hole the size of Texas to get lost in. If you understand the summary above, that is more than enough to follow along with the course for the rest.
Having said that, though, I can point out some resources for those who would like to know more.
On Windows, [this](https://red-dot-geek.com/basic-windows-command-prompt-commands/) is a pretty good discussion on the most common commands.
For Linux, and to a large degree Mac oS, I can recommend [Linux Journey](https://linuxjourney.com) as a pretty accessible way to get used to the terminal.

## Git
### Summary

Git is a very powerful, but also rather abstract and at times infuriating piece of software.  It's main function is to keep track of changes to files over time, similar to how you can look at different versions of a file on Dropbox.

Git essentially takes that functionality and blasts it into the stratosphere. This is why developers the world over use it to keep their code safe from inadvertent mistakes and regressions.


Before you can use git, you need to initialize a repository* or repo for short in the folder you want to work in. You do this using the "git init' command.

After you've done that, the basic idea of Git works like this:

* First, you change one or more files, just by working on them. At this point, running "git status" will tell you there are untracked changes present.
* Next, you add the changes to a kind of staging area. This extra step is here because you may not always want to snapshot all your changes, maybe just some of them, or even just one single file. You do this by using the "git add" command, with the file or folder in question as it's argument.
* Finally, you commit your changes. This is akin to making a snapshot f the project at that point in time, one you can always come back to should you need to. For this, you use the "git commit" command, generally using the -m switch followed by a commit message in quotes. Something like: git commit -m "Fixed typo".

At this point, this version of the project is saved and retrievable. If you're with me so far, you're good to go for most of the course.

Git can do more than just this, though. In what's known as a branch*, you essentially tell Git to still keep track of the changes you make, but in a different ...well ...branch, a branching path from the main road as it were. You may or may not come back to the main road at some point, but for now you just want to work on something without it affecting the main road, in such a way that you can instantly switch back and forth between the main road and your branching path.
Changes in a branch are isolated from the main road and vice versa, they have a shared starting point but that is all they have in common. Once you are done with your branch, you can perform a merge*, which tries to integrate the changes you made into your branch back into the main road. At this point, the main road would be affected by your branch, and if the merge succeeds, your branch is no longer required and can safely be deleted.
In a developer team, if you are working on a new feature, you would do this in a branch. That way, you can work on the feature without breaking the product you're working on, even ush* your changes online and have your colleagues look at them, and only merge them into the main product once you're sure everything works. More on that below.

### Resources

Git can ...honestly be a bit of a git to get used to :) If after this you still have questions, obviously you can share them, but a good discussion that goes more in-depth can be found [here](https://www.w3schools.com/git/).

## Github
### Summary
So far, everything we've done on git has been local to our own machine, apart from a few hints here and there that this is not the only way you can use it.


Github, as well as other platforms like Gitlab and Bitbucket, are hosting providers for your git repos. They allow you to send your code to the cloud in various ways, either for backup, sharing or collaborating purposes.


Github in particular is very popular and is used by a lot of open-source initiatives like the NVDA screen reader to do their development out in the open and allow anyone to contribute to the project if they have the expertise to do so. It also allows anyone to download the source code* of the project to inspect, play with or learn from.


In fact, the code for this very website is on Github. It's just a few markdown files, but still, it's up there and can be found [here](https://github.com/zersiax/zersiax.github.io).

Finally, it allows projects to track various aspects of the project. Things like documentation, contributing guidelines and user-facing issues can all be handled on Github. 

Indeed, one of the first things I'd recommend you do when encountering a problem in an open-source* project is to file an issue* with that project so the maintainers are aware of it. This, far more than posting to forums or social media, will get it to the right people and give them a way to discuss the problem both among themselves as well as with you and other users.

To fully understand where Github comes in, we need to add a few tools to the list of things git can do, namely the following:

* Clone: a git clone retrieves the entire project from git in its current state. If you just want the code to look at, uild or inspect, this is what you would do first.
* Push: A git push sends the changes in your current branch that have not been uploaded yet to the remote host*, in this case Github.
* pull: The opposite of push. A git pull retrieves the latest changes from the remote host and integrates them into your local version of that same branch. You would do this, for example, if you are working on a branch together with someone else to see what the other person changed and stay on the same page.

With these three extra actions, we can see how Github literally becomes a hub for people working on projects using git.

### Pull Requests

In class, I brought up the example of adding a feature to NVDA. 

Like I stated above, Github lets anyone who has the expertise lend their help to a project, and this would normally happen through a pull request. For the sake of simplicity, we're going to assume the person has access to push branches to the repo directly; this is often not the case but we'll get to that in the section on Forking below.

In class we used the example of making NVDA available in Klingon*. You woke up with this brilliant idea, cloned the git repo to your computer, made a new branch and got to work.


After a while, you run into a snag you need a bit of help with. Because you made a branch first, you can safely push your branch to the remote host and have someone else take a look. 


Rather than telling you what the problem was, they were on their development machine anyway so they pulled down your branch, made a few changes and pushed them back up, letting you know to pull their changes so you can see them on your local machine.


This is exactly what you needed and you continue on, finally finishing your work and pushing the final changes to your branch. Now what?

Generally, only certain people on a repository on Github or similar platforms have the permissions to merge in new code. If that wasn't the case, things would rapidly devolve into chaos. So at this point, you create what is known as a pull request. You essentially request the maintainers of the project to "pull in" the changes you made On some platforms this is referred to as a "merge request".

You do this from the Github page of the project and it involves selecting the main or master branch as the "base", and your new branch as the one that needs to be pulled in.

At this point, the pull request is created and allows maintainers to see your changes, review them and discuss them. Because you are all master coders, there's nothing more that needs to be done and your pull request is accepted, after which you are thanked for your contribution and your changes are merged into NVDA. Awesome, you've just created something a bunch of people will use.


### Forking

Forking is the final topic we'll highlight for now, as it may come up, and who knows, maybe you're just curious what the term refers to.

A fork is in some ways similar to a branch. When you fork a repository on Github, you essentially make a copy of that entire repository and save it to your Github account. That fork is now yours; you have full permissions on it and can do whatever you like with it, to the extent the license of the original product lets you. Generally, there's a couple of reasons to do this, here's a couple:

* People generally don't have permission to directly push a new branch onto a repository that isn't theirs. Select people will be granted contributor status, which often means they do have this permission, but doing this for everyone would cause all sorts of trouble. So in our pull request above, what we would do in reality is first fork NVDA to our own account, make a branch on that, do our work, and then send a pull request from our fork, rather than a branch in the main NVDA repository. Just a minor distinction.
* Maybe our pull request was not in fact met with approval, but you still want this functionality to be available to others. At that point, you can maintain the fork of NVDA with your Klingon language feature for other people to download.
* If, pray tell, NVDA were to ever be abandoned by its current maintainers, other interested parties can fork the product and resume development on it. Generally several people will do this and at some point it becomes clear what fork is the new "main" repository to keep an eye on, but that can get a little finicky and is outside the scope of this course.

And now we'll cover ....nah, just kidding. That's it. If you're still reading at this point, go get yourself a snack, you deserve it.

