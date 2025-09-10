+++
template = "page-with-toc.html"
title = "Questions and notes from workshop day 2"
+++



## Icebreakers
Let's test the notes with some icebreakers! :icecream:

### What was the last animal you saw?
- Otaniemi geese (aka angry birds)
- Squirrel :+1:
- A bird that tried to steal my sandwich :angry: 
- Pigeon
- Spider
- Two hyper happy kids of mine
- Our office dog. Collecting pets and treats
- ... isn't it human for most of us?  before that CATS.
- Cat +3
- fly
- bee 🐝 
- some small fly
- .
- human +1
- Dog
- Red vented Bulbul
- Duo (bird in Duolingo)

### What do you want to be when you grow up?
- A research software engineer! +2
- A Scientist
- Time traveller
- financially independent (and a computational chemist, hopefully)
- A kid +1
- I work in a university now but wouldn't mind going to a company someday, if it's doing something useful.
- A magician.
- sheep farmer
- electical engineer,  but later computer scientist

### Poll: Which path did you use yesterday to interact with Git?

- GitHub: oooooooooooooooooo
- VSCode: oo
- Command line: oo
- I was not here yesterday (no problem): o
- I wished you offered a path for a different tool (which one?): 
    - Jupyter
    - VScodium
    - ...


## Questions
1. questions here
   - answer
2. Can I do today's exercises with just a Github account?
   - In theory yes, we support that.  Some parts are similar to yesterday, some are new.  Some bits may not be fully possible.
3. The video quality at our end is a bit mixed, sometimes good, sometimes very low. Do others have the same? Perhaps it is our wifi (DTU Lyngby)
   - Try to set it to "quality: Source" in the settings (gear button) to force it to be high.  If it still happens, let us know and we can see if we can do anything better. (Somehow it's the browser thinking to save bandwidth) 
   - THanks trying that now. Seems maybe wifi here is the issue, so trying to find a LAN cable...


## git-intro day 2

### Local workflow
https://coderefinery.github.io/git-intro/local-workflow/

4. I have a meeting at 12 I wanted to ask when the break will be. I just want to know if I will miss anything if I go a bit before time? 
   - The (1hr) break should start about 2hr from now and a 10-min break starting in 40-50 min.
   - If you have to leave early though, you can watch the parts you missed on Twitch, or later on YouTube, so don't worry :)
5. Could you put your videofeed of your faces to the lower part of the screen. As it is you hide the url you are using . Thanks 
   - the url is https://coderefinery.github.io/git-intro/local-workflow/
   - but we will try to find a more convenient place for the faces (it's hard!)

6. When working in command line, how to make sure the new file is in the right directory, eg. soups? (in point 4 of the excercise)
    - (on linux/mac) you can use pwd and ls to check in which directory you are, and what files are in it. git status shows changes to the repository.
    - The git repository is a normal directory/folder on your computer, so everything you use for moving or locating files will work normally
    - But yes, this is a very good point!  From command line you need to make sure you are in the right place.

7. Should I be worried by the message "warning: in the working copy of 'pasta/cacio.md', LF will be replaced by CRLF the next time Git touches it"?
    - This tells you that there is a missmatch between the type of linefeed (or newline) character your system uses and the one on the repository. If it is your own fork, I would not worry about it.
    - Yeah, won't affect the course for now.  You can figure it out later if it becomes a problem.

8. How to exit the graph in command line? I have [END] message but enter, ctr+c nor ctr+x works?
    - :q should work
    Thanks, was it vim? or less?
    
:::success

# Exercise until xx:40

You can find the exercise here:
https://coderefionery.github.io/git-intro/local-workflow/#exercise

*(don't forget about the zooom help room if you need help and you're alone)*

Progress report - add 'o' to the relevant option. You are:

- done: oooooooooo0oooo
- stuck: o
- not trying:
- working on it:

What tool are you using?
- command line: oooooooooooo
- vscode(ium): ooooooooooo
- github
- VS code but ultimately want to use Rstudio so trying that too!
    - Can the same thing be done directly in Rstudio? 
- command line, but want to learn with VS code (ubuntu user)
- vim
- 
:::
9. Should we keep the branches we have created and then merged to the main one for our exercises to serve as proof for the certification test, or is it ok if we delete them and simly show our graph and history tree as proof that we did what was expected in each exercise?
    - didn't we just need to proof that we followed Exercise 3 for today?
        - As long as you are learning and doing and there are "digital traces" that you have practiced/tried, the "proof" is not too strict in this sense.
    - Yes, i guess you are right. this was more of a general question for the previous day too.

10. At step 7 I used the terminal in VScode to view the graph, but at the end of it it just said END and I can't seem to exit the command (tried ESC etc). 
   - try pressing q <- worked thank you :) <- you are most welcome :)

