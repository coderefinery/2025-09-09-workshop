+++
template = "page-with-toc.html"
title = "Questions and notes from workshop day 9"
+++

## Icebreaker

- What programming language(s) are you normally working with (add an o for your answer):
    - Python:oooooo
    - R: 
    - Julia: o
    - C++: o
    - Fortran:o
    - Bash:oo
    - CUDA:o
    - HIP
    - (add yours here)...
- What is one small habit or workflow that helps you stay organized while coding?
    - Start new .py whenever I complete one section. And try to put comments upfront to explain what it is for.

## Modular code development
Materials: 
- https://coderefinery.github.io/modular-type-along/
- https://github.com/coderefinery/modular-type-along-exercise

Add your questions and comments here:
1. ...
2. ...
3. ...
4. 

:::info

### Exercise: two tracks (below), until xx:42
https://coderefinery.github.io/modular-type-along/exercise/
You have twenty minutes to either do the discussions below, or try to modify and modularize the code yourself.  We'll return 

:::



### Discussion track

A. What does "modular code development" mean for you?
   - Build parts of code that are general enough, and be able to put them together later on. Like Lego blocks.
   - Divide the code into modules, classes and functions that are either specific to a particular task or help avoid code duplication.
   - .
   - Divide code in blocks (whatever that blocks are), that are versatile enough but also easy to understand in separation
   - Something about [abstraction layers](https://en.wikipedia.org/wiki/Abstraction_layer) and separating concerns so you can build more complex stuff more simply.  Abstraction layers are really everywhere in computing

B. What best practices can you recommend to arrive at well structured,
   modular code in your favourite programming language?
   - Use functions where appropriate.
   - Split code into blocks (functions, classes, modules...). Block names should be easy to understand and descriptive, but each block should have only one reason to change (as a principle to guide how big the blocks should be)
   - Use modules, functions, and classes that are relevant to each part of the workflow. Also, include comments, docstrings, and other forms of documentation.
   - Though I am not practicing it TBH, I would say writing classes, functions, comments, splitting in files that are a meaningful whole. Also having diagram figures included for explanaiton would be nice. Also good instructions, preferrably as a video (something like "live coding example"). Then one can countionue in a same manner whether it's future you or someone new.
   - Command line interfaces let you make bits that are easily testable

C. What do you know now about programming that you wish somebody told you earlier?
   - GIT not being scary and difficult. I wish intros/shorcuts/setups were explained earlier to me for some stuff, cause just starting off takes a lot of time,i.e. "a right moment" that is often prolonged.
   - Have a main function instead of some free code at the end of a .py script +1
   - It's not hard to make something that is 'pip install'-able, you don't have to put it on PyPI, and this makes it easy to reuse stuff.  (I spent too much manually downloading and extracting into a PYTHONPATH).
   - PEP and good practices.
   - Motivational things you guys were saying throughout, that it is ok to have a messy code and similar (like I was not using this, i was not using taht but i do now, e.g. GIT, sphinx, etc.), just work on it. I am always thinking I am the only one having these problems and only one writing code that bad. XD
   - that there is no silver bullet. Things can get much better with proper practices and tools, but we are still fighting against our cognitive limits when developing software +1

D. Do you design a new code project on paper before coding? Discuss pros
   and cons.
   - Not usually, but when I do the outcome is usually much better!  (then why don't I do it more...?)
   - Sometimes. If not at the beginning, usually there is a point in time where I take pen and a paper and draw diagram at least. Nothing without pen and paper. It stays longer in my mind definitely.
   - Sometimes I just sketch a general workflow to guide me through what I need to do.
   - I like to rush to write some code to have feedback, but it hits me in the head sometimes


E. Do you build your code top-down (starting from the big picture) or bottom-up
   (starting from components)? Discuss pros and cons.
   - Usually top-down. I never really went for modular development, but for "just make it work". And then I am looking to finish it, not to be beautiful.
   - Whichever lets me get something I can run to see an output fastest, so I can start seeing if something is going wrong.  For example bottom-up if I can make a small bit I can run separately.
   - Top-down, most of the times. It depends on the task.
   - I need to go bottom up because otherwise I can't get things to work incrementally. If I think I know what I'm doing I do top-down, but then I don't get feedback until I have gone to the bottom


F. Would you prefer your code to be 2x slower if it was easier to read and understand?
   - Not always, but usually yes. I am not in an industry that will suffer if it isn't in "near real-time".
   - Most of it yes.  Not the (usually very) small bit that is speed critical.
   - No. 2x slower would be a nightmare handling billions of data.
   - I would like to have two versions of the code and use the one easy to understand to validate the other. Maybe impractical? 
       - I have done this too, once!  It gave me a lot more confidence in the accuracy.
   - Given the "Git" theme, I'd say it's very important to make the code more readable for the collaborators. Especially for the review!

### Coding Track:
https://coderefinery.github.io/modular-type-along/exercise/#coding-track

What are you trying to do:
- Replace comments with function names, remove redundant comments
- Understand what I need to change in the future, so that I can decide how to best pack stuff together: if I do not have to change what the notebook does and it works, I think it's clear enough that it does not need changes...

:::info
### Break until xx:03
Then live coding to make our example modular
:::

## Making our notebook more modular

Example solution (we don't have to do what is here in this order, you can make other suggestions): https://coderefinery.github.io/modular-type-along/solution/

Ideas to do (please give us suggestions):

- Plot for multiple month
    - using for loop, not copy/paste
    - using a function for the body of the for loop

- Is there a way to replace all "january" with "month_data" at once?
  - If you use a proper editor or IDE, definitely yes (something like right-click -> refactor -> rename)

- Tight view for images? Smaller ones? e.g. 3 rows 2 columns

- There is still quite a lof of repetition in the loop body, right? 
  - Also, we are doing `fix, ax = plt.subplots()` twice which scares me 
  - We could have as parameters:
    - the column of the df
    - the string for the title of the plot/y axis
    - the color
    In other words, the things that differ between the two "copies" of the code in the for loop

- How would you tackle if atm you need just one month per figure, but later on you may want all three months in the same plot?
  - Sometimes I will then also pass it an `ax` object to say "plot on this axis I have made" :+1: 
    - to default as "None" and in that case a new axes object should be created
     - I was thinking more of having three different colors for three months in single graphics, not using "ax" to have three one next to each other?

- I would use keyword arguments for that function (when I call it)
  - Good idea.

- month_data is a global, better to pass it as a parameter (for readability, I like to see what a function needs at the call site)
  - Good idea.
  - We left it off so that you can see the problem analyzed in vscode.

- Why do we need the 'arithmetic_mean'? (answered on stream: to separate plotting and statistics)
  - if I want to separate plotting from statistics I would pass the "mean_value" to the plot function, or perhaps pass the "summary" function in as a parameter?
  - Yeah, you can do it with a "summary" function.  I've done similar.

- .In your call to the plotfunction you have a "," after file name, why - there is no more parameters?
    - I often do this so that if I add another parameter, I won't forget the comma, and the version control history won't show the previous line as being edited.  Can make stuff a bit more clear, but of course is optional.

- Can you refer once again to "main" fucntion, its behaviour and purpose. Just a recap.
  - main() in python is not a special function. In this script, we call the "top level" function main(). 
  - the special thing about python is that in any module, there is a variable called `__name__`. If we are running that "module" as a script, that `__name__` is equal to the string "__main__". So, in that case, we run the main function when we run the script, otherwise we do not.

- Can you put 'argparse' in context of 'click' and running in command line? How similar/different is it?
  - argparse makes your script behave more like a typical unix application, where the behaviour can be modified with `--options`. Typically you create a parse object, add options to it, and get the values of the options that then you can process separately
  - click makes your script behave more like git or docker, with subcommands (but it can also be used to add 'options', as done in this case). It relies more on function decorators (define a function as a sub command, and define options for that subcommand using decorators on that function)
    - Argparse can have subcommands but it is a *lot* more typing (to the point I hardly ever do it...)

:::info
## Break until xx:08
Let us know what you would like to discuss:
:::

- How much of AI tools do you use when coding? How do you use it? Best one so far in your opinion?
    - Ask AI to explain it line by line. :D

- What do lecturers find useful (general tips/tricks/libraries) for coding that have not been mentioned during workshops?
  - debuggers
  - was TDD mentioned? For sure!

## Feedback

:::info
Today we have discussed how to make a simple script more modular and reusable.


This is the last lesson of the workshop! 

So we ask you for feedback not only on this last lesson, but also on the whole workshop.

Do not forget: you can ask more questions in https://coderefinery.zulipchat.com
:::


### For Today

Today was ... (vote for all that apply):
Speed:
- ..too fast: 
- ..too slow: 
- ..right speed: 
- ..too slow sometimes, too fast other times: o

Level:  
- ..too advanced:
- ..too basic: o
- ..right level: o

Usage and recommendation: 
- ..I will use what I learned today: o
- ..I would recommend today to others: o
- ..I would not recommend today to others: 

One good thing about today:
- Good topic, good lecturers.
- Clear in explaining.

One thing to improve for next time:
- Maybe keep it more "coding" during live coding, avoid copy-pasting. While writing discuss what you are typing. With copy-past it gets overwhelming.
- TBH, I expected more. I expected full coding experience, both bad one first (as typical rookie example), and good one (as a solution how good RSE does it). Level of task complexity can remain. Yet, I mised combining everything from the workshop. That would be a BOOM. Have it all together, relatively simple task, with two people coding, using git, wiritng documentation, etc. It can be same repeated from workshop to workshop, just work on it to have a FINAL MEGA RECAP. :)
- Pity not that many people joined for the last session, both viewers and especially organizers.
