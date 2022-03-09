# Glossary
## Session 1
### Commandline

* Operating System (OS): The software that makes your computer go. Examples are Windows, Mac OS and Linux, as well as iOS, Android and Chrome OS.
* MUD: Multi-user dungeon/domain/dimension, a form of text-based online game that was primarily popular during the 90s but is still a thing today. Notable examples are Alter Aeon and Miriani.
* Bash/zsh/shell: A shell is essentially an interface to your computer. Bash and ZSH are shells commonly found on Mac OS and Linux variants. The Windows equivalents would be Powershell and cmd which to my knowledge doesn't have another official name, although some people refer to it as a DOS shell, command line, command prompt etc.
The new Windows Terminal is a program that can essentially access both of these, but setting this up is at least for now outside the scope of this course.
* Environment Variable: In programming, a variable is essentially a box in the computer's memory you can stick a value into. In that sense it's similar to mathematics, x=5. When we say x, we mean 5. In programming these valuees can often be changed, hence the name variable.
Environment variables are bits of information about your environment, essentially your system, and the PATH variable holds the list of folders to look through when you run a command on the commandline.
* GUI: Graphical User Interface. Essentially just buttons and such you can click and tab through, as opposed to CLI (commandline interface). Some people pronounce this Gooey, others just spell it out, take your pick.

### Git / Github

* Repository: Often abreviated to repo. This refers to the git storage for all the changes it keeps track of in a folder you're working in. When you make a new repository on GitHub, the term repo is often used for the project in general.
* Branch: Branch off from the main branch and keep track of changes from this point forward  into that new path, making sure not to influence the main branch. To make a new branch, the command is: git checkout -b nameForYourBranch. To switch back to another branch, the command is: git checkout nameOfYourBranch, so without the -b switch.
* Merge: Take the changes made in a branch, and integrate them into the main branch. This will generally happen automatically unless there's a merge conflict, which happens if the main branch and the new branch both touched the exact same line. At that point, you need to tell it what version to go with. The command is: git merge BranchToBeIntegrated, so you would generally run this command from the main branch.
* Push: Send your local unpushed changes in the current branch to the remote host.
* Source Code: The source code is the human-readable version of a program's programming code. This code is either interpreted or compiled to make that code executable, more on that in later sessions.
* Open-Source: Essentially, source code out in the open. There's more to it, but I invite you to google "what is open source" for that one.
* Issue: An issue on Github is a point of discussion, usually either a feature request or a bug report. Someone files an issue after which the core contributors take a look into it and provide feedback or further questions.
* Remote Host: A remote (as opposed to local) place where something is hosted or served. In this case, GitHub.
* Klingon: Fictitious language of an extraterrestreal warrior race from the Star Trek Universe.


## Session 2
### VS Code

- Code Editor: A code editor is similar to a text editor but may have some code-specific features like visual syntax highlighting, running your code from within the editor, getting popups for code documentation etc.
- Integrated Development Environment (IDE): An IDE is a code editor on steroids, together with various other tools like a debugger\*, UI designers and all sorts of other integrations and tools.
- Debugger: A debugger is a tool that essentially lets you step through a running program one line at a time, in order to carefully examine what a line is doing and how it might be causing problems. We'll cover the debugger in a few sessions.
- Reaper & ProTools: Both digital audio workstations to edit and manipulate audio with. Reaper is cheap and speedy, ProTools is pricy and complicated, which of course makes it an industry standard.
- Cross-platform: Able to be used on more than one operating system, e.g. not just for Windows but also Mac OS.
- Feature Perity: A term used to indicate if two versions of the same program have the same feature set. To not have feature perity means that one version is missing features the other version does have.

### Python

- Linting: The process of checking code for style problems, code considered to be following bad practices or other things that don't outright break your code, but make it look less pretty, efficient or readable  than it could be.
- Pip: A python tool to download bits of code other developers have written and made available to augment your own project. 
- String: A string is a series of characters like a word, a sentence or some other piece of text. In Python, we make a string by wrapping said piece of text in quotes.
- Variable: If we are going to need a value for a longer time, we stick it in a variable. It's essentially a box to hold onto the value for us while we go do other things. We give the box a name, which then becomes a way to refer to the box's contents, similar to how you know the trash can has garbage in it and not rose petals. Once a variable has been created, its contents can still be changed, hence the term variable.
- Function: For now, consider a function as a mini program. You give it something to work with, it does magic, and it returns\* a result.
- Return: When a function is done doing its magic, it's likely here's some kind of result of that magic. If your function transforms a human into a toad, your function acts on the human, and returns a toad.If we need the toad later, we can store it in a variable.
