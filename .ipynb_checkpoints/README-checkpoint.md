# Introduction

This tutorial & exercise, initially developed in 2024, is designed for trainees interested in joining the lab directed by Dr. Suzanne Leal in [Center for Statistical Genetics at Columbia University](https://www.neurology.columbia.edu/research/research-centers-and-programs/center-statistical-genetics#:~:text=We%20are%20a%20group%20of,statistical%20genetics%20and%20genetic%20epidemiology.). It reflects our expectation of your computing skills with R and Linux shell commands, and hopefully your ability to learn new tools in bioinformatics and related fields as well. In completing these exercises, you will first set up the computational environment on your computer then perform some small scale data analysis using test data. However, it is important to point out that after joining the lab, most of the research requires access to high performance computing cluster in Linux, on large-scale data such UKBiobank and All of Us data.

Applicants are recommended to have experience with one or both of the languages we mentioned above, but we believe that the learning curve for things you are not that familiar with (but required in this exercise) is reasonable. You are encouraged to search online for learning new tools, and even to ask ChatGPT if necessary, as the ability to search for answers and solve problems itself is also required in our lab. However, if you run into a major issue as you go through the material, please do not hesitate to contact me (Rui Dong, rd2972@cumc.columbia.edu). (When you do so, please describe your question clearly and provide all the information necessary for us to help you.)

## Task 1: Unix command shell and install softwares

We assume you are comfortable with command-line interface (on Linux or Mac). In this task you are going to work with `git` from command shell, set up the computing environment, and install basic softwares and packages needed for data analysis of Tasks 2-3.

### Git

Most of our work will be saved and shared on github in public or private repositories. If you have not used git in the past, please follow the [instructions here for a 5 minutes git tutorial](https://wanggroup.org/orientation/5m-git).

As the next step, please [fork](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/fork-a-repo) this repository and clone it to your computer. Then, add your name to the Markdown file named `hello.md` and commit it to github with a customized commit message, e.g., "Add my name and github handle". Lastly, [create a pull request](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/about-pull-requests) so we can see your update and incorporate it to the repository.

### Markdown and shell

Create a new markdown file (using any text editor you prefer) named `research_shell_JohnSmith.md` (replace `JohnSmith` with your name), and create a section about any research project that you have been working on, with at least two subsections, some links, *Italic text* and **bold text** (to highlight some important content) and at least one table or figure. The content of the report willl not be considered in the evaluation, but it is important to make sure it is well structured and formatted, and written in clear English. This section should be ~300 words.

In the same markdown file, create a second section with your answers to the questions about shell commands in `notebook/shell_questions.md`. If the answer is a code, put it in a code chunk in markdown.

### Install softwares and setup computing environment

You will need to have [jupyter notebook](https://jupyter.org) installed to run the analysis, and the two main notebooks are both in [`R`](https://www.r-project.org) (task 2 and 3).

You can either install jupyter notebook directly or install other tools such as [anaconda](https://www.anaconda.com/download) or [micromamba](https://mamba.readthedocs.io/en/latest/installation/micromamba-installation.html). As long as you can run a jupyter notebook, you are good to go!

After you setup the computing environment, please append your name to the notebook filenames such as `FineMapping_JohnSmith.ipynb` and `MendelianRandomization_JohnSmith.ipynb`.

## Task 2: Fine mapping analysis to identify true causal variant in complex traits

The first notebook, `notebook/FineMapping.ipynb` is an exercise with the `susieR` package in R. This is somewhat advanced material for those who has a background in statistical genetics.

### Summary of the SuSiE method
Please add another section in the notebook after where you put your name, and make the section title "Summary of the SuSiE method". Then take a look at [this paper](https://academic.oup.com/jrsssb/article/82/5/1273/7056114) before you run this notebook to know some basic concepts that we might mention. Please then summarise the SuSiE method in a paragraph and describe what it does. You are supposed to summarize it yourself instead of copying content from the abstract directly. You can start the summary after reading the paper but you may also understand it better after you run the notebook. Feel free to come back and edit this section any time.

Please note that you can use ChatGPT or other tools to help you understand the method, but make sure you understand what you write here -- we may ask you questions based on your response during the interview.

### Run the notebook

Please follow the instructions in the notebook, and run all the cells. Answer the questions within the notebook directly and keep the code (that you use to get the answer) instead just leaving the answer there.


## Task 3: Two-sample Mendelian Randomization

The second notebook, `notebook/MendelianRandomization.ipynb` is an exercise with the `MendelianRandomization` package in R. In this notebook you will find fewer examples of code. To go through the analysis you will need to write more of the code on your own. Feel free to use ChatGPT or any tool you can find, but again please be sure you understand what you are doing here. The concepts of Mendelian Randomization are relatively easy to follow, and at the end of the notebook there is an bonus question where you can visualize the results. Please follow the instructions in the notebook and answer the questions with the code. 


## Task 4: Report your work and submission

Organizing and communicating your work with others is essential to your success in conducting reproducible computational research. After you have completed all the tasks above, please make a tarball of the markdown file and two notebooks and email it to `rd2972@cumc.columbia.edu` for us to review. Please make the email subject as "Complex Traits Research Assistant Application: Exercise Submission".