11. Maybe it is just us, but it would be easier to watch if your screen was normal size (not long format).+2
    - This is done for those who need screen space for other things (notes, or their own following along activities)
    - Also, you could put the notes (if you are interested) on the other side of the screen
        - I understand, but it makes it difficult to follow. I'm sure it would be easy to move between notes and your screen even if it is full size. Maybe it is possible to ask how many need the screen to be long like now? Sorry for being difficult!
    - In past workshops the portrait screenshare has been very appeciated.  We know it can be a bit cramped, but it forces us to keep the screen clean and provides learners with lots of space for your own work.  With a full-screen screenshare, everyone has very little room to work.
        - Ok!

12. Your broadcast goes in and out of focus - am I the only one having this prolem?
    - Try using the gear icon for settings to switch to "Source" quality - this will force it to use the highest quality.  Sometimes the browser tries to save bandwidth.


13. What is the difference between fork and clone ? again. 
    - fork: creates a copy of the repo, but on the GitHub servers. You own the copy and you can do (almost) everything with it. Your copy of the repository "remembers" the repository it was forked from
    - clone: creates a copy of the repo, but not on the github servers: typically on the computer you are using. The repository on the computer you're using (the *local* repository) will 'remember' its connection to where it was cloned *from*.
    - technically, a fork is a clone, but a fork is on github/gitlab/whatever    

14. Can we have a video or demo with R also ?
    - Hopefully someday, but for this workshop we probably don't have time.  If you know the concepts and words, you can probably read and adapt to RStudio (or whatever) quickly.  At least that's our goal!
    - +2 would love a short R/R studio specific workshop/demo. A lot of colleagues would be interested ;)


15. When I enter commit it says make sure you configure your user.name and user.email
    - You can set this like this: https://coderefinery.github.io/git-intro/configuration/#name-and-email-address-for-git-commit-metadata
    - From the command line (the vscode terminal should also work), run:
    - ```
      git config --global user.name "Your Name"
      git config --global user.email yourname@example.com
      ```
16. Will all the walk-through be carried out in VS? It's hard to follow when I was doing the excercise in command line. 
    - The next one will be with command line
    - Later also another demo with VS code



:::info
### Break until xx:10
We've just done the same as yesterday, but now on our local computer.  Something we can actually use!

We'll continue with this by looking at more of the history after the break: really dig deep to understand what we can get from it.
:::

## Inspecting history
Lesson material for now: https://coderefinery.github.io/git-intro/archaeology/

