+++
template = "page-with-toc.html"
title = "Questions and notes from workshop day 5 (Social Coding)"
+++

**How is the weather today at your location?**
- Helsinki, sunny but chilly
- Trondheim, raining and grey - autumn weather
- Copenhagen, it is sunny (for now....)
- Eindhoven, bit downcast
- Tampere, blue sky for now...
- Copenhagen, chilly but the sun is out
- Delhi, sunny but HOT 
- Belgrade, sunny
- Tübingen, raining and grey
- Kiel, chilly and surprisingly sunny
- Stockholm, sunny and cold
- Konstanz, cloudy and cold
- Karlsruhe, grey on grey
- Resistencia(AR), very sunny

**Have you shared some of your code with colleagues? Or has a colleague shared code with you? How did they share it?**
- email +6
- GitHub +7
- OneDrive
- gitlab, gitub, code snippets in group internal chat platform
- Had written some analysis scripts stored in the group's cluster, so I just transferred them to a common access folder +2
- usb
- Slack
- Teams/email for sharing R scripts mostly



## Social coding
https://coderefinery.github.io/social-coding/social-coding/

## Question 1: Why would I want to share my scripts/code/data?

**Choose many**. Vote by adding an `o` character:

- A: Easier to find and reproduce (scientific reproducibility)
  - votes:o oooooooooooooooooooo
0
- B: More trustworthy: others can verify correctness and find and report bugs
  - votes:oooooooooooooooo0ooo

- C: Enables others to build on top of your code
     (derivative work, provided the license allows it)
  - votes:ooooooooooo

- D: Others can submit features/improvements
  - votes:oooooooo

- E: Others can help fixing bugs
  - votes:ooooooo

- F: Many tools and apps are free for open source, so no financial cost for this
     (GitHub, GitLab, Appveyor, Read the Docs)
  - votes:ooooooo

- G: Good for your CV: you can show what you have built
  - votes:oooooooooooooooo

- H: Discourages competitors. If others can't build on your work,
     they will make competing work
  - votes:o

- I: When publicly shared, usually we time-stamp or set a version,
     so it is easier to refer to a specific version
  - votes: oooooo0ooo

- J: You can reuse your own code later after change of job or affiliation
  - votes:ooooooooooo0ooooo

- K: It encourages me to code properly from the start
  - votes:oooooooooooooooooooo


## Question 2: The most concerning thing for me, If I share my software now

**Choose one**. Vote by adding an `o` character:

- A: It will be scooped (stolen) by someone else
  - votes:ooo

- B: It will expose my "ugly code"
  - votes:oooooooooooooooooo

- C: Others may find bugs and mistakes. What if the algorithm is wrong?
  - votes:ooooooo

- D: I will get too many questions, I do not have time for that
  - votes:oooo

- E: Losing control over the direction of the project
  - votes:oooooo

- F: Low quality copies will appear
  - votes:o

- G: I won't be able to sell this later. Someone else will make money from it
  - votes:oo

- H: It is too early, I am just prototyping, I will write version to distribute later
  - votes:ooooooooooooooo

- I: Worried about licensing and legal matters, as they are very complicated
  - votes:oooooooo


## Question 3: Why is software often treated differently from papers?

Free-form answers:
- No idea, is it?
- Maybe because it doesn't work for all
- Because software can be constantly improved and modified whereas results in papers are usually a one-time publication :+2: 
- (More related to code accompanying papers than software) - but there's no standard way to share (e.g. OSF or GitHub?), or journals don't have specific requirements? 
- Because usually there are no reviewers for code.
- In my field, it seems like  nobody uses each other's code. Everyone develops a different method, haven't seen many cases where e.g. a GitHib repo is cited. Papers are "what counts"
- CBecause Reviewers in biology often don't have much coding knowledge and don't really ask questions on it besides general ones
- Some Code might be considered as reserach infrastructure, more than a reserach output 
- Software usually require maintenance over periods of time and in most cases the maintence part of it doesn't get recognition/citations. Hence people sometimes abondon a code when they no longer have to use it anymore
- Not knowing how to do it properly (not having real coding education and being poor or rookie at organizing it, versions, etc.), publishing code is sometimes pain in the ass, or just publish something so it is there.
- Difficult to write variations as in case of producing text
- Software is like a recorded song: developers can "sample" existing code snippets and reuse them to create new applications, much like a DJ. Papers are like sheet music: you can't just copy the notes; you must create an original composition by building upon the ideas and citing the source. Just different ways we treat the format.
    - Hey, you think you can. But code is also copyright protected. ;-)
