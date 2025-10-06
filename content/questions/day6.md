+++
template = "page-with-toc.html"
title = "Questions and notes from workshop day 6 (Documentation)"
+++

# Day 6 - 01/10/2025

Let's test the notes with some icebreakers! :icecream:

**What did you have for lunch today?**
- Omelette +1
- Some vegan dish 
- Cheese and pickle sandwich
- breakfast +3
- pasta
- rice, chicken, farofa, and salad
- tofu tomato soup
- nothing yet
- beef and vegetable 
- croissant, peanutbutter and jams
- Thai green curry
- pasta

**How would you explain your current job to someone in the year 1700? (if you don't know, write what you do and we'll try to figure out!)**
- I use a special interactive abacus to create a picture of how small bits of matter move and interact
- Draw a conceptual workflow
- Mechanical calculator operator
- I use a calculator to do chemistry because lab chemistry makes me dizzy : (
- I do maths on animals
- We ask children lots of questions to try and find out what makes them feel sad
- We try to figure out how to help people having bad headaches and seizures (brain tumors)
- I'm like Luther, making knowledge available to the whole society
-  We try to understand what happens in the plants and soil when your sheep are grazing or not
- Coordinating the work of a group of people
- I make recipies for magic thinking rocks.
- ..
- 

**What's the best documented project you've seen?**
- sklearn or pandas (LAMMPS in my heart) +1+1
- pytorch is pretty well documented that even a scrub like myself managed to get a project going
- +1 +1 for python documentation in general
- Pennylane - quantum computing framework
- KielMAT: Kiel Motion Analysis Toolbox
- The ArviZ project
- ..

##  How to document your research software
https://coderefinery.github.io/documentation

### Motivation and Wishlist
https://coderefinery.github.io/documentation/wishlist/

#### Is project documentation important? Why?

- Yes, so I and others can understand at any (future) time what we were doing and why we were doing it in this way +1
- Yes - helps me to understand what I was doing and how to use the code in the future (when I've forgotten most likely), also lets others understand how to use the software
- Yes, needed to get the paper published -.- +1
- For reproducibility 
- Yes; it is also a way to follow the evolution of a project.
- Projects are living things. People come and go and one of the more difficult things is getting new people on board with the context of the project and the methods. Good documentation helps not lose momentum and have all people up to speed
- Yes, if someone cannot use your code because it's documented poorly, then you code isn't being used optimally
- Yes absolutely. A well-documented project allows others to reuse your code and even warn about errors o bugs in it. So, you can improve your code and increase their quality.


#### How would you describe a useful documentation?

- Easy to understand and complete.+1
- Concise, precise and easy to follow. +3
- One which provides dummy data to work through alongside.+1
- Also, video form of going through a documentation I find very helpful. Sometimes it's hard to get used to documentation syntax.
- Ones that assume that you know nothing +1
- Appropriate to the scale of the project being documented
- user-friendly


#### How can you motivate your colleagues to contribute to the documentation?

- Ask them if they still know what they've done for the project a few weeks ago and if not ask them to document it better :D
- "future you will thank present you" + 100
- No cake for them on friday if they do not help
- +1 for cake motivation above
- With presonal example XD


**Your questions here:**

1. How to find a balance between writing documentation, comments in the very code, and time spent on all this?
    - This is a hard question, it depends on the project. If there a are many users, you should spend a lot of time writing documentation. If only a few, portion of time should be low.
    - Test it. Have someone else try and use your documentation. If it works, it was enough. (excellent advice)

2. Difference between text/ascii and .md and .rst files
    - markdown and rst offer some more options for formatting and "presentation" over pure text, while still being lightweight compared to writing something like latex.

3. How would I type mathematical expressions in markup languages?
    - Like this: https://github.com/pytorch/pytorch/blob/v2.8.0/torch/nn/modules/instancenorm.py#L127
    - details might depend on what dialect of markdown you are using.
        - Alright, thanks!
    - We have an example with MyST in the lesson material: https://coderefinery.github.io/documentation/sphinx/#exercise-sphinx-and-latex
    - For situations were the answer might depend on fairly arbitrary decisions I tend to look at what the projects in the area I am working in are using. That way the result is likely to be similar to what people there are already used to. That's why "numpy" is pretty much also a documentation style. https://numpydoc.readthedocs.io/en/latest/format.html

4. Regarding zombie code. I understand why comments should not be used for this purpose. However, sometimes I try to optimize code using various ideas. By keeping my failed attempts as zombie code, I remember them and more importantly, don't try the ideas again. What is the alternative?
    - I tend to have lots of commented code or attempts/debug output that I remove before I make a pull request.
    - Some code snippets that you want to keep around would probably be fine to keep as a comment as part of internal documentation with some additional explanation why you are doing it (not) that way.


## Writing good README files
https://coderefinery.github.io/documentation/writing-readme-files/

5. What tool should I use to properly render the markup language of a readme file on my computer? Can I use an ordinary browser?
    - There are some web based ones. Your browser can usually render markdown. I tend to not bother and just push it to github, where it gets rendered. You can also use hedgedoc/hackmd
        - Alright, thanks! The reason I ask is that ideally, I think it should be possible to read the readme file on your own computer without having to go through github.
            - A lot of readmes will include badges or some kind of additional information pulled from CI/CD or other sources, so at least some of the time you can not get the full version as it would be on the repo.
            - For documentation you can run tools like sphinx locally, which will generate the webpages you can then browse with your webbrowser.

6. What is alt text?
    - Alternative (I believe it stands for) text that should be added to images, describing the image shown for e.g. screenreaders (so that a blind person would also benefit from the information shown in the image)

7. When using badges, we link a badge image.  Do we need to somehow create our badge image before, or we do that through markdown?
   - Typically badges are available at a site somewhere on the internet, that is linked then in the markdown file. The badges can be "dynamic", in the sense that while the url of the image stays the same, the image itself changes (e.g., when the tests in the continuous integration setup pass, you get a green badge, when the tests don't, you get a red one)
    - If you are making e.g. a test coverage report badge, than there are pre-made github workflows that will help you create that badge as part of your CI pipeline. That workflow will then also commit the generated file to your repo so it can be referenced from the readme.
  
::: info
## Exercise untill XX:58

You can do either of these exercises: 
README-2: https://coderefinery.github.io/documentation/writing-readme-files/#exercise-improve-the-readme-for-your-own-project
README-3: https://coderefinery.github.io/documentation/writing-readme-files/#exercise-discuss-the-readme-of-a-project-that-you-use

Please note observations and recommendations in the collaborative notes.
:::


#### Some example README files
https://github.com/paboyle/Grid
https://github.com/opendatalab/MinerU

Any questions about the exercises? Ask below: 

8. Bit confused what we are meant to do?
    - You can choose exercise 2 or 3, there is no need to do both. 
    - Either comment on the example README or discuss any questions, or just try out some markdown features on your own README file. 
    - Please note observations and recommendations in the collaborative notes.

**Question to all**: Any comments on README files you have seen or you are working on? (in other words, you can add observations from Exercise  README-2 and README-3 here)

9. One of the READMEs has links to the wiki in the Github repo - is this a good idea?
    - May be hard to keep in sync, but if it is stable, ok
    - Other options than Wiki (for extended documentation) shown in remainder of this session 
    

## Sphinx and Markdown
https://coderefinery.github.io/documentation/sphinx/

:::info
For the following session, if you want to follow along on your local machine you might need https://coderefinery.github.io/installation/conda/
Join the Virtual Help session (link in e-mail) if you have questions or need technical support
:::

> Please do type along, if you want to :) You can find all commands in the lesson material: https://coderefinery.github.io/documentation/sphinx/ (you will also have time to do it during the next exercise session)

:::info
## Exercise session until XX:55

**Start with Sphinx-1 and see how far you get :)**
Sphinx-1 (was shown by Michele on stream): https://coderefinery.github.io/documentation/sphinx/#exercise-sphinx-quickstart
Sphinx-2: https://coderefinery.github.io/documentation/sphinx/#exercise-adding-more-sphinx-content
Sphinx-3: https://coderefinery.github.io/documentation/sphinx/#exercise-sphinx-and-latex
Sphinx-4: https://coderefinery.github.io/documentation/sphinx/#exercise-sphinx-autodoc
:::

Questions regarding the exercise: 

10.  I have myst_parser but sphinx cannot import it. What could cause this:           
     ```
        (coderefinery) user@mint:~/Desktop/Downloads/doc-example$ python -c "import myst_parser"
        (coderefinery) user@mint:~/Desktop/Downloads/doc-example$ sphinx-build . _build
        Running Sphinx v7.2.6

        Extension error:
        Could not import extension myst_parser (exception: No module named 'myst_parser')
     ```
        
   - Is that the same interpreter?
       -> Try running `which sphinx-build` and `which python`. Those should both print a path: Are the two in the same folder? Let us know what it prints.
        - Or even `type -a python`
    - This is the answer from prompts. Sphinx-build is always linked to the same path, nomatter which environment I used to initialize it:
      ```
         (coderefinery) user@mint-desktop:~/Desktop/Downloads/doc-example$ which sphinx-build
        /home/user/.local/bin/sphinx-build
        (coderefinery) user@mint-desktop:~/Desktop/Downloads/doc-example$ which python
        /home/user/miniconda3/envs/coderefinery/bin/python
        (coderefinery) user@mint-desktop:~/Desktop/Downloads/doc-example$ type -a python
        python is /home/user/miniconda3/envs/coderefinery/bin/python
      ```
      - It looks like sphinx is not installed in your conda environment, but to your user home directory. You can try running `conda install -n coderefinery sphinx`
      - Long term solution: at some point in your past you did something like "pip install sphinx" without being in an environment, and that went to the default location in "/home/user/.local/bin/". Ideally in the future you want "/home/user/.local/bin/" to be empty so that things are only in the environment you have activated, otherwise they will always have higher priority and override the sphinx-build which is in "/home/user/miniconda3/envs/coderefinery/bin/" :+1: 
          - With python things, better to have everything in venvs/conda envs or similar to avoid these kinds of conflicts
      - Run python3 instead of python. I had a similar issue. That is, try python3 -c "import myst_parser"
      - Yeap, with `python3 -c "import myst_parser"` cannot import it. However, its late now to fix. Thanks anyway!
      - You can still join the virtual help session if you want to set it up to play around with it later. 

11.  What is the syntax for a numbered list? Any (non-negative) integer followed by a period?
     - Yes (to my knowledge), and they will be automatically renumbered
         - Ok, thanks!

## Sphinx documentation to GitHub pages
https://coderefinery.github.io/documentation/gh_workflow/

> Please do follow along with Yu to deploy your own sphinx documentation to GitHub. If you prefer, you can also lean back and just watch (and try it out on your own time). https://coderefinery.github.io/documentation/gh_workflow/#exercise-deploy-sphinx-documentation-to-github-pages
  Repository to clone (to save time): https://github.com/new?template_name=documentation-example&template_owner=coderefinery

Questions continued: 

12. . SUGGESTION: YOU ARE GOING TOO FAST!!!!!
    - Thank you for the feedback! Sorry that it went too fast. 

13. Because we have to do exdercies for homework, right?
    - I don't understand the question. Seems like some context is missing. 
    - there are exercises i couldn't finish during the lecture today
        - You are welcome to continue working on them.

14. If we choose to build a sphinx mini website for the certificate exercise, how big should it be? Like the size of the tutorial we did today or a bit bigger?
    - One page is enough :) but if you are having fun, do something bigger! Try various templates...etc... It's your chance to experiment and learn what you need/want.