17. How to get networkx in command line? I don't have it in my cloned local repository
    - it is a different repository that needs to be cloned separately
        - https://github.com/networkx/networkx/
    - you would typically do something like
      ``
      cd # without arguments to get to your home dir, outside of any existing repository
      git clone https://github.com/networkx/networkx.git
      
      ```

18. But it it like a general repository, with some methods? Not like our recipes?.
    - The networkx repository is a repository containing code from a real project (which in this case is python code).
    - The recipes repository is a toy repository that contains only text (maybe this is not true, the recipes there might be true ones, and I believe that recipes still deserve to be under version control, even if my grandma did not do it)

19. for whatever reason i cannot copy paste into my terminal. Is there a setting i can change to fix this?
    - you might need to do right-click to open a context menu and then select "paste" or "copy"
      - okay thank you
    - in other cases, you might have to use "CTRL+SHIFT+C"  to copy from the trminal (you should still be able to use CTRL+C to copy from all other windows) and "CTRL+SHIFT+V" to paste in your terminal (still use CTRL+V in all other windows)
    - this is also be

20. Can you copy the link of page with exercise here which is being shown in live?
    - https://coderefinery.github.io/git-intro/archaeology/#exercise Does this answer your question? (See also the box just below this)



### Exercise until xx:45
https://coderefinery.github.io/git-intro/archaeology/#exercise




21. I cannot type "/Logic Error" while the 
    ```
    git annotate networkx/algorithms/threshold.py
    ```
    is in use. Is that normal? 
    - When you type the first '/' you should see it appearing at the bottom of the screen, and then the following "Logic Error" should appear (if you type it) following that.
        - It works, but then shows no pattern found?
        - It means that, in the version of the repository you are looking at, that file does not contain that sentence... Perhaps you need to "checkout" a specific version first?
        - the exercise suggests you do 
          ```
          git switch --create exercise networkx-2.6.3
          ```
        - And, **be careful with capitalization! It's "Logic error", not "Logic Error"**
        - i was using "" but it didn't need them, just Logic error. my fault
        

I use the command: git grep "degree_correlation"
That should 
surely find the line, but it does not. It 
finds 5-6 other lines with the wordser inspection the file I shold find does not exists, so maybe there is an explanation. The cloning was wrong. NO that was not it, the file is there. The line is NOT in the file. Yeah, I did not follow the recipe entirely by the book, as I need not learn - not to copy. But that is likely the reason.
I will change my question: In git switch --create exercise networkx-2.6.3, how do I find that I should use networkx-2.6.3. I get that you say it, but how to find the alternatives?
Ahh, "git tag"
    - you can use git status to check what the current state of the repo is
    - at the beginning you should be on the version that is tagged networkx-2.6.3

22. . How do I fix the error - Python was not found; run without arguments to install from the Microsoft Store, or disable this shortcut from Settings > Apps > Advanced app settings > App execution aliases.
    - that looks like you are trying to execute python, which is not installed on your machine. You can install it, but it's not required for this exercise.

23. When using vscode on Windows, it looks like the terminal does not have a pager available: doing `git annotate -p` still prints the full content to stdout. How can I get a pager? Is this related to the selected terminal option in vscode, which one would be preferred?
    - If the output of git commands does not get through a pager, you can still do
      ```
      git <git-subcommand and options> | less
      ```
      that is , add a `| less` at the end of your command. `less` is a standard pager, and `|` is a way to connect the output of the previous command (the git command) to the input of the next command (here, `less`)
      - That didn't worked for me on Windows. I used the following code and then it worked: 
        ```
        git <git-subcommand and options> | code - --wait
        ```
      - On windows, if you use Git Bash, the trick with `| less` should work. But if you are using Powershell, a different approach might be required as PS uses a different syntax than bash.



24. When trying to switch to a new branch with given hash with "git switch --create just-before 90544b4fa~1" i get a lot of messages like "Deletion of directory '.circleci' failed. Should I try again? (y/n)". Is this normal behaviour in vs code?
    - It shouldn't be normal, but I'll be hard for us to figure out the problem.  It seems to think that a directory can't be deleted (this would happen when switching to another commit: it will delete anything that doesn't appear in the older commit).  And somehow, it gives an error here.
    - If it doesn't let you go further, it might be something to ask a local person to look at.
    - Is there anything interesting about your setup?  Shared computer?  Network drive?  Multi-user accounts?
    - I think it is because I am using Onedrive... Sorry for that:)
    
25. Explaining bisect is going tooooooo fast!!! Please make sure to speak what you are typing. Not speak about one thing and write different things in shell. It's confusing and hard to follow! +1+1+1+1+1
    - Sorry, this was not intended to 'spoil' the exercise but as a quick overview that you did not need to follow in detail.
    - Do you need more detail on anything?
        - No worries. Maybe then you could just briefly repeat the biscet in 5 senteces, without examples.
            - sure

26. If I understood correctly when creating a branch pointing to a specific commit (via HASH) the whole code in the branch goes back to the specific date the commit pointed was created. Is that right?
    - If I understand the questions correctly: yes.


First briefly going over bisection a bit more:

## Sharing your work
Currently displaying/discussing: https://coderefinery.github.io/git-intro/sharing/

### Exercise until XX:30
https://coderefinery.github.io/git-intro/sharing/#exercise



27. I get the message "A Git repository was found in the parent folders of the workspace or the open file(s)." I'm working in VSCode, can I do this in the terminal?
    - In the terminal: you can check if you are currently inside of a git repo with `git status` before you `git init`.
    - well, that means that your folder is already in a git repository
        - I made a new folder on my desktop...
            - if you want a graphical way: use a file browser (e.g. windows explorer on windows), go to your desktop folder and check if there is a .git folder in there. If so, and there is not a VERY good reason why you need it that way, delete that .git folder and start over (don't delete your desktop folder though ^^)

28. Can I configure both github and gitlab in VScode ? 
    - yes, where you push to and pull from is called a remote. You can configure pretty much arbitrarily many remotes. To add an additional remote, you can ctrl+shift+p and type `remote`, then you 
    - in the terminal it's `git remote add <name> <url>`
    - in VSCode, if you want to add another remote to the repository, you need to click the three dots beside repositories on the source control tab, then select remotes--> add remote, this will give you a pop-up where you can enter the remote address, after it should ask for a name
            - Will try
        

29. In VS Code, when adding a new file to a new branch, just before merging to the main, appears the "Sync Changes" button. When is the right time to click that button? For example, in the Local work lesson notes, in the solution at (6) Merging branches locally screenshot appears that button, what to do then?
    - You should see that button if your local repository is connected to a remote repository (e.g., on GitHub) that might have changes that you do not have locally. If you were working with a remote repository that you are the owner of and you did not make any changes  to, then you should not see that message. If you connected VSCode to a remote repository that was changed by someone else, then you should see that button.
    - You should sync changes as often as possible, but make sure your work is committed first. Conflicts might appear.
    - (asking if someone else has more experience with VSCode)
        - It makes sense, thanks!, it was a repository clonned fro GitHub, I made changes locally (new branch, new file) just before merging the button appeared.


30. . I am using command line. At the step: git push -u origin main
    I get asked for my username and password. When I fill these in I get "remote: Invalid username or token. Password authentication is not supported for Git operations."
    - It looks like an authentication issue. Are you using  https or ssh?
    - I am using ssh. But I needed to create an Personal Access Code. Sorted now. 
    - ssh should not work with Personal access codes, but with SSH keys. You can see how you configured your repository with the command 
      ```
      git remote -v
      ```
      if the output contains `git@github.com`, then your repository was set to use SSH and you need to set up ssh keys on github for that to work; if instead the output contains `https://` then it was using HHTPS and you should be able to use access tokens for that
      - Yes 'git remote -v' says I am using https. Is there a way to edit it to ssh?
      - Yes, you can use
        ```
         git remote set-url <remote> <the "ssh" url you get from the "green code button" on the front page of your repo>
         ```
         where `<remote>` is typically just `origin`.
     -Thanks!