- If data is sensitive, you can't make it available to use with the code. In papers you just publish the summary statistics or model outcomes.
- Funders don't care as much about it?

## Question 4: When you find a repository with code/library you would like to reuse, what are the things you look at to decide whether you use it?

Free-form answers:
- I usually go from a paper to the code, then I check whether I can understand the code and it matches what was described in the paper :+3:
- Kind of same, read a paper. Check if it has explanation, good documentation. Try to understand it, if I do i go for it, if not i quit.
- Read the paper, then the code and see if it is logical. Ideally, I also like to see test data samples where I can use the code on, to see if it really works as intended right out of the box before I proceed with my own stuff. (and also whether I can freely use it or there are licencing restrictions) +3 
- Paper to code as well. Check documentation, applicability and licence. +2
- F...
- If there are available tutorials and the code is well explained
- If its maintained, when it was updated last etc: :+2: 
- If the architecture is made so that I can take what I need, which might not be the whole code for example (the "I needed a banana, I got a gorilla and the whole jungle" problem)
- Good installation instruction, class structure, and assumption
- Ease of use, while still doing the job
- Tests! So I can trust it

## Any other question or comments related to social coding
1. Do reviewers ever check the code? Does anyone in academic have time to do that?
    - As a reviewer I do check it. And there are even good tools to anonymise the code when peer review requires anonymity (I will post the link later)
        - How about others? Is it most of them do, or most of them don't?
2. I find it frustrating when someone has done part of the analysis in paid-for software and the remainder in open source, so the full analysis is not possible to replicate. +2
    - Indeed. Some tools allow for a "runtime" tool to run code written in their proprietary language. But often it is just "private"

3. Are the codes checked for plagiarism?
    - We will get to that :)

4. Are there tools that will review your code or suggest better formatting (e.g. markdown) aside from AI platforms
    - There are for example *linters*, tool that review code violations etc, not exactly the type of refactoring that an AI model might suggest https://aaltoscicomp.github.io/python-for-scicomp/productivity/
    
5. on the importance of licenses: IIRC, in order to finally publish this code https://www.4c-multiphysics.org/history/ the legal department of a universityr had to chase up every contributor since the beginning of time so that a license could be agreed on by everybody. Is this a common problem?
    - I don't know how common it is, but some research groups have been developing code for years with multiple contributors, so I guess it would be a similar case if the code would suddenly need to become a product
    
6. Are there ways to check that the code I am using from someone else (given the licenses allow) is original and not plagiarized from another source? 
    - There are some code plagiarism checkers, but as far as I know they are only proprietary like: https://codequiry.com/ 

7. Are you devoted to explaining your old codes to newly interested people? For how long would you do it on aregular basis?
    - I guess nobody should be required to explain their old code, it becomes more of an ethical rather than legal matter. As researchers we want to be transparent and if someone is doubting our implementation we should at least clarify their doubts.

8. What if I find inspiration from someone's code but don't exactly use the same? +1
    - It depends. :) In a way the "clean room" design can be that (getting inspiration on how a certain function takes some inputs and produces some outputs, but not necessarily writing the content in the same way)

9. What's the difference, from the legal point of view, between taking someone's else code and using it (with 'using', 'import', 'include' or link time) and actually modifying it for your own purposes or copy/pasting it into your codebase?
    - If I use an external code (proprietary or not) in my code, all I need to do *ethically* is to tell others how they can reproduce/import/link the external code (e.g. build a conda environment so that you can import the same dependencies I have). In the moment that somebody else's code becomes part of my code (in a subfolder or even with bits of code inside my own code) then I need to consider that their license is compatible with my license for such derivative work.