15. If i delete the repo from which a website is built does that also delete the website or do i have to do it separately?
    - In general there is a github action on the repo that builds the website and publishes it. Deleting the repo only removes that process, i.e. any further updates to the page. Generally you would need to delete the existing website separately. Details may depend on the exact configuration you are using.
    - In the context of github pages, deleting the repo (including the branch served on the website) will also delete the website


:::info
### Thank you for today!
We hope you learned something new about documentation and can take up some of the tools and techniques into your daily work

### Next week we will look at Jupyter Notebooks

You will need the CodeRefinery environment to play around with Jupyter and do the exercises. Even if you think you know Jupyter Notebooks already, you might get something new out of this session!

### Continue the discussion and ask questions

You are also welcome to join our community chat at https://coderefinery.zulipchat.com to continue discussions and ask any questions you may have!

:::

## Feedback for today

Please let us know how todays session went for you: 

Today was (vote for all that apply):
- too fast: oooooo
- too slow: 
- right speed: ooooo
- too slow sometimes, too fast other times: oo
- too advanced:
- too basic:
- right level: oooooooooo
- I will use what I learned today: oooooo
- I would recommend today to others: ooo
- I would not recommend today to others: 

One good thing about today:
- It was one of the best lectures of this workshop. Very, very good.
- A comprehensive introduction to building and deploying Sphinx. 
- Very useful resources and examples
- Overview of making good READMEs (sometimes that's all a project needs)
- I look forward to start using what I've learned today.
- Useful tools(Sphinx and GH actions) to apply on my projects


One thing to improve for next time:
- Not per se an improvenent, but I'd be interested in more information on GH actions.
- Give a bit more time to follow the exercises
- ..

Any other feedback?
- Lecturers were great.
- Really interesting and helpful, and enjoyed the presentation - thank you +1
- ..YES LONGER SESSIONS. So that we get finished all exercises etc during the day.... especillay when creating new documents, folders... than all that updating at github omg it takes a lot of focus to do it immediately

General questions continued:
- Too fast: yeees, a lot of things in a short time
- Expand this lecture in future, maybe into two days (not just longer, but deeper). (boring documentation turned out to be pretty hot ;)


