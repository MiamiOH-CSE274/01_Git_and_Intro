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

It is okay to keep a local copy of your repo on a USB, or the M: drive as long as after each session that results in changes to the repo, the changes are pushed to the origin.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

You should clone your latest repo from the origin on github to the computer in the lab then work on it there. After work is done the changes should be pushed back to the origin on github so your latest work is available for access from any computer.

#### 3. Morin, Exercise 1.1 (p. 25). NOTE: You should not actually implement the solution with code. Instead, explain your solution using English. Pay special attention to explaining which data structure you ought to use, and why.

1. To accomplish this, a stack should be used to read the file then the LIFO(last in first out) interface should be used to write in the file backwards.
2. To do this, wrap the code in a while loop that runs as long as there are more than 50 lines of code. Once there are less the remaining lines are printed out backwards using LIFO, and while there are 50 or more lines, LIFO is used once an array of 50 lines is filled using addFirst and removeFirst.
3. A queue wrapped in an if statement that adds lines until the size is 42. Then an if statement can be used to check if a lines size() is == 0 then if true, get is used to return a line 42 spaces back by doing size()-42 as one of the get(i,x) parameters.
4. USet and the USet add(x) should be used since add(x) for this interface only adds if x is not present. As soon as a line (or x) is a duplicate, it won't be added.
5. A FIFO(first in first out) interface should be used to get the first line and remove the first line after.
6. SSet can be used with find(x) which returns the smallest element in the set, then the compare(x,y) method can be used if two equal length lines are found.
7. Everything should be added to a queue, then removed by using priority queue to remove the smallest element and the removed element can then be added as it will be the smallest.
8. A stack could be used that starts at 0 and skips a line until the end is reached. Then the remaining lines would all be even, and could all be added with another stack. 
9. Deque can be used to add the lines to the front or back by getting a random number between 1 and 2. If 1, then addFirst(x) would be used, if 2, addLast(x) would be used.

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

1.2 - A Dyck word can be expanded infinitely by adding 1 the same way as a stack can be expanded infinitely by adding more elements with push(x). The same applies to subtracting 1 or using pop() to remove elements. Once A Dyck word or stack is at 0 you can't subtract 1 and you can't use pop().

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - Otherwise known as a "binary large object". Contains file data, but not the files name or other metadata.
2. tree - A tree is a level in a directory. Trees record path names, identifiers, and some other metadata.
2. tree - A tree is a level in a directory. Records hierarchies 
3. commit - Commits are metadata for each particular version of a file.
4. repo - A repo is a database that holds all of the data needed to build a particular project.
5. hash - A hash is a 40 character value that identifies all of the information for a particular object. 