31. Will we get haunted by Linus Torvalds if we use a GUI-based version of git?
    - Heh.  We should be beyond that, everyone needs git these days and you don't have to be an expert.  Do what is useful to you (for each particular problem) <= That is good to know :)
    - Most of us mix different UIs depending on the need.

32. How did people do version control before git?
    - There were various other similar programs.  cvs (very old), subversion, mercurial, bazaar, many more.  In some ways it's nice to have one common tool now (if only the user interface was a bit nicer...)

33. What about other IDEs, I am using R Studio (using R :) and am a bit hesitant to switch to VS Code. I'm sure Git also works in R Studio, do you have any comments about differences or even suggestions where should I go?
    - For "does X work with git" the answer is usually yes.  I don't know details but I checked and it has the main operations.  I'd either look in the menus (now you know the terms so you can understand what to use), or a web search.
    - For all these, if the UI can do most, you can always drop to command line for very advanced things.
    - And +1 for using what you already use.

34. If you're using several computers, you should probably put the home directory for your local Git repositories on a local folder and NOT on some kind of synced network drive like OneDrive?
    - Yeah, probably best not to use a cloud-drive type of syncing.  Many small files there may not work too well
    - A high-performance network drive like used for workstations or HPC clusters is probably OK.
    - Important is to be very careful if it can be edited from multiple places at once in the cloud drive.  I coud imagine some stuff could go wrong there.  (of course Github/Gitlab/etc is the syncing mechanism for multiple people working, we'll see that tomorrow).

35. There is software herritage - which is archiviing all github projects - https://www.softwareheritage.org/, you recive there also PID (similar as from Zenodo).

:::info
### Break until xx:58
Then a session of practical advice: you can hear what us instructors actually do on a daily basis, what tools we use, how we treat small projects different than bigger ones, etc.
:::

36. One of the presenters was able to see in which branch he was on his command line interface (it was in a parenthesis next to his username). How can i do the same for my command line interface?
    - different shells can be configured to do that. If you use zsh as your shell instead of bash, it comes out of the box (and it is further configurable). In Bash I am not sure you can do it (there is a way but it is a little cumbersome)
       - If you really want to do that in bash: you need to change an environment variable called "PS1", which is a pattern that dictates how your prompt looks like. 
       - This is an example: https://askubuntu.com/questions/730754/how-do-i-show-the-git-branch-with-colours-in-bash-prompt , it requires changing your bash configuration files so that the PS1 variable is modified.
    - I think Git Bash for Windows offers this also out of the box
      - true
    - thanks guys, i will look into it then : )
      - before you change your .bashrc (and so your bash settings), you can try copy-pasting this in your terminal (the effect will vanish when you close it):
        ```bash
        parse_git_branch(){
        git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
        }
        export PS1="\u@\h \[\033[32m\]\w\[\033[33m\]\$(parse_git_branch)\[\033[00m\] $ "
        ```
        
     - I sourced this in my bash and it works perfectly. thank youuuu
       - Happy to help. But be careful about running code found on a remote corner of the internet on your terminal :-) <= but people can always be trusted, no :(

## Practical advice

Practical advice: How much Git is necessary? 
https://coderefinery.github.io/git-intro/level/

37. What about using AI to write commit messages?
    - Personally, if the person who presses enter for that commit message has reviewed and read the AI message, I am fine with it. (double work?)
    - I'd usually say, if it's long, why get AI to write it now if a better AI can later tell me about it?  Maybe for a one-line summary, but that's short enough I can do it.  If I don't care, I'll just say "changes" or something.
    - The point "why it changed" being more important than what changes is probably better here.

38. I would add: commit messages can be changed afterwards! (though, this practice should not be abused...)
    - Changing commit messages would change the history.  Changing the latest commit  before it's pushed is something I do all the time, but it shouldn't be a thing for old commits.

39. To edit code is it better to make a branch and do edits there, or directly on Main?
    - choose the simplest workflow that satisfy all the requirements of your organization/team.  +1
    - Often, if you are modifying a complex software you do not want to commit directly to main, because you want to have the pull request/review mechanism to have feedback on your work (that can be automatic feedback -e.g., a suite of automated tests - or feedback given to you by humans). But ideally you should try to merge often (that's what Continuous integration is about)
    - Yes, start simple

40. "A GitHub private repository is just a public one waiting to happen." Enrico Glerean :)

## What to avoid
https://coderefinery.github.io/git-intro/what-to-avoid/


41. In https://coderefinery.github.io/2025-09-09-workshop/certificates/ in question 3, at the end it says that we should reflect on the content of the 6 days. Okay i stop writing you got the better of me :)
    - Oh yes this time they are 9 days :) (I will fix it. We used to have longer day 4 which now becomes shorter day 4 + shorter day 5, and so on)

