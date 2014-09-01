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

A USB drive is an excellent location to store a copy of a repo, but it is not sufficient to only store the repo in one location.  A USB drive could easily be lost or damaged, so it is important to have the repo backed up in multiple locations such as the M: drive.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

If I forgot to bring my USB storing the repo, I would simply use a back up copy of the repo stored on the M: drive or clone a new copy directly from the CSE 274 GitHub page.  

#### 3. Morin, Exercise 1.1 (p. 25). NOTE: You should not actually implement the solution with code. Instead, explain your solution using English. Pay special attention to explaining which data structure you ought to use, and why.

1) Create a new stack and push every line of input onto the stack.  Next use a loop to pop each line of input off of the stack and print it out.   
 
2) Create a while loop that pushes the current line of input onto a stack and contains a counter.  At each time the counter%50 is 0, pop every item off of the stack and print it out.  

3) Create a queue that stores each line of data as it is encountered and put it in a while loop with a counter.  Enqueue each line of data until the counter reaches 43.  Next call the dequeue method each time a succesive line is enqueued and if the line is empty, print out the dequeued element.  

4) Create a sorted set that adds each element that is output.  If the output matches something contained within the set, do not print the output.

5) Create a queue to handle each individual line of input.  Next create an ordered set to store each line that is dequeued.  If the dequeued line matches an element of the set, it is printed.

6) Create a new sorted set and add each line to the set.  Next output each line unless the current element is equivalent to the next element in the set, in which case skip the current element.   

7) Create a new sorted set and add each line.  Next use a loop to iterate through each element contained within the set starting small and finishing with the largest.

8) Create a new unsorted list and add each line to the list.  Next use a while loop with a counter to that increments for every line in the list.  If the value of the counter%2 is 0 print the individual line.  Next create a similar loop that prints the line if the counter%2 is 1.  

9) Create a new unsorted list and add each line.  Next use the find method with a random number as a seed to output each line and remove the element until the list is empty.

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

[Your answer here]

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - TODO
2. tree - TODO
3. commit - TODO
4. repo - TODO
5. hash - TODO