10. Now that I've learned how to use GitHub from this course- If I've previously published a paper, how do I go about linking the paper to the newly available code (previously in supplemental info)? +1
    - You should publish it in a repository (like zenodo or institutional). Many repositories have integration with Github. Then you can get a DOI and licence. The metadata in the repository can contain the link to the paper. If the paper is already published it's difficult to link from the paper if the publisher often wont allow modifications of the paper.
    - I think it would be useful to have an overview of the different repositories? I thought GitHub was the repository... what's the difference between using that vs zenodo vs OSF (and probably many more).
    - overview of repositories: https://www.re3data.org/ but I think very code-specific repositories exist. A data repository like Zenodo will provide a DOI and mandatory metadata that makes your research output (more) FAIR. A repository should treat your published code with same value as paper. So you can't just delete it. If you change it, the DOI is versioned to be able to track individual versions.
    - Ok thanks. It really feels like there are way too many options... quite overwhelming to look at that website as a notice and attempt to decide which is the best to use. There seems like theres always more layers!
    - I totally understand. Ask your academic library for advice or try to find the repositories used in your discipline. If you have an institutional repository, use that one.
11. I've seen citation options on OSF, for code that is linked to a paper. Is it better to cite the code directly rather than the paper?
    - I think it's field dependent, but in general citations to papers are the "metric" for academic careers, so researchers tend to maximise those rather than citations to code (or to data).

12. I am very nervous about people seeing my messy code. How do I find the sweet spot between sharing my code and hiding my mess?
    - Start from day 1 with non-messy code by having lots of comments and structure. Pretend *they* are already reading your code.

# Software Licensing 
Link to the material: https://coderefinery.github.io/social-coding/software-licensing/
 
## Question 5: Which of these are derivative works?

**Choose many**. Vote by adding an `o` character:

- A. Download some code from a website and add on to it
  - votes:ooooooooooooooooooooooo

- B. Download some code and use one of the functions in your code
  - votes:oooooooooooooooo
- C. Changing code you got from somewhere
  - votes:ooooooooooooooooooooo

- D. Extending code you got from somewhere
  - votes:oooooooooooooooooooooooo

- E. Completely rewriting code you got from somewhere
  - votes:ooo

- F. Rewriting code to a different programming language
  - votes:o

- G. Linking to libraries (static or dynamic), plug-ins, and drivers
  - votes:oo

- H. Clean room design (somebody explains you the code but you have never seen it)
  - votes:oooo

- I. You read a paper, understand algorithm, write own code
  - votes:ooooooo


13. Comment/question: It confuses me in the figure on licenses that the two horizontal arrows have different colours. Does the colour carry any meaning? I missed it if that was explained.
    - Yes red is the proprietary licenses (basically copyright/IPR/patents) and the green the spectrum of open source licenses. Public domain (zero license) is at the bottom in grey.
    - Hmm right I mean the arrows pointing across
        - Yes that the very permissive can become fully red (your changes to the library can stay private), while the weak copyleft allow you to use it, but if you change some bits of that library you need to "give back" to the community (green arrow, this is what Björn was mentioning about the mozzila license MPL). Sorry if this wasn't super clear :)
        - OK I think I see the point, still struggling with the graphical illustration of it. An arrow into the red seems to suggest it becoming closed.

14. Are there cheat sheets for all these licences, explained in simple words "you can do this, you can't do that"? 
    - Good question! Nothing that I remember, but check for example https://fair-software.nl/
    
15. Are there any licences restrictive exclusively towards Big Giants? 
    - They can do what they want. :) Look at all copyright materials they have been able to use for their AI models. :)
    
