+++
template = "page-with-toc.html"
title = "Questions and notes from workshop day 3 (Git Collaborative)"
+++

## Icebreakers :icecream: 

**If you could ask for any superpower (can be computer-related), what would you ask for?**
- Time travelling (not just with git)
- To able to code and speak in any Language +1!
- To be able to fall asleep whenever I need in whichever condition I am
- No need to sleep :smile: o
  - But I like to sleep!
- Mind reading
- Communicate with nun-human organisms
- Teleportation
- Ability to heal oneself
- Superintelligence (my own, not artificial)
- Flying


**In preparation for today, unless you are part of a team/classroom, have you opended an [access request issue in access request github page](https://github.com/cr-workshop-exercises/access-requests/issues/new?template=access-request.md)**

Yes: ooooooooooooo
No: oo
What?: o



## Questions

1. Question: In the program on https://coderefinery.github.io/2025-09-09-workshop/ the times for day 4 and onwards say 10.50 - 11:00 Icebreaker/connecting time, then 12-14:30 the topic of the day. Is it a typo that nothing is scheduled between 11 and 12?
    - Well spotted! Days 4-9 last only 2.5 hours, from 12:00-14:30 Oslo/Rome timezone. So the icebreaker should be at 11:50 CEST (10 minutes before it starts) 
    - And it is now fixed!

2. What it means to be a collaborator to the exercise repository?
   - you will see soon!

3. What if I asked to be a collaborator but now I am not sure if I can join?
   - it's not going to be a problem

## Collaborative distributed version control
Teaching material at https://coderefinery.github.io/git-collaborative/

In particular, now looking at: https://coderefinery.github.io/git-collaborative/concepts/

4. +1 This being the most fun day! It's also very good for future careers.

### Collaborating withing the same repository
Now looking at: https://coderefinery.github.io/git-collaborative/same-repository/

5. Apart from the context of this exercise, what would be another reason to generate a repo from a template and therefore flatten the history? Would it not be always better to keep the history as a way to follow the context of how a repo has changed and its philosopghy has changed through time and how we may contrubute to it?
    - A template could be, for example, some basic setup for a web site. This is not very relevant to the site you are building and is always the same. <- makes sense. Thank you!
    - If you keep the history, you can also attempt to merge. If you really want a new project, you might not want that.

6. Please go over again how to give collaborators write access in Github.
   - We can show you in the help room if necessary
   - Is it under access > collaborators?
     - yes, then you can "add people" there searching for them in various ways
     - I can see them in manage access, but not where to change read/write permission
     - Collaborators on GitHub have write access (to my knowledge)
       - digression: on GitLab, there's more granularity in access control
       - good to know
     - Ah, ok thanks :)
   
7. Should we work in command line or Github?
   - You can use Github for the whole exercise but if you prefer to do some of the steps on the command line you can do that as well.

8. How to review and merge someone's pull request? I have "Merging is blocked due to failing merge requirements" message +1
   - It might have failed the tests, for example it's missing a '## Ingredients' or '## Instructions' part?

9. Why can I not create a new branch? I can only switch branches... +1
    - Have you accepted the invitation to join the organization?
        - yes, but I also got an email later saying that I was canceled again - dont know the reason for that
        - try to open an issue at https://github.com/cr-workshop-exercises/access-requests/issues/new?template=access-request.md
            - dont worry, I ll just watch then

10. How to review and merge someone's pull request?  I have "At least 1 approving review is required by reviewers with write access."
    - Go to the pull request tab and choose a pull request you wish to review. Once you approved the review you can merge it.
    - We will go through the process after the exercise.
    - Done! Thanks! I forgot to review it.
 
 
 11. Are we supposed to publish/push the new branch to the remote?

:::success
# Exercise until xx:50
You can find the exercise here:

https://coderefinery.github.io/git-collaborative/same-repository/#exercise

*(don't forget about the zooom help room if you need help and you're alone)*

Progress report - add 'o' to the relevant option. You are:

