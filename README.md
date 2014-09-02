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

Having a copy of your repo on a USB drive is fine assuming when you are done working on it you commit and push your changes.  Having the ONLY copy of your repo on a USB drive is not ok and defeats the purpose of using git and github.  Keeping it on the M: drive is the same principle.  As long as it's not the only place it's ok.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

Simply clone a new repo onto the local computer from an existing repo online.

#### 3. Morin, Exercise 1.1 (p. 25). NOTE: You should not actually implement the solution with code. Instead, explain your solution using English. Pay special attention to explaining which data structure you ought to use, and why.

1. Queue interface because you want the elements to be in reverse order. Add all elements one at a time until no elements remain, then remove each element.

2. Queue interface because you want the elements to be in reverse order. Add first 50 elements, remove all elements, repeat until no more elements to add.

3. SSet interface because you need to know what string is where. Add 43 elements, continue removing 43rd element and adding elements until 1st element is 0 length, in which case return 43rd element.

4. USet interface because you need to know what is there but not where it is. Add and print first element, see if next element is already in set, if not, add and print element.

5. USet interface because you need to know what is there but not where it is. Add first element, add current element if it doesn't already exist in set, print current element if it does currently exist in set.

6. SSet because you need to not only sort a list but make sure none are repeated. Add all unique elements, comparing to sort from smallest to largest then printing them all from smallest to largest.

7. Priority queue that removes the smallest element first. Add all elements, remove all elements.

8. SSet because you need to know order added.  Add all elements, remove element 0, then 1, then 2 until end is reached, then continue to remove element 0 until empty.

9. USet because you need all elements to be returned in random order.  Add all elements, remove element at random from 0 to list size    


#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)
	
Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

1.4 
remove element from stack s and add to queue, continue until stack s is empty.  Queue will be in reverse order from stack s. 

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - Version of a file. Contains the data but not any references to the data's name or other qualities.
2. tree - Allows for the creation of directories. Contains information on where the blob is and reference other trees to know where itself is. 
3. commit - Contains the changes made to the repo.
4. repo - Holds all of the files in a project as well as all of the previous versions of the files.
5. hash - the unique "name" git gives to each blob. 
