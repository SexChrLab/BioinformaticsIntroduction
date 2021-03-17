# Bioinformatics Introduction

Here we compile our best practices for introducing new trainees to computational biology.

This includes links to codes, trainings, and other useful computational resources.

## 1. Introduction to command line
For any work we will do as computational biologists it is exceedingly useful to understand that there is a way of interacting with data via the command line. 
Many students have found it useful to start with the tutorial:

		https://www.codecademy.com/learn/learn-the-command-line

Now that you've tried out the command line in a browser, let's see how it works on your computer. 

#### 1. Mac: Accessing the command line

If you have a Mac, you actually have two operating systems installed. You have the Mac operating system that you typically interact with, and you have a Unix operating system that you can interact with via the terminal. To find the terminal, you can go to Applications > Utilities and find the application called "Terminal.app". The pathname (remember our Command Line tutorial above) is: /Applications/Utilities/Terminal.app Double click on Terminal.app. You are now in the Unix terminal on your Mac machine. 

#### 2. Windows: Accessing Linux-like command line
If you are on a Windows machine, you can install MoabXterm, a Linux-like environment that will allow you to run basic Unix commands and to SSH/SFTP. You can install it from here:

		http://mobaxterm.mobatek.net

#### 3. Unix/Linux Tutorials 
Now that you have access to the shell/terminal on your computer, you can run through additional tutorials. Students in the lab have found these tutorials useful: 

		Learning the shell
		http://linuxcommand.org/learning_the_shell.php

		UNIX Tutorial for Beginners
		http://www.ee.surrey.ac.uk/Teaching/Unix/

## 2. Text editors
Throughout your coding, you'll want to use a text editor to write and read your code. While Word or Pages are easy to work with, they add invisible characters and are not saved in a format that can be input into other programs easily.

If you like to work in the terminal you can use terminal-based text editors like vi/vim:

		http://www.vim.org/

Alternatively you may want a GUI-based text editor, like Sublime: 

		https://www.sublimetext.com/

Or Atom:
		https://atom.io/

## 3. Introduction to python
There are many different languages that we can write code or scripts in for analyzing our data. One of the most commonly used langauges in bioinfomatics is python. The tutorial at codecademy can help you get started with learning python syntax, though there are many other places to learn coding in python.

		https://www.codecademy.com/learn/learn-python-3

For advanced python, you can run through the Python Data Science Handbook: 

		https://github.com/jakevdp/PythonDataScienceHandbook

For visualizing what your python code is actually doing: 

		http://pythontutor.com/visualize.html#mode=display

## 4. Introduction to R
Other than working within the terminal (command line), and writing codes in python, the other key component to doing bioinformatics is being able to do statistics. For our lab, nearly all the statistical analysis we do will be in R. R is a "free software environment for statistical computing and graphics": https://www.r-project.org. 

Here is how you can obtain R and R studio (a user-friendly environment for running R):

		https://www.youtube.com/watch?v=dRH-SasnzzU

Similar to python, there are many tutorials for R, but one that many trainees in the lab have found useful is: 
		
		https://www.datacamp.com/courses/free-introduction-to-r

Alternatively, Data Carpentry has in Intro to R course:

		http://datacarpentry.org/R-ecology-lesson/index.html

Here are videos for how to do basic computation in R, and basic programming in R:

		https://www.youtube.com/watch?v=3xriAzqc-fw
		https://www.youtube.com/watch?v=S6EVGoV8PpU		

For advanced R practice, you can run through R for Data Science: 

		http://r4ds.had.co.nz
		
R for Data Science solutions are available here:

		https://jrnold.github.io/r4ds-exercise-solutions/

Or you can work in R studio using the swirl R package: 

		https://swirlstats.com/students.html

## 5. Introduction to SSH and SFTP
For many of the types of analysis we do, you won't be able to run the analyses on your local computer. Instead, you'll need to access a computer cluster. 

First, you'll need to make sure you have an account. For WilsonSayres lab members, please request an account on ASU Research Computing: https://researchcomputing.asu.edu 

Second, you'll need to know how to get there.

SSH is the Secure Shell protocol (so, how to access your account on the cluster and run in the cluster environment). 

Here is a tutorial for how to access the ASU cluster via SSH:

		https://cores.research.asu.edu/research-computing/user-guide#connect

You may also want transfer files to/from the server. There are many ways to do this, but SFTP (Secure File Transfer Protocol) is one way. You can use a variety of tools, including MoabXterm (from above), the SFTP command line tools (https://linux.die.net/man/1/sftp), or a GUI-based SFTP program (people in the lab like FileZilla: https://filezilla-project.org and CyberDuck: https://cyberduck.io - both work for Mac or Windows). 

## 6. Batch scripts
Once you have an account on the cluster, you'll want to be able to run jobs. You may be tempted to run large jobs directly after logging in... don't. This is because of the typical strucutre of a cluster. Typically there is a login node where everyone goes when they log in to the cluster, and compute nodes, where most of the computation happens. To submit jobs that will need a lot of time or memory, you'll need to write a batch script to submit your job into a queue to run on the compute nodes. Trying to run large jobs on the login node will usually result in an error and a warning message. To get your jobs to run, you'll need to make a batch script. 

A batch/job script for SLURM (the Simple Linux Utility for Resource Management) will list information about who is submitting the script, how long it will take, what kind of memory it requires, if it should go in a special queue, and then the commands to run your script or program. 

Here is a SLURM command creator:

		https://marylou.byu.edu/documentation/slurm/script-generator

And here is a SLURM Quick Start Tutorial:

		http://www.ceci-hpc.be/slurm_tutorial.html

Here, you will find a tutorial on making and submitting a sbatch script on Agave:

		https://github.com/SexChrLab/BioinformaticsIntroduction/tree/master/BatchTutorial

## 7. Git and Github
Finally we get to the page you're actually on! Git and Github (while separate) are often used together to organize code for projects, allow collaborators to contribute to the project, and most importantly, manage multiple versions of code/documents. We will use Git and GitHub for our projects in lab. While most of the commands are fairly straitforward Git/GitHub uses specific terminology that you'll need to familiarize yourself with. 

Here is an intro to Git and GitHub: 

		http://product.hubspot.com/blog/git-and-github-tutorial-for-beginners

Here is a "hello world" tutorial for GitHub (you don't need to know how to program to do this tutorial):

		https://guides.github.com/activities/hello-world/

And are some GitHub guides:

		https://guides.github.com

## 8. Secure File Transfer 
When you are working on a cluster, you will at some point want to transfer files from your local computer to the cluster or from the cluster to your computer. You can do this using SFTP from the command line, or using a SFTP graphical user interface too.  

Common SFTP GUIs are CyberDuck: 

		https://cyberduck.io/
And FileZilla: 

		https://filezilla-project.org/

## 9. Snakemake 
One of the first rules of bioinformatics is that it is (nearly) always worth the time to make your analysis reproducible. Snakemake can help you with reproducible analyses. 

You can start out with this video: 

		https://youtu.be/8xnm_RKkycQ

And this tutorial:

		http://slowkow.com/notes/snakemake-tutorial/


## 10. R Shiny
It can be useful to create interactive plots for your data. One way to do this is with R Shiny.

		https://shiny.rstudio.com/tutorial/

## 11. Databases - MySQL
Sometimes you may want to create or interact with databases in R.

Here is an introduction in creating MySQL databases and querying them with R:

		https://programminghistorian.org/en/lessons/getting-started-with-mysql-using-r

And some information on R Shiny database basics:

		https://shiny.rstudio.com/articles/overview.html