- done: ooo
- stuck: 
- not trying:
- working on it: 
- waiting for recipe to be merged ;) ooo

If you are waiting for access to centralized-workflow-exercise, please create a new issue.

:::


12. I am working on command line. I've merged my new recipe. How do I make a pull request?
    - Pull requests are created on GitHub. (Other sites like GitLab and BitBucket have similar features.)
    - You should not merge from the command line, you should go to the pull request page of the repository (e.g. https://github.com/cr-workshop-exercises/centralized-workflow-exercise-recorded/pulls) and then create a new pull request.


13. In new recipe for lichen soup, fixes #97, GitHub says that it has not passed all tests because there is a problem with the Instructions section. I cannot find the mistake for the life of me. Am I blind?
    - Never mind, I found the mistake, I am indeed blind.

14. It seems that my issue (#100) was not closed automatically even though my PR was merged. Why is that?
    - To have an issue be closed automatically, one needs to have a commit which contains something like "closes #100" or "Fixes #100" in  the branch of the PR. 
        - My commit message was "This is the new recipe; fixes issues #100.". Shouldn't that work?
        - Perhaps the wording is not exactly correct. The complete reference is https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/using-keywords-in-issues-and-pull-requests
        - I think that you would need "fixes #100" and not "fixes issues #100"
        - Accepted keywords for automatically closing issues: https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/linking-a-pull-request-to-an-issue#linking-a-pull-request-to-an-issue-using-a-keyword
            - Ok, thanks!

15. With respect to question 9, how can one introduce these checks (e.g. ## Ingredients) up front?
    - GitHub provides an automation  feature called "github actions", that can be configured to do practically anything (within reason). See, for this repository, e.g. https://github.com/cr-workshop-exercises/centralized-workflow-exercise-recorded/blob/pasta-feta-spinach/.github/workflows/check-recipes.yml

16. Why is the check failed showing next to the recipe with a red cross? For a pull request. And how to fix it as the error is for python for another recipe (check_recipes.py)?
    - we will discuss this as the first topic after the break in one minute
    - Thank you. However, the error is showing for some other recipe for my pull request. 
The error is:
File /home/user/work/centralized-workflow-exercise/centralized-workflow-exercise/soups/lichensoup.md is missing a section: "## Instructions"
Error: Process completed with exit code 1.
      - The automated check is saying that there is no line "## Instructions" in your file. It is a silly test, but you got the idea.
    
    - My recipe is not the lichensoup and the pull request is for formatting the recipe which has been merged earlier.
      - You can correct the `soups/lichensoup.md` to fix the problem. You could open an issue named, for example "lichensoup does not pass test", and create a branch for that
    - So I can fix someone else's recipe?
       - Creating an issue first, mentioning the author of the problematic file (check with git annotate/git blame) is a good practice here.
       - Correcting other people's mistakes using the issue/PR mechanism is very common
     - Gotcha!
       - Issues and PR might typically come from different people (someone finds the issue, someone else knows the solution to the issue)
       - Someone is already fixing it :) https://github.com/cr-workshop-exercises/centralized-workflow-exercise/issues/100
       - But this is the real life scenario of untested code/code with errors being merge to the company's main repository. Usually on a friday afternoon.. (check the Read Only Friday)
     - In this particular case the code was merged without passing the tests
         - Yes, a hasty software engineer who wanted to leave early :) :+1:

17. Sometimes there is an error on the automatic check where it says that the formating is not respected, but if you inspect the file it is ok. What makes the check_recipes.py flag them as incorrect?
    - we will discuss this as the first topic after the break in one minute

18. (not good practice, but common): 10 line PR: reviewed for an hour discussing naming choices to extreme detail - 500K line PR: LGTM
    - I know the feeling :)
    - And I do hope people do not submit 500K lines PR (but with AI tools these days who knows...)
    - There might be power dynamics at play (someone will do that, but you can't tell them off)
        - Indeed! And the beauty of an open workflow is that you can infer the power dynamics in public. The Linux kernel git repository is full of these "dramas".
        
19. Any recommendation of using Copilot?
    - personal opinion: as with any tool, you should not use it to do things you cannot do otherwise, but you should use it to increase your productivity in the things you *can already do*. 
    - Long, but worth reading ["Here’s how I use LLMs to help me write code"](https://simonwillison.net/2025/Mar/11/using-llms-for-code/)
    - See also Allea code of conduct for responsible use of AI in research: https://allea.org/code-of-conduct/ (in short; you are still responsible for the result when using a tool like Copilot)
      - Thanks for the TL;DR!


20. In the exercise we created a branch. Does modifying a file work the same way for pull requests?
    - You can work on that branch (which might be already part of an opened pull request) and keep on doing changes to files and committing them. The pull request will show all the changes and when you are ready you ask for review and they merge. You can also turn a pull request into "draft" to signal to your colleagues that you are still working on it and that it is not ready for review.

## Practicing code review

Material at: https://coderefinery.github.io/git-collaborative/code-review/

:::success

## Exercise until xx:58
https://coderefinery.github.io/git-collaborative/code-review/#exercise


*(don't forget about the Zoom help room if you need help and you're alone)*

Progress report - add 'o' to the relevant option. You are:

- done: ooooooo
- stuck: 
- not trying:
- working on it: 
- waiting for recipe to be merged ;) oo

If you are waiting for access to centralized-workflow-exercise, please create a new issue.

:::

21. Guys my net died for a moment. what are we doing now?
    - See above. Come to the zoom if you are lost. :)

