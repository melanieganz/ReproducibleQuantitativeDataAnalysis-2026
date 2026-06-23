# ReproducibleQuantitativeDataAnalysis-2026
Repository for the UCPH SCIENCE PhD course Reproducible Quantitative Data Analysis 2026

My own file

# ReproducibleQuantitativeDataScience

A course prepared by Dr Melanie Ganz and Dr Cyril Pernet and guest speakers, e.g. Michael Hanke. The course structure is over 5 days plus personal work: 2 days, course work, 2 days, course work, and 1 day with presentations.

During the course, active participation is expected. In session 1, we'll use [padlet](https://padlet.com/dashboard) to interact with each other (anonymous posting allowed) and also do group work. In session 2, we use GitHub (that you learn in session 1) to share code and review each other code. It is recommended to share something you are working on, but if you feel uncomfortable with that, prepare something to be shared/reviewed. In session 3, you must present in front of everybody. While it may feel uncomfortable, it is expected from any PhD student to be able to do so, and not just for this course. In general, there are no rights and wrongs in trying to improve reproducibility, it is only expected that you try given the conceptual and practical tools presented.

## Part 1

### Day 1 - Data Collection and data storage

- Introduction to reproducibility: Definitions and origins  
- How do you store data on your computer? Data structures and data naming  
- Data provenance: keeping track of where data are coming from  
- Reproducibility is hard: [case studies](http://www.practicereproducibleresearch.org/core-chapters/4-casestudies.html)

### Day 2 - Reproducible designs, protocols and pre-registration

- Concepts and tools for protocol documentation, and study pre-registration
- Data Privacy, Ethic and GDP - lecture and practical case reviews 
- Using markdown see [cheat sheet](https://www.markdownguide.org/cheat-sheet/) for documentation - practical  
- Version control and social coding with Git -- people who know can pair wih newbies

### Course work

Using your PhD research data, protocol, code, etc, write a report explaining from where you start, and which measures are already in place to increase reproducibility as per concepts presented during days 1 and 2. What measures can be taken to increase reproducibility and if any, why some cannot be implemented? (page count 2 to 3)

Submit your coursework via e-mail to Cyril and Melanie.

## Part 2

### Day 3 - Better coding 

- Programming
- Good coding practices
- An introduction to computational analysis methods: permutation, bootstrap, cross-validation, out-of-sample generalization

### Day 4 - Better analyses 

- Feedback on coursework and discuss further issues to make your PhD reproducible and next assignment
- P-hacking
- Understanding p-values 
- Computational reproducibility

Please prepare before the course:
- [Installing UV](https://docs.astral.sh/uv/getting-started/installation/#installation-methods) 
- Install the gitannex typing in a terminal ``uv tool install git-annex`` and then ``uv tool install datalad --with datalad-next --with datalad-container`` (or if datalad was installed ``uv tool upgrade datalad --with datalad-next --with datalad-container``). Finally make sure to activate a uv-based DataLad installation: on Mac/Linux: ``source $(uv tool dir)/datalad/bin/activate``, on Windows (cmd.exe) ``AppData\Roaming\uv\tools\datalad\Scripts\activate.bat``. Further checking and instructions can also be found [here](https://slides.edu.datalad.org/modules/installation.html#/).
- You should already have VSCode from the last session; otherwise, [install it](https://code.visualstudio.com/docs/copilot/setup) **with Copilot AI**.
- Clone this repository: git clone https://github.com/poldrack/ai_testing.git and run uv sync with repo directory
- [install docker on your own machine](https://docs.docker.com/engine/install/) so you can use a container and then build a container.


### Course work 

Improve code you are using based on the concepts and tools reviewed over the 4 days: from version control and better inline documentation, to functionalization and modern computational statistics.  
Make a 10 minutes presentation summarizing all of your course works and what measures you have taken to improve reproducibility in your PhD (including work from session 1). 

## Part 3

### Day 5 - Data sharing 

- The ‘data’ cycle, sharing from raw data to figures - lecture  
- Copyright and Open Access in publishing - Lecture by Rasmus Rindom Riise from the Royal Library
- Reproducible publishing [see example here](https://preprint.neurolibre.org/10.55458/neurolibre.00014/) - Lecture by Nikola Stikov from University of Montreal (remote)
- Presentations and discussions/social event (incl. drinks and pizza)

