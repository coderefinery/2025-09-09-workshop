+++
template = "page-with-toc.html"
title = "Questions and notes from workshop day 8"
+++

## Icebreaker

- What programming language(s) are you normally working with (add an o for your answer):
    - Python: oooooooooooo
    - R: ooo
    - Julia: oo
    - C++: oooo 
    - Fortran: ooo
    - Bash: oooo 
    - CUDA: o
    - HIP
    - (add yours here)...

- What does testing your code mean for you? How do you test?

    - Craft a dummy data set where i can easily follow what my code is doing to it and verify it is working well. +1
    - Test = automatic test: manual test -> too expensive -> do it too rarely
    - small tests are nicer to work with than big ones +1
    - big ones tend to be more useful but a pain to work with 
    - Run > fix error > run > fix error, etc. +1
    - Test examples and small features using CI capabilities on github
    - Test suite with Python unittest, and use a Github action to run it
    - (add your comments here)...

## Automated testing
Material: https://coderefinery.github.io/testing/


## Motivations
Material: https://coderefinery.github.io/testing/motivation/
Your questions and comments here:

1. How to (approximately) measure code coverage? If you have a function, and a single test invoking that funciton, you compute it as +1 function tested?
   - there are tools for that, that tell you "line" coverage and "function" coverage. "line" coverage is the ration between total code line of your program (excluded empty lines and comments) and lines that were executed during a run of the test suite. It's not a perfect metric of course (and be aware of Goodhart's law: https://en.wikipedia.org/wiki/Goodhart%27s_law).
   - function coverage is - I think - the ratio between functions in your code and functions that were executed during a run of the test suite.

2. After running pytest, i also got two directories, one called `__pycache__` and another called .pytest_cache. Could you comment a bit on their use and purpose?
   - `__pycache__` is a directory that contains files that python (not pytest in particular) produces during the execution, and might be reused later when python runs again, saving time (it can contain, e.g., bytecode-compiled python code and things like that). This is the general idea of a "cache"
   - `.pytest_cache`  is a cache directory specific to pytest
   - caches are not necessary, you can delete them and everything will work as expected, albeit a little slower because all the stuff in the cache might need to be recreated.

## Testing locally
Material: https://coderefinery.github.io/testing/locally/

:::info 
## Exercise - Until xx:54
Instructions: https://coderefinery.github.io/testing/locally/#exercise

Progress report... are you (mark with an 'o' or any letter):
- done: ooooo
- need more time:
- had major problems: 

If you have problems and / or want to talk, you might join the zoom help room (information on how to join it has been shared in emails sent in the past)
:::


3. In the excersise, when we change to "-", is there a way for pytest to test all asserts, i.e. not to stop at the first one that does not fulfill condition?
    - You could put each assert in its own test function.

4. Can this testing heavily influence complexity of code, when dealing with e.g. fancy ML/DL models? Is it demanding in processing?
    - Not sure I understand the question.
        - Ideally test are lightweight enough, that you can work with them interactively. So you can, quickly iterate quickly, code -> (compile) -> test -> fix resulting problems, repeat. That's not always possible, however. For ML models, you rarely run a full training that can take hours or days as a test as part of an automatic development pipeline. You do still evaluate your model of course, but not in the context of automated software testing 
5. How the testing works? Does it simply runs all functions even when they aren't called?
    - pytest - the framework we are using - inspects your files (even directories) and will find all the functions that start with `test_` or end with `_test`, and call them for you. If you tell pytest to "test a directory", then it will look for all files that start or end with "test". In this sense, we may say that "registering" a test just requires you to name a function appropriately.
    - in other languages one has to explicitly "register" tests using macros (see Catch2/Google Test approaches), and then the testing framework does the work of calling all the registered tests.

6. How it differs from "try"?
    - "try", for catching exceptions, is something that you expect to be used at run time, when your software is doing actual work, and is encountering an error that you want to manage (and you expect it to happen sometimes). Here, we are creating test cases - when we run test cases, we verify assumptions about how our software works.


## Automated testing

Material: https://coderefinery.github.io/testing/continuous-integration/

Will be done as a walkthrough: https://coderefinery.github.io/testing/continuous-integration/#continuous-integration

Please post your questions and comments here:
7. Bonus question: why is the job on Johan's github actions failing?
8. Would it make sense to split the github action job between those parts who succeeded and the parts who failed? They do different things, right?
    - It can, but since creating the coverage report requires running the tests, you would be running some things multiple times.

:::info
## Break until xx:38

:::

## Test design
Material: https://coderefinery.github.io/testing/test-design/

::: info
## Exercise until xx:02
Have a look at the list of exercises in this episode:
https://coderefinery.github.io/testing/test-design/

Suggestion: start with the initial ones, which are simpler
(and fundamental).

Progress report... are you (mark with an 'o' or any letter):
- done: 
- need more time:
- had major problems: 
:::

Questions, continued:

9. Design 3 solution throws PermissionError: [WinError 32] The process cannot access the file because it is being used by another process: 'C:\\Users\\M\\AppData\\Local\\Temp\\tmpd6relgrg'.
    - Could it be that the file is opened in an editor? Nope.
    - From the file path, I think it's a temporary file created in the test. It's really weird that the test does not have access to it. Is the same filename used in multiple tests, maybe?
    - I had the same issue, commenting the os.remove line worked for me, but I still don't understand the error. 
        - I confirm this.

10. How would I write a test to make sure the correct error is raised when an incorrect input is passed?
    - depending on the language/testing framework, there are different tools to do that. 
    - In python you can do something like
      ```
      try:
          your_code()
          assert False "Exception not raised"
      except ExceptionYoureExpecting:
          pass
      except Exception:
          assert False "Wrong exception raised"
      ```
      But for example in pytest there's a context manager (`with ....`)
      called "pytest.raises()", which does that job in a better way than reimplementing it yourself
    - other languages/testing frameworks have similar facilities that do this for you, even if you could write out the logic yourself 
        - Ok, many thanks! I had python (pytest) in mind, and raises() seems to be what I was looking for.

:::info
### Catch2 example, see https://coderefinery.github.io/testing/locally/

:::


## Feedback

:::info
We hope you got an impression what automated testing can be useful for and how it can be implemented for different programming languages. The lesson materials will continue to be available for reference. 

Join https://coderefinery.zulipchat.com/ to ask further questions and meet the instructors and rest of the team.

### Outlook for the next lesson: Modular Code Development
It will tie the whole workshop together and we will revisit almost all of the topics of the full workshop and apply them.
    - Great, looking forward.

:::

Today was (vote for all that apply):
- too fast: 
- too slow: 
- right speed: o
- too slow sometimes, too fast other times: o
- too advanced:
- too basic: 
- right level: oo
- I will use what I learned today:oo
- I would recommend today to others:oo
- I would not recommend today to others: 

One good thing about today:
- Great overview of different types of testing, and hands on practicals very useful +1
- Presenters were good, yet Oscar could try to type a bit slower (to ease the following). :)

One thing to improve for next time:
- Interesting topic, but I would recommend to devote more time, at least another hour or two, to go slowly and finish everything that is prepared.

Any other feedback?
- Maybe stick to one programming language (e.g. python), and devote extra day to other languages.
- How about having a topic on debugging and best practices of debugging?! I somehow lack that and miss that in the workshop.

