+++
template = "page-with-toc.html"
title = "Questions and notes from workshop day 7"
+++

# Day 7 - 8/10/2025 - Jupyter Notebooks
https://coderefinery.github.io/jupyter/

Let's have some **icebreakers!** :icecream: 

If you could have a fully paid holiday right now, we cover all your costs, what would you like to do? Where would you go?
- I would take my family to some warm place with sea/swimming pool and amazing fresh food like fruits, veggies, fish...
- Spend a week on one of the canary islands with my family and/or friends
- Visit my family in the Austrian alps
- I'd just stay home and enjoying doing nothing!
- I'd like to take my family to Swiss Alps
- ...

Do you have a paper notebook at hand?
- I love post-its with different colors for different things, but they are not the same thing
- For important things I like to have a physical place where to write things
- Always! ...
- I write my (mental) pipelines with pen and paper
- ...
- ...

What is your way of working when it comes to writing code for your research projects?
- If I am not reusing previous version of scripts / pipelines, I first sketch things with Jupyter/R-studio interactively, then rewrite the jupyter bits into python scripts / RScripts, and run them from terminal for the final analysis (to avoid having results without being 100% sure on what the running order of cells / R lines was).
- do some analysis in IPython (a terminal version of jupyter notebooks), copy the code from IPython to python files (with %save), glue together those python files with a bash script <- should replace this with a proper workflow manager I think
- I am a total beginner, happy to hear what works for others. +1
- ..
- ..

## Questions
*Please remember to set the TwitcTV stream quality to "source"*

1. Can you please increase the volume? 
   - You should be able to increase the volume in the Twitch video to your likings. Does that make it loud enough?
   - Is it better now?
   - Yes, Thank you.
2. Seems some difference in audio volume between different speakers - XXXXXXXX fairly quiet compared to the rest
    - Thanks. We can fix it. (I won't talk at all basically)
    - LOL

> Forgot to mention about breaks: There will be one break (in about an hour) and [two exercise sessions](https://coderefinery.github.io/2025-09-09-workshop/exercises/#day-7) today (one before and one after the break).

## Jupyter notebooks

Course material: https://coderefinery.github.io/jupyter/motivation/

Your questions here: 
3. What is the differene between Jupyter Notebook and Jupyter Lab? Is it ok to use Jupyter Lab just not using all the features if not needed?
    - We will get to that in a bit 
    - For today it is OK to work with either
    - For the record and future readers:
        - Jupyter Notebook: the core system that interprets the notebook files (json) and via web browser allows communication with the kernel which runs the python bits that are on each cell
        - Jupyter Lab: a development tool that also includes ways to start terminals, work with git, browse file system. It is basically a fully working IDE that runs inside your web-browser
        - Bonus (for more confusion): Jupyter HUB: a large scale web application that allows multiple users to start their instances of jupyter lab. Most likely your university is running jupyter-hub, to let you start jupyter-lab sessions, and in those sessions you will run a jupyter-notebook :)
4. How does this compare to R Markdown? (Thank you so much for all these answers, guys! :D )
   - R markdown is written in plain text almost as code, while a jupyter notebook is something more in the "what you see is what you get". Also R markdown is mostly for R (although you can use other languages there...)
   - Also, jupyter notebooks are developed in a browser, while R-markdown notebooks are mostly written in RStudio (correct me if I am wrong)
     - jupyter notebooks can be also edited using vscode (with a plugin), possibly offering a more similar experience to RStudio/RMarkdown?
   - Maybe what I feel as the biggest difference is that Jupyter notebooks have a more interactive element, Rmarkdown is more about writing a reproducible document with text and code (and results) all in one place.
   - Maybe Quarto combines both world of Rmarkdown "papers with code" and Jupyter "interactivity". See examples https://quarto.org/docs/interactive/
   - Tooling: there is quite some tooling developed for jupyter notebooks: difftools, validation tools, converters to/from various other formats and ways to include those in documentation corpora. I am not sure about RMarkdown

## The user interface 
Course material: https://coderefinery.github.io/jupyter/interface/

5. Actually there seems to be one icon fewer in my Jupyter notebook UI.
    - out of curiosity, which one is missing? (I doubt it will affect your work)
    - It looks like the version control icon is missing, am I right?
        - I think so
        - Do you have the version control button on the side? Above the table of contents?
            - No
6. What fancy terminal app and plug-ins does the presenter use? They look fine as heck. (not the vs code one, the previous one where he was in his mac terminal)
    - ok, we can ask him to fill this info during the break :) (thanks!)
    - The terminal is called Warp: https://www.warp.dev/, I also use `zsh` instead of bash.  The downside of warp is you have to create an account and login... But it's a great terminal! (thank you, i will take a look at it because it seems really helpful with the autocompletion and suggestions : ) )