22. We are meeting back in 1 hour?
    - exercise for 25 minutes, then a couple of words before lunch break. Lunch break starts at the end of the hour.

23. Should we copy the repository again to our local drive (if we are working locally), since it was changed from the last time we worked on it?
    - It should be sufficient to run `git pull` (switch to main branch first for consistency with the others) 


24. Exercise is to review the code? But how?
    - Once a pull request is opened, you can review it by looking at the changes in it and writing a review. Come to the zoom room if you need help.
    - The link in the exercise was wrong, should be correct now.
    Can you please share here?
    - https://coderefinery.github.io/git-collaborative/code-review/#exercise

25. .I just try to clone the repo again ( https://github.com/cr-workshop-exercises/centralized-workflow-exercise) and it gave me the following error: +1
    ```
    error: invalid path 'new recipe : Carrot cake.md'
    fatal: unable to checkout working tree
    warning: Clone succeeded, but checkout failed.
    You can inspect what was checked out with 'git status'
    and retry with 'git restore --source=HEAD :/' 
    ```
    - So you just run on terminal "git clone URL"? (or via vscode?)
    - on terminal "git clone URL" +1
    - I have never seen such a message ...
    - Which folder are you in? Do you have write access to it?
        - Yes.
    - That repository has a file called "new reipe: Carrot cake.md". I guess you might have some automation in your bash (?) that checks the current files/branch. (not a good name for a file, spaces and bash are not best friends :))
    - Are you on Windows? Filenames with ":" are not allowed
        - Yep just tested it on Windows and it fails (in Linux it works). I will rename that file in the repo.
        - yeah I'm on Windows
        - We are fixing it by removing the file.
            - And it is fixed! (CarrotCake moved to desserts folder).

26. I cannot find that plus and minus symbol when I add a review :/
     - We will look at this on stream, it's easier to show than describe in text :smile:

27. this \pm feature for suggestions in code review is also available on GitLab 

28. What does the "Verified" tag mean?
    - it means that GitHub is reasonably sure that it was you (or whoever was claminig to be) making the commit, e.g. the person you defined with git config --global user.name / user.email matches. But GitHub will also add "verified" to any commit that was done through the web interface, because GitHub thinks to be reasonably sure that it  was you since you were logged in.
    - if you wish to verify your commits which were made locally, you need to use something called GPG to "sign" your commits and then use `git commit -S`. Note: this is an advanced technique and not often used in small projects.
    - For code that has a security aspect, this is important 

