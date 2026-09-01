# ReproducibleQuantitativeDataScience

A course prepared by Dr Melanie Ganz and Dr Cyril Pernet, with guest lecturers: Dr Robert Oostenveld, Dr Michael Hanke, Dr Nikola Stikov, and Dr Russ Poldrack. The course structure is over 5 days plus personal work: 2 days, course work, 2 days, course work, and 1 day with presentations.

During the course, active participation is expected. In session 1, we'll use [padlet](https://padlet.com/dashboard) to interact with each other (anonymous posting allowed) and also do group work. In session 2, we use GitHub (that you learn in session 1) to share code and review each other code. It is recommended to share something you are working on, but if you feel uncomfortable with that, prepare something to be shared/reviewed. In session 3, you must present in front of everybody. While it may feel uncomfortable, it is expected from any PhD student to be able to do so, and not just for this course. In general, there are no rights and wrongs in trying to improve reproducibility, it is only expected that you try given the conceptual and practical tools presented.

## Part 1

### Day 1 - Data Collection and data storage

- Introduction to reproducibility: Definitions and origins
- How do you store data on your computer? Data structures and data naming
- Data provenance: keeping track of where data are coming from
- Reproducibility is hard
 
### Day 2 - Reproducible designs, protocols and pre-registration

- Concepts and tools for protocol documentation, and study pre-registration]
- Data Privacy, Ethic and GDPR - lecture and practical case reviews
- Using markdown for documentation - practical
- Version control and social coding with Git see the [quick sheet](https://github.com/CPernet/Quicksheets/blob/main/git_github/git.mkd) -- people who know can pair wih newbies

*Please prepare before the course*:

- install [git version control](https://git-scm.com/install/windows) on your machine
- create an account on [GitHub](https://github.com/) if you do not have one
- we recommend installing [GitHub desktop](https://desktop.github.com/download/). It usually also comes with git but we have seen some weird windows installation, so please check git bash is present on your machine
- not mandatory, but recommended (also used in the next section), is to install [VSCode](https://code.visualstudio.com/download), open it and sign in your github account.

### Course work

Using your PhD research data, protocol, code, etc, write a report explaining from where you start, and which measures are already in place to increase reproducibility as per concepts presented during days 1 and 2. What measures can be taken to increase reproducibility and if any, why some cannot be implemented? (page count 2 to 3)

## Part 2

### Day 3 - Better coding

- Programming
- Good coding practices
- An introduction to computational analysis methods: permutation, bootstrap, cross-validation, out-of-sample generalization
- Agentic coding. 
- Time to update your code - implement some of the practices discussed today using agentic coding, let's review each other work/discuss. Tip: don't forget to version control your code, makes it easier to see what the agent changes.

*Please prepare before the course*:

- Install python for [windows](https://www.python.org/downloads/) or [mac](https://www.python.org/downloads/macos/)
- Install pip (package manager for python)
- Install [VSCode](https://code.visualstudio.com/download), open it and sign into your github account.  Make sure agents are enabled in your VS Code settings. You can use Copilot for free by signing up for the [Copilot Free plan](https://github.com/settings/copilot/features) and get a monthly allowance of inline suggestions and AI credits. It helps to let VSCode run code in the terminal - depending on what admin rights you have - check [code.visualstudio.com/docs/terminal/shell-integration](https://code.visualstudio.com/docs/terminal/shell-integration).

### Day 4 - Better analyses

- Understanding p-values (see notebook)
- P-hacking your data
- Feedback on coursework and discuss further issues to make your PhD reproducible
- Computational reproducibility 

*Please prepare before the course*:

- [install docker on your own machine](https://docs.docker.com/engine/install/) so you can use a container and then build a container. For windows users, you need 1st to have the linux subsystem insalled (in power shell, type ``wsl-ext --install``)
- [install uv](https://docs.astral.sh/uv/getting-started/installation/) this is a package managment + virtual environment that plays well with python

### Course work

Improve code you are using based on the concepts and tools reviewed over the 4 days: from version control and better inline documentation, to functionalization and modern computational statistics.  Make a 10 minutes presentation summarizing all of your course works and what measures you have taken to improve reproducibility in your PhD (including work from session 1).

## Part 3

### Day 5 - Data sharing

- The ‘data’ cycle, sharing from raw data to figures
- Peer review
- Reproducible publishing
