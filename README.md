01_Git_and_Intro
================

Practice with basic git functions, and intro to study of Data Structures

Reading
=======

**Version Control with Git, 2nd Ed**. Loeliger and McCullough. 

http://proquest.safaribooksonline.com/book/databases/content-management-systems/9781449345037/version-control-with-git/id302681?uicode=ohlink (Free access through www.lib.miamioh.edu, but limited to 100 simultaneous users across all OhioLink. I recommend downloading/printing the required readings ahead of time, just in case.)

Read only the following:

1. Chapter 1
  * Background
  * The Birth of Git
2. Chapter 3: Getting Started
  * Intro
  * The Git Command Line
  * Quick Introduction to Using Git (read all sections)
  * Configuration files (Intro only, may skip part on aliases)
3. Chapter 4: Basic Git Concepts
  * Basic concepts (read all)
  * Object store pictures
  * Git concepts at work (read all)
4. Chapter 21: Git and Github
  * Repo for Public Code
  * Creating a GitHub Repository
  * Forks
  * Creating Pull Requests
  * Managing Pull Requests
  * Coding Models

**Open Data Structures in C++**. Morin, edition 0.1G-beta

http://opendatastructures.org/ (Free access. I recommend downloading the PDF version.)

Read the following:

1. Chapter 1 (pp. 1-21)

Homework
========

1. Create an account with github.com. You may select the free account. If you want to get some free private repos, you may apply at https://github.com/edu
2. Go to https://github.com/MiamiOH-CSE274/01_Git_and_Intro and fork the repo, which will create a copy of it in your github account.
3. Install git on your computer, if you do not already have it. I recommend installing http://windows.github.com/ if you use windows, or http://mac.github.com/ if you use Mac. **HOWEVER, I highly recommend using the command-line tools for everything, and ignoring the GUI. I will not be providing help with configuring/using the GUI.**
4. Clone your repo from github to your computer. When you are at the web page for your repo, `https://github.com/[your github id]/01_Git_and_Intro`, you will see info about how to clone it. The easiest way is to go to the command line terminal, and type `git clone git@github.com:[your github id]/01_Git_and_Intro.git`
6. Complete the exercises below by modifying this file.
7. After you complete each answer, be sure to create a new commit with the changes (using `git add README.md` and `git commit -m` as appropriate). Also, be sure to upload to github frequently by using `git push`
8. If I don't see at least 4-5 commits on this homework, I'm going to be unhappy.
9. Once complete, send me a pull request. This is your official "turn in" of the homework, which I will grade.
10. Double check that you did the right thing by going to https://github.com/MiamiOH-CSE274/01_Git_and_Intro/pulls and making sure that your pull request is there, and looks like you expect. Optimism is the root of all evil.

Exercises
=========

#### 1. Based on the reading in the Git book, is it okay to keep your local copy of your repo on a USB drive and just carry it around? Explain why or why not. What about keeping it on the M: drive?

After reading part of the Git book, keeping a local repo on your USB drive seems like an o.k. idea. After all, if the origin of the repo is located in Github, then the USB drive can do no potential harm to a project if it is destroyed or compromised. The M: drive would be alright to store a local repo as well for the same
reasoning. No matter what happens in the local repo, if the final part of the code is within Github, one can choose not to push the contents of the M: drive local repo to the origin so as to keep the original code clean. 

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

After forgetting to bring my USB drive, I would promptly log into the Github website and go to my repositories screen (if the computer did not already have Git installed, I would download that as well). On the repositories screen, I would select the repo I would want to work from and copy the url to which it was assigned. 
In Git, the url can be pasted after a git clone command to copy the repo from Github to the local machine. After changing directories to the right repo, I would then be able to work on my project.

#### 3. Morin, Exercise 1.1 (p. 25). NOTE: You should not actually implement the solution with code. Instead, explain your solution using English. Pay special attention to explaining which data structure you ought to use, and why.

[Your answer here]

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

(1.4) In order to reverse the order of elements of a stack 's' using only a FIFO queue 'q', I would first load all the elements needed using a while loop with push(x). So, if there are five elements labeled 1, 2, 3, 4, and 5, they would show up 5, 4, 3, etc... Then, to get them to reverse order using a FIFO queue, 
another while loop can be used to first get an element from the original stack queue and enqueue the pop(element) into the new output, thus reversing the order. The purpose of using the while loop is to keep popping elements until there are none left, so that the program accomodates for dynamic sizes. 

[Your answer here]

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - a term to describe a binary large object that conatins only the data of the contents of the file or version of the file (not the name, metadata, etc...).
2. tree - represents one level of directory information. This is where the metadata and names of the files are, as well as identifiers for blobs. 
3. commit - a Git object that holds metadata for changes to a file, such as author, committer, and other information about the file version. The commit points to a tree object that holds the directory state.
4. repo - a data structure that holds a set of commit objects or references to commit objects. The repo can be stored in the Github database or locally.
5. hash - Hash is the hexadecimal code that is generated when an object is created. The hash is a form of cryptography that ensures the security of the file versions.
