# Session 5
## Notes
I thought long and hard about how to structure these notes, due to the somewhat conceptual nature of ARIA. ARIA, at its core, is really just a somewhat complex set of HTML attributes that work together to enhance the degree of accessibility of an HTML page, primarily to make interactive applications work better with assistive technology.


Given the acronym ARIA stands for Accesible Rich Internet Applications, this makes sense. It truly comes into its own when a page is powerd, at least in part, by JavaScript or a similar dynamic technology like the Python-pioneered HTMX technology. Most of that is outside the scope of this session or even this course, so I highly recommend looking at some of the coding resources in the session 2 notes if you want to dig more into making pages dynamic, at least for now.



Having said that, though, I will not leave you completely without notes. For this one, I do highly recommend watching the recording of the lecture and ask questions if you have them, as it covers most of what you currently need to know about ARIA rather well and shows the effect of various ARIA attributes off using a running screen reader, something I'd be hard-pressed to reproduce textually.
For a more complete, text-based look, I highly recommend reading through [this article on ARIA by WebAIM](https://webaim.org/techniques/aria/) which goes into some of what I said during the video and expands on various points I introduced.



If the bit about components and JavaScript went over your head a little, that is just fine; you won't need to know how this works for the coming sessions and it's a rather tricky bit of engineering to wrap your head around at times, particularly when first getting started.

## Resources & links 
During class, several questions were asked that unearthed some useful tools for developing websites and checking for accessibility compliance. I will link to some of these below:

- [AXE](https://www.deque.com/axe/): a browser extension that can run some accessibility tests to check websites for WCAG compliance
- [Web Accessibilizer](https://www.stsolution.org/WebAccessibilizer/): This is a user script that lets you modify a page in various ways to make it more accessible. You can also store these modifications so they get applied each time a page loads. Finally, you can retrieve various bits of information about the elements on the page. Note that this is a user script, which means you'll need the Tampermonkey or Greasemonkey browser extension, depending on what browser you're using. Instructions are on the website.
- [NVDA Developer Toolkit](https://addons.nvda-project.org/addons/developerToolkit.en.html): This is an NVDA addon that has some of the functions of the script mentioned above, but integrated into NVDA itself.
- [ Class resources](https://www.dropbox.com/s/e91u6c4iilc49vp/filesforclass5.zip?dl=1): In this file you can find the chat log for this session, as well as the closed captioning text file which might help you if listening to the entire lecture proves problematic.
- [Final code for the class](https://www.dropbox.com/s/o727c7bh59862xi/aph%20aria.html?dl=1): This file contains the code we were looking at in this session. I added a few small things you can dig into for the exercises described below.

## Exercises

The final resource in the list above leads to an HTML file that has a few ARIA attributes set. See if you can figure out the following exercises, and send me a link to a file containing your answers on Slido, the Discord or per email/twitter.

- There is a heading at the top of the page with the text of "Hello". This heading is not shown when loading the page. Figure out why this is, and fix it.
- What do sighted people see, rather than our cleverly hidden message in the heading below the first one?
- Extra credit: There is a div element that has some rather odd things going on with it. What has been done to this element? Why is this a bad idea?


See you all next week :)
