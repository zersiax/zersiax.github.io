# Session 4 Notes

The notes for this final session will be very brief, for a very simple reason.
Over the last four sessions, we have covered a number of tools. We've looked at several resources, how to deal with accessibility issues you might find in said resources, and finally covered some code in two languages: HTML and Python.
You've gotten your feet wet, and I'm hoping it's made you thirsty for more.


It is, however, up to you what flavor of water you'd like to go for next. Last week, we covered Python.  This week, we covered the markup language HTML. They are two very different beasts, and yet, they do have some similarities and they even meet up in particular kinds of projects. But they are still their own entities with their own rules and usage domains.


I've expanded the resources sections of the previous pages with some more resources I can personally vouch for, oth for HTML and for Python. I will briefly cover what we discussed in class this week, after which I leave things up to you all. 


Want to learn how to program? Go learn Python or JavaScript. Want to just mark up some text so you can make interactive stories or easy to navigate text documents? HTML is all you need.



Want to build the next Facebook? You might need all three! :)


The sequel to this course will cover both domains more thoroughly, talking about more coding concepts as well as what you might run into if you decide to go for a career in this field. If that sounds good to you, we will pick it up again in April. If not, I'd like to thank you all for sticking with me through this course. Either way, all avenues for questions remain open to you, please use them, as I can only help if I know there is a problem, and no question is ever stupid or unimportant.


Before I send you all off for spring break, however, let's cover this week's material.


## What the h]ll is HTML?


HTML stands for Hypertext Markup Language. And that is actually a very good, if terse, description of what it does.


HTML is used to mark up regular text in order to turn it into hypertext. Hypertext sounds like text with super powers, some kind of Marvel Comics reject, and that wouldn't even be too far from the truth.


The way HTML works is simple. We start with regular text, and then we wrap that text in so-called HTML tags. By wrapping, I mean that we put an opening tag at the beginning of the relevant bit of text, and a closing tag at the end of it. This way, the text in question is "wrapped" in HTML tags, like so:

```html
<h1>Hello!</h1>
```


This text is wrapped in h1 tags, which make the text into a heading level 1. There's six heading levels in HTML, where number 1 is the most important and number 6 the least important. In that sense, you can use headings to outline your page. H1 might be your title, h2 your chapter, h3 your subsection, h4 your subsubsection etc.and in fact, this is very similar to how navigation levels in Daisy talking books work.


In class, we covered that tags don't just wrap text, they can also wrap other tags. This is called nesting tags, and it happens in every HTML document. Like we demonstrated, the head and body tag are wrapped in the html tag, and the title tag is in turn wrapped in the head tag, making a kind of hierarchy akin to a treeview. In fact, there is a treeview you can call up using the browser's so-called development tools that represent your HTML exactly like that.



Now, apart from content, a tag can have so-called attributes. They only show up in the opening tag, and give the tag some kind of information to work with. In class, we showed this off with the lang attribute, which sets the language that particular content is written in.


This way, elements, which is the word we use to indicate pieces of content including their tags, are in a sense enhanced to do more than regular text would. Let's show this off with an anchor tag, which is used to make links.

```html
<a href="https://google.com>This is a link to Google</a>
```


Here, we see that the text "This is a link to Google" has been given the super power to be a link. That means, a user can click only this bit of text, and doing so will take them to Google. It knows where to take the user, due to the href attribute, which is set to the web address of the Google website.



ARIA, which stands for Accessible Rich Internet Applications, is an extra set of attributes developers can use on HTML elements to make them behave a certain way for screen reader users in particular. This was done to make HTML able to do things it wouldn't be able to do before, mostly as a response to the explosive growth of what is possible on the web these days. It was always meant to be an addition to HTML, but unfortunately due to many developers' poor command of HTML as well as the browser's lack of strictness, ARIA is often used to patch over poorly written HTML when it later turns out that HTML is a problem for some users.


As stated at the top of this page, these explanations are terse for a reason. At this point, you are supposed to be equipped to go dig into resources that can be found on this very website to supplement your knowledge on the topics you in particular find interesting. The Resources channel on the Discord is a great way to vet a resource you have found that isn't listed, and all question portals will be monitored closely for the coming weeks to make sure we can get everyone up to a level they feel they want to reach.
For those who would like to look at the code we wrote in class, that could can be found [at this dropbox link](https://www.dropbox.com/s/tsk91p2q5wyhbxd/aph.html?dl=1).



Now, I say onto you all, go forth, and code!