7. What tool do you recommend for version control of a notebook? Now every time I rerun a book, there is some diff shown up. I don't want those to be in the git history.
   - This will be discussed later. git has a filter mechanism that can be configured for that. ("nbdime" is the search word)
   - The nbdime program can be set up to be used with git: see https://coderefinery.github.io/jupyter/version-control/#using-nbdime-on-the-command-line


## A first computational notebook
Course material: https://coderefinery.github.io/jupyter/first-notebook/


:::info
## Exercise until: XX:00
https://coderefinery.github.io/jupyter/first-notebook/#an-example-computational-notebook


What to do? 
- Create a notebook with markdown and code cells and copy and paste the content from the exercise materials


:::

*If you have troubles, you can also ask for help in the help zoom room (link in the e-mail)*

*If you have extra time, you can take a look at https://coderefinery.github.io/jupyter/examples/#cell-profiling (We will cover widgets if we have time, so don't do that one :smile:)*


## Notebooks and version control

Lesson material: https://coderefinery.github.io/jupyter/version-control/


## Sharing notebooks

Lesson material: https://coderefinery.github.io/jupyter/sharing/

:::info

## Exercise until xx:55 

Instructions: https://coderefinery.github.io/jupyter/sharing/#sharing-dynamic-notebooks-on-binder

What to do?
- Create a public repository with the pi calculate example and connect it to Binder

Optional Exercise:
 - https://coderefinery.github.io/jupyter/sharing/#importance-of-tracking-dependencies
:::

Your questions here: 
9. It took forever to launch it. Is this usual for a first time notebook? It didnt take that long with the other (oohhhh ok get it)
    - So yes, the first time means creating the environment as well.
10. I used matplotlib==3.10.1 and it worked in case that helps
    - good to know :) 
12. Is the jupyter lab through binder running on our local machine or it is on a cloud?
    - in the cloud

13. So we didnt **specified where** is our **dependency list** when launching on **Binder**, it is preassummed on requirements.txt in the root of the repository?
    - ~~if you are using the coderefinery conda environment, then the dependencies were installed in the conda env~~ (edit: irrelevant for binder)
    - yes, for Binder the requirements.txt at the root of the repository defines the dependencies (see [here](https://mybinder.readthedocs.io/en/latest/examples/sample_repos.html#python-environment-with-a-requirements-txt). An alternative is the `environment.yml` for a conda env (see [here](https://github.com/binder-examples/conda))
    - Also, if its a R notebook, you should have a runtime.txt

## Widgets

Instructions: https://coderefinery.github.io/jupyter/extra-features/#widgets
14. I had trouble getting matplotlib to behave interactively with widgets when %inline is invoked. Maybe remove that? I think matplotlib has a quick way to invoke its widget with %widget as well
    - Thank you for sharing, this also worked for the instructor! <3
15. Can you please repeat how to enable rich git diff on GitHub website directly?
    - Click on you profile picture, and then feature preview, and then rich jupyter notebook diff. 
16. Can you send us last notebook with interactive function via widgets
17. AttributeError: `np.Inf` was removed in the NumPy 2.0 release. Use `np.inf` instead. Kindly help
## Feedback

:::info
Today we looked into Jupyter notebook and you got to play around with it. 
Next week (same time same place) we will continue with a lesson on automated testing. 
You will get some hints on how you may prevent yourself and others from breaking your working code by running tests manually and automatically.

Ask more questions in: https://coderefinery.zulipchat.com
:::

Today was ... (vote for all that apply):
Speed:
- ..too fast: 
- ..too slow: o
- ..right speed: oo
- ..too slow sometimes, too fast other times:ooo
Level:  
- ..too advanced:
- ..too basic: ooo
- ..right level:oo
Usage and recommendation: 
- ..I will use what I learned today: ooooo
- ..I would recommend today to others: ooooo
- ..I would not recommend today to others: 

One good thing about today:
- The content may have been basic but I get why it is super important to know how to handle these things and it was presented at an overall nice pace, so kudos for that
- ..both speaker taught are same pace and level
- ..

One thing to improve for next time:
- Maybe add one more exercise or theme in this session where we connect to a cluster with a jupyter notebook and work in data analysis, using installed programs on the cluster, submitting SLURM and things like that. o
    - That would be great, but unfortunately not everyone has access to a cluster, or even the need to work on a cluster and learn how to deal with it. 
    - Understandable. I am looking forward for more specialised courses then offered from you with these things in mind in the future.
    - Our friends at Aalto university have a HPC kickstart course, but I am unsure if Jupyter is a part of that: https://scicomp.aalto.fi/training/scip/kickstart-2025/ (it does not, I just learned, but anyway leaving the link here for review :) ) 
- ..