29. ![](https://notes.coderefinery.org/uploads/71fe8e32-df86-4e71-a5fa-acb7ce1b325d.png)
    what is the difference of these mains?
    - They are in different forks. Each repostiry has its own main branch (and other branches)
    - If there is a need can we merge those mains to the black one? 
        - Yes, when you create a pull request, you can choose which branch you want to merge.

:::success
## Break untill XX:00

:::

30. We never closed/resolved issues? Is it just clicking on a button or anything intereting to know about closing?
    - If a commit that is merged explicitly mentions some ["closing keywords"](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/linking-a-pull-request-to-an-issue#linking-a-pull-request-to-an-issue-using-a-keyword) the issue will also be closed automatically, otherwise you close it by clicking the close issue. 

31. How to prevent people from senindg unwanted pull requests?
    - You cannot stop people from creating pull requests on your repository. You could have an automation so that a pull request that does not follow certain criteria is automatically closed and rejected.


:::info

This morning we have collaborated on a single repository, creating pull requests from branches in the same repository.

Now we will have a look at the workflow you need to adopt when you do not have access to the repository where you want to change the code.

:::

## How to contribute changes to repos that belong to others

Material here: https://coderefinery.github.io/git-collaborative/forking-workflow/

32. Is there echo or only at me?
    - I do not hear echo
    - just me
    - The usual is two twitchtv windows open :) (once I had 3 :D)
    - excatly


33. How to fork with command line?
    - A fork cannot be done on the command line, you need to do that on GitHub (it's a GitHub concept).
    - You will be able to connect to the forked repository from the command line, though.
    - remember from this morning:
    ![](https://coderefinery.github.io/git-collaborative/_images/forkandclone.png)
     
34. When I commit my changes locally, I see there is nothing new and all updated, but how can I see if there was something done remotely on the repo which I need to take care or. Git status only shows these local changes right?
    - you will have to use `git pull` or `git fetch` to synchronize your local repository to the remote one ("pulling" the changes from the remote repository into yours). `git status` will then give you the relevant information  
    - Note that `git pull` and `git fetch` might update only the information on the branch you are on in your local repo
        - Is `git fetch` and `git pull` the same ? 
        - Does that mean I should always start my work by doing a `git pull` to get the latest updates in the remote repo and then start working?
            -  Yes, it is good practice.

35. What is the difference between Part of team/exercise room and Following on your own?
    - If you are in a team (in-person), the team lead creates a repository and you collaborate on it.
    - If you are not in a team, A. is the team lead :smile: the address to the repository is in the exercise description

36. When we create the issue in the upstream repo should we also assign ourselves to the issue or no since we will fork it this time?
    - Usually you can only assign yourself if you are in the team that develops the software. 
        - So now that I am supposed to simulate a scenario where I am approaching a project in which I am not a member, I might not assignmyself to make it realistic?
           - Correct. Since you are a member of cr-workshop-exercises, you probably can assign yourself, but usually you cannot.

:::success

## Exercise until xx:50

Exercise is here:
https://coderefinery.github.io/git-collaborative/forking-workflow/#exercise

*(don't forget about the zooom help room if you need help and you're alone)*

Progress report - add 'o' to the relevant option. You are:

- done: oooo
- stuck: 
- not trying:
- working on it: 

:::

37. So after I merge changes on the branch of my fork, I need to create a pull request for the main branch for approval ?
    - You can create directly a pull request from a branch on your fork to the main branch of the original repo. But yes, in order to get your changes integrated in the main branch of the original repo you need to create a PR for approval.
    - Cool. Thanks!

38. Should we click to merge when our request has been approved or should we wait for another person to do it (one of the managers of the repo we want to contribute to)?
    - If you are not one of the managers, you cannot actually merge. In the exercise, you are one of the managers. It's still usually not recommended to merge your own pull request.
        - Ok then I will play it by the book and will not personally approve it and wait for someone to do it :)
        
39. In "files changed" how to get the side by side view of the previous and changed file? I only see one with red/green highlights
    - you could use the "compare" function by adding "/compare" at the end of the url in the browser, and then compare the branch you want to merge into main with the main branch

40. Is there a way to add folders from GitHub web interface?
    - you cannot create an empty folder but you create a file in a not-yet-existing directory by typing the full path to it, e.g. `directory-i-want-to-create/filename`

41. I made a branch, merged it back to my main fork and then did a pull request back to the original repo. This pull request has not been merged yet. In the meantime I decided to make a new addition, so I made a new branch, merged it with my main fork and then pulled request to the original fork. Problem is, the issue of the second pull is deemed already closed, even if I do not see the new pull in the pull requests of the original repo. How did this happen? Actually I just checked and the new pull was grouped with the first one... WHy did they not count as 2 separate ones? I see, makes sense then
    - This is a bit complicated, but one possible problem: A pull request connected to a branch, in this case your main. If you change the main branch, that changes the content of the pull request.
    - So it should not be possible to create two pull request from the same branch to the same upstream branch. If you created a second one, that was probably from a different branch.
        - So the correct way would have been to either make sure I have merged everything in my main branch before issueing the pull, or pulling through 2 distinct branches to make sure the issues are not clumped together?

42. Should I make a draft pull request or create pull request? 
    - you can create a normal pull request

43. Is it possible to tag the issues from upstream repo, when pr from the forked repo?
    - yes you can tag the issue in the upstream repo with #issue-number

:::success

## Break until xx:02
:::

43. When we modify our own fork, and in the meantime the original repository is also changed, when we see that the original is let's say 2 commits ahead. When we sync, do the changes in the original repo and in our fork blend together?
    - In simple cases, the branches in the fork will update to the ones in the original repository. But in more complex cases you might have conflicts, or a merge commit might be needed, and in that case the "sync fork" button might not work and you would need to do a proper merge (via PR, for example).


## Feedback, day 3

:::	success
### News for day 3
- We covered everything as scheduled
- The format for part two is changing: once a week, 2.5h. They are more like self-contained workshops under the theme of reproducibility and good research practices
- **Day 4** (Wednesday 17/Sep 12:00 CET) is **all about reproducibility!** From the reproducibility crisis, to good data and code  (and the whole computer!) management.
- Remember to setup conda for the next days if you plan doing the exercises https://coderefinery.github.io/installation/
:::

Great. :))

