# Session 6 Notes

## Notes

The majority of this session's notes will, very similarly to session 3, be contained within the code we worked on during the lecture. Not a huge amount of material was covered, as we took an idea, that of a Guess the Number game, and wrote a very simple implementation of said idea. In that sense, what we did was take a number of concepts we covered before, and put them together to hsow off how they would be used in an actual working program.



To do this, we first wrote down a set of steps that, when followed, result in the program doing what we expect from it. This breaking a problem down into steps we can work on one by one is referred to as an algorithm, and in a program as simple as this one, it also serves as a document that is referred to as a functional specification.



Next, we used this list of steps to, one bbbby one, check them off the list as we wrote our code, all the way down the list until the program was completed.


While we were doing this, we frequently ran our code using the commandline. This is a flow I've found to work well when working with a screen reader, and it works as follows:


- First, open up your code in Vs Code, or another editor of choice.
- Next, open up a commandline window, and navigate to the folder where you have the code open in your editor. You can use the cd command to do this. Make sure the prompt matches the folder your editor has the file open in.
- Now, you can do "python your_file_name.py" to run your code as you work on it, to inspect the output it gives you. This is very similar to refreshing the HTML page in your browser if you're working on an HTML page, and indeed, a lot of modern front-end techniques do this for you automatically, letting you immediately see what your changes actually change on the page.


For this week, the main takeaways are this flow of working, as well as the way a conditional like an if statement can send the code down different paths, depending on what happens prior to the crossroads, if that makes sense. The annotated source code for this lecture will make this clearer, but feel free to ask question if you have them.
You can [download the code for this lecture here](https://www.dropbox.com/s/yv93pg78uiw0d8y/numbers.py?dl=1).


## Homework

For next week, you can try some of the exercises below:

- Having the right_guess always be 20 is great for debugging, but boring hen one actually wants to play the game. Figure out a way to make this number random. You will likely need to import some functionality into the script to do this.
- Right now, we're trusting user input and hoping they are nice and won't type something like potato into the guess prompt. If they were to do that at this point, the program would crash. See if you can figure out a way to make that not happen.


