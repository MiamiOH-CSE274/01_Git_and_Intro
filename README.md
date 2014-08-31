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

editing a repo from a flashdrive is fine because moving the repo from computer to computer on the same drive is comparable to just cloning it to that system.
The M: drive works the same way as a flashdrive in this sense because it is the same files being accessed on all computers.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

If the repo was pushed at the end of the last work session cloning it to the new machine would work fine to solve this problem.

#### 3. Morin, Exercise 1.1 (p. 25). NOTE: You should not actually implement the solution with code. Instead, explain your solution using English. Pay special attention to explaining which data structure you ought to use, and why.

1.Write to a stack and then pop them off of the stack.
2.loop to write to a stack 50 times then pop 50 times, repeat until finished.
3.make a queue with no more than 43 lines in it and if the most recent addition is blank output the oldest line, if it isnt, just remove the oldest line. 
4.Use an SSet and write the first line, look at the second line, if it equals any previous line, skip it, if it doesnt output it and then add it to the sset.
5.Use an SSet and write the first line, look at the second line, if it equals a previous line, output it, else, write it to the SSet.
6.write the first line to a list, read the next line and compare lengths until its proper position is found, compare the current line to all lines of the same length, if it is the same as any of them, skip it, else, write it to the list.
7.write the first line to a list, read the next line and compare lengths until its proper position is found and insert it to the list at that position.
8.create 2 queues put all even lines into one and all odd lines into the other, the output the entirety of the even one first and then do the same with the odd queue.
9.Write all lines to a USet then output a random line using a random number generator with a max of the length-1 of the uset.

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

1.2 All stacks are examples of dyck words because, much like a deck of cards, if there are no cards in the stack, a card cannot be taken away.

[Your answer here]

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - TODO
2. tree - TODO
3. commit - TODO
4. repo - TODO
5. hash - TODO