16. Do you check licence for every single library you install/use in e.g. python?
    - our university legal team will say "yes" to this question
        - They are not the ones using it and writing codes, are they? Are you consulting them for every single one? :)
                - of course they are not, but they need to handle the legal claims. I'm not a researcher, but we need to handle this when assisting researchers in publishing data and code. In the spirit of this course, try to document libraries etc that you reuse in your code from the beginning :-)
    - Open source license are based on common sense :) so if you do not plan to modity the software, you can just download and use. The issue is when some products supposedly open add a "by the way, if you are an organisation with more than 200 employees, you need to pay us for using our software" (this has happened with Anaconda https://www.cdotrends.com/story/4173/anaconda-threatens-legal-action-over-licensing-terms; they recently removed non-profit/public sector from their license).

## Comments on LLMs for coding
- I haven't used it to write code (LLMs), but im not a programmer per se. Mostly write bash/python scripts for post processing simulation data in vim.
- I have used LLMs to generate small snippets of code, but never ended up using them as is +1

## Questions continued
- Why do we use LICENSE folder with many licenses? Wouldn't then licenses clas eachother?! One will allow something, while other would prohibit it? Up to now, I thought that we need to stick explicitly to single license?
    - We stick to one license for our own work, but if we "remix" work of others we also add their licenses and we make sure that they do not clash with our license (e.g. strong copyleft)

- There are tools to do a quick check for plagiarism on a draft you have made. Is there something similar for code?
    - Yes there is but it's proprietary https://codequiry.com/ . I don't know of any open source tool that can easiliy detect plagiarised code, unless one does searches of code snippets... 

## Exercise
**Do you cite software that you use? How?**
- Usually for molecular simulation software, they tell you which papers you could cite in order to support the team that makes the software but also to be "proper" when it comes to citations. +2
- . i refer to a paper introducing the code or a GithubRep +1
- I mostly use R packages, I mention all analysis related ones in the methods with their version and put the library citation there. Same for databases. (Non analysis related ones like ggplot2 are loaded in the publicly available code)
- Usually not, since it is written in README please cite this paper, and I find it enough.
- Yes, with author names and versions
- Yes, I footnotes of papers. +1
- For example like this: Skar Christiansen, Asmus; Andersen, Sebastian; Nielsen, Julius (2020). Adaptive Layered Viscoelastic Analysis (ALVA). Technical University of Denmark. Software. https://doi.org/10.11583/DTU.12387305.v7  +1

**If I wanted to cite your code/scripts, what would I need to do?**
- Cite the paper the code was part of.  +1+1+1
- Cite the paper and the code (as specified in README.md). +1
- Say that it was revealed to you in a dream :D
- .
- .That's the dream ;)
- .

Feedback
:::info

Today was (vote for all that apply):

- too fast:
- too slow:
- right speed: oooooooo
- too slow sometimes, too fast other times: o
- too advanced:
- too basic: 
- right level: ooooo
- I will use what I learned today: ooooooooo
- I would recommend today to others: ooooooooo
- I would not recommend today to others:

One good thing about today:

- Always good to discuss this and listen to, because I feel like having no one, or at least no one being interested in this topic and being able to provide any feedback to discussion.
- Reading about licenses and ethics and what can and cannot be used is usually like a fever dream for me. This was helpful in making some sense in all of this chaos.
- Thank you for the tools to check licenses among different codes.
- Introduction to licences. It has always apeared a very time consuming concept to me.
- It was a great lesson, not only it were reviewing important concepts but also it were discussed about what is important to share the code and to use a properly license too!


One thing to improve for next time:

- Precise explaining of licences, those mostly used. Like a table: this one means this, that one means that. +1 +1 +100
- Code plagiarism checker?
- Perhaps it would be useful to add some example of which license to choose in X use case
- .

Any other feedback?

- I know this is not a lot but the volume/voice was really an issue making it difficult to follow and enjoy the conversations! +1
- .


General questions continued:

- Can you make an starter introduction to HuggingFace, like we had for GitHub? +2 +1
    - We are actually planning something like that at Aalto. Stay tuned :)
- How about adding another week on AI tools, how to use them, good enough practice, etc., for everything covered through CodeRefinery? +2
    - This was discussed yesterday internally :D
- Is this series of Wednesdays workshops on youtube?
    -  It will be, if it is not already there. https://www.youtube.com/@coderefinery/playlists I see only first three days for autmn workshop for now.
    -  Can you order the list of videos in the youtube playlist from first to last? Thanks!
- Is there a SLACK community to coderefinery? It would be good to make one, and be able to ask questions there throughout the year. +1
    - We have a [Zulip chat](https://coderefinery.org/join/chat/)