## Feedback, day 2

:::info
### News for day 2 / preparation for day 3
- We covered everything as covered in the schedule
- Tomorrow, we show how projects with multiple people would work: both a small group like your own team (centralized), and bigger projects (decentralized, not everyone has direct access).  It's probably the best day.
- Preparation for tomorrow:
    - If yesterday and today worked, you are probably good for tomorrow (Github connection is very important)
    - But **you need to request access in advance** - this will give you access to projects we work on tomorrow.  Check your email for instructions.
    - It's also like extra practice for everything we have done today.
:::

Today was (vote for all that apply):
- too fast: 
- too slow: o
- right speed: 
- too slow sometimes, too fast other times: ooooo
- too advanced:
- too basic:
- right level: oo
- I will use what I learned today: oooooooo
- I would recommend today to others: oooooo
- I would not recommend today to others: 

One good thing about today:
- No "too small font" issue today, thanks for fixing this :) 
- Conceptually everything was clear to me and I understood the relevance of what we were doing
- I like the discussion and good to know there are multiple ways to do stuff
- Yes discussion helpful, when you respond to questions
- After yesterday and today I feel good about it and ready to use Git.

One thing to improve for next time:
- Maybe it would've been helpful to sprinkle the practical tips in between the exercises, as an anchor to make the context clearer and improve pacing +1
- it would have been useful with a proper explanation of all the terms being used such as staging etc as it was not covered yesterday. +1
    - Does this help?:  Maybe we should show it more. https://coderefinery.github.io/git-intro/reference/
    - Yes! but would also help if the instructors explain it quickly when they go through so you understand the context