Today was (vote for all that apply):
- too fast: 
- too slow: 
- right speed: oooooooooo
- too slow sometimes, too fast other times: 
- too advanced:
- too basic:
- right level: oooo
- I will use what I learned today: ooooooooooooo
- I would recommend today to others: oooooooooo
- I would not recommend today to others: 
- Amazing! oo

One good thing about today:
- This was amazing! and yes, really fun to collaborate!
- Great support and clarity on answering questions!
- Very informative and instructors did a great job explaining new concepts.. thanks! +1
- It was fun to collaborate together with people around the world! :) +1
- I learned a lot and it was also fun to do the exercises! It made all these concepts really simple to me. +2
- I learned something :) +1
- After three days, it all comes together. +1

One thing to improve for next time:
- I guess the speed and accent, but maybe captions can help!
  - Youtube will have captions :smile:
- More examples on how to use VS code :) How to create all this on VSCode and less on Github webpage
- I liked having the test failing, but maybe add how to solve a conflict next time.


Any other feedback?
- I found a good overview to using Rstudio with some of the concepts covered this week in case it's helpful for others https://aberdeenstudygroup.github.io/studyGroup/lessons/SG-T1-GitHubVersionControl/VersionControl/
        Thanks!
- Thank you for the workshop!

General questions continued:
- Will there be exercises (or just lectures) next weeks and do we need to prepare something?
  - There will be exercises! (link with planned exercises: https://coderefinery.github.io/2025-09-09-workshop/exercises/)
- Can you please share the link/requirements for certification? Thank you!
    - https://coderefinery.github.io/installation/
- Will the information on reproducibility be language agnostic?
    - We try, but for the purpose of showing/exercises we use Python. 



