# Session 7 Notes


In this session, we didn't do a huge lot of coding, but covered a lot of theoretical concepts that would feature in a coding project like the one we covered last week.
Below, I will expand on the two concepts that were central to this lecture: refactoring and object-oriented programming.


## Refactoring


Last week, we ooked at our Guess the Number game and created the most minimalistic version we could get away with. This kind of version is often referred to as an MVP, or Minimum Viable Product. As a developer, you will often create these to try out a new technique, defend research you did or test the viability of an algorithm or solution you have thought up.



Now, a Minimum Viable Product is often more focused on getting something to work than doing something in a way that is maintainable or easy to read. This is where refactoring comes in.



Refactoring is essentially the practice of taking existing code and altering it, so it becomes easier to read, maintain, test and extend. Usually, this involves breaking the code up into functions, cleaning up code that doesn't need to be there anymore, etc.


Refactoring is also performed to keep the code up-to-date with other portions of the code, or to solve security, accessibility and localization issues. To what degree these kinds of fixes have priority depends a lot on the company in question, and leaving them for later is so common that it has earned itself a jargon term: technical debt.


In class, we showed off that we can take some portions of the Guess the Numbers code and wrap it into functions, instead of doing it in place. The main advantage of this is that you can focus on the flow of your program first, and fill in the details later. You can, for example, do something like this:

```python
right_guess = 20 
welcome_user()
input = retrieve_input_from_user()
check_guess(input, right_guess)
# etc
```


Looking at this listing, it's pretty obvious at a glance what this program does. Responsibilities are split up between functions, which means that if a particular task is failing, we should only need to look at the function performing that ... well ...function. :)


Another advantage of doing this is that we can essentially take functionality of one program, and use it in another. Once we wrap our functionality in a function, that function can be clipped out of the program and added to another one. As long as we give the function arguments it can work with, it can run, irrespective of where it aws initially written. This will become clearer when you look at this week's code file which can be downloaded at the bottom of this page.


Now, copy-pasting functions from one file to another is one way to do that, but there's simpler ways. You can use Python's import statement to do this programmatically. We've already seen several examples of this in this course, but I will briefly recap in the below code sample.


```python
import random # import the entire random module. To access any of its functions, you need to do random.blah.
from random import randint # only grab the randint() function from the random module. You can call this function directly, without using random. in front of it.
```


This will work for files in the same folder, as well as modules you have installed in your Python distribution, more on that next lecture.


## Object Oriented Programming

There comes a time a system grows to be difficult to reason about or maintain without splitting it up into pieces. And there is various ways of doing that; indeed, we covered one of them just now.


One way that is pretty popular is the concept of Object Oriented Programming. In Object Oriented Programming (OOP for short) we group behavior, referred to as methods, and bits of information, referred to as fields or attributes, into cohesive units called objects.


Objects are often writtten in such a way that they resemble real-world objects. In class, we covered how you might write a Dog object, that has methods like bark(), eat_furniture() and play(toy). It might also have fields like number_of_paws, number_of_tails and cuteness_factor.


Now, you don't write objects directly. You essentially first write up what an object should be able to do, as well as what it should be able to tell about itself, essentially a definition of the object. A blueprint on how to make it, if you will. Such a blueprint is referred to as a class.



Then, you call a special method, known as a constructor, on that class in order to make objects that fit that particular blueprint. We call this instantiating the class, which really just means that we make the blueprint into a finished product we can work with in our  programs. Classes have an empty one by default, but you can also write this method's definition yourself. You would do this to make sure objects you create from the blueprint have some sensible defaults. You would for example generally want dogs to have four paws. :)



Object-Oriented Programming is a bit of a rabbit hole, and this explanation really only scratches the surface. You will doubtlessly learn more about this concept in the various resources that are already linked on this website, so I encourage you to do your own research on this topic. Truth is ...a lot of people struggle with this at first, and it takes the right explanation for it to click for you in particular. Maybe that is my explanation, maybe not, but either way looking at multiple sources on this one is a very good idea.


## Final Odds and Ends

For this lecture, there's no real homework, given next week is our final class. If you've stuck with it so far, go you, you're awesome, and I really hope I was able to teach you some things and show you this field is definitely learnable as a blind or visually impaired computer user.



The code for this lecture can be found [here](https://www.dropbox.com/s/cv63iri954325cr/numbers_refactored.py?dl=1). Muahahaha, sneak in one final inaccessible link :)
I will see you all next week.