- Make sure presenters speak loud and clear (it was rather good) but avoid ocassional fast mumbling words (as if speaking for themselves).

Any other feedback?
- I was able to follow along with the 'how to turn your project to a Git repo and share it' following the VScode instructions fine, but got lost with the Rstudio version. I think there may be a step missing linking the github account with Rstudio or I've missed. 
    - Update on this - i needed to use the SSH key on the branch step (i was trying to use the https)
- It would be good to have some cheetsheet at the end with most important commands and explanations, easy to remember or visaulise. +1
    - We have! Cheatsheets are here: https://aaltoscicomp.github.io/cheatsheets/git-the-way-you-need-it-cheatsheet.pdf
    - More cheatsheets at https://aaltoscicomp.github.io/cheatsheets/
- hey. XXXXXXX here. Thank you so much for engagement. I really appreciate it ;) im learning a lot.  P-S Why my font color doesn't change??? heheh :)

General questions continued:
- I don't really understand the implications of using SSH vs HTTPS vs general URL. Why does it matter and what's the use cases?
  - the general URL does not provide an authentication mechanism, so you can perhaps pull/clone, but you might not be able to push. The HTTPS authentication (which does use a URL, which is very similar to the plain URL) might be simpler to use, and since access token can be used provide different security guarantees than SSH, which tends to be very convenient if one has SSH keys set up on their account on their machine.
- Can I just use local version control for sensitive data? 
  - you can also store encrypted data in a repository. If it is encrypted, you can also push it to a public repository and it will be safe.
  - The 'remote' does not have to be github.com / microsoft / gitlab.com. You could have that the 'remote' is an ssh server at your university and when you push to remote you basically upload from your local computer, to the storage in the university server.
- If I made changes in code already but not satisifed to commit it to main, can it be added to a branch?
- Forgot to git pull/fetch before making changes, ALL THE TIME!!!
- Want to know more about rebasing with some real use cases and examples.
- Will we learn more about gitignore in the future? +1+1 +1
- If I have accidentally been storing files (and converting files...) inside my repository folder, can I delete this change history? I now have too many changes for my push to Github to succeed... (The error message is: fatal: protocol error: bad line length 197)


