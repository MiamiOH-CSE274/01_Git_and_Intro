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

It seems like it would be ok to keep a local copy of it on a USB drive as long as you have it on a desktop or laptop that you have easy access too. If you aren't using the repo to push your changes, it is pointless to have though. The M: drive is the same kind of concept. As long as you are actively pushing the changes you're making, you're good.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

You should work on something that you know needs to be changed. Maybe a different class or a different function that needs to be completed. After you push these changes, they will be available to you when you get back to your room or wherever your actual copy of the repo is.

#### 3. Morin, Exercise 1.1 (p. 25). NOTE: You should not actually implement the solution with code. Instead, explain your solution using English. Pay special attention to explaining which data structure you ought to use, and why.

1. You could do this by pushing everything that in entered onto a stack, and then popping them off one by one using a loop, displaying them as they pop off.
2. You could create a variable that would act as a counter for the loop. As something is entered, it can be pushed onto the stack, and the counter is then increased by one. As the stack gets to 50 items, the counter % 50 will equal 0, so there could be an if statement that pops every item off of the stack and displays them.
3. You could do this with a Queue. You could add the line to the end of the queue. If the line being added is a length of 0, you could subtract 42 and print out the line.
4. You could create a sorted set. This would allow you to store every new item that is entered. The new input could be referenced against that sorted set, and if it is contained within the set, it will not be printed. If it is not included, it can be printed, and then added to the sorted set so that it cannot be printed again.
5. You could create a sorted set. Using the first input, you could compare it to the next input. If it is the same as the next one, you can add it to the set, and output it. From there, the inputs can be referenced with the sorted set and if there is no reference of the input, it gets added to the set. If there exists one of the same input in the set, it gets output.
6. You could start by writing the first line to a list. From there, all the new inputs' lengths will be compared to things in the list. If the line is the same length as a different item, a check must be made to see if they are the same thing. If they are, that item can be ignored, and the next input is evaluated.
7. Do the same thing as the last problem, but instead of ignoring the ones that are the same length, output them anyway.
8. A FIFO Que with a loop that allows you to keep track of line numbers would be the ideal way to go about this. After that loop has gone through and printed all the even numbers, it can be started over with all of the odd numbers.
9. A Uset could be a good way to do this based on the fact that the set is not ordered. A function that shuffles the current item into a random slot would make it so that the list is in a random order after every slot has been shuffled at least once.


#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

1.4 In a dyck word, it is possible to add +1 infinitely many times. In a Stack, push(x) can be used infinitely many times. The second a dyck word = 0, adding a -1 to it will make it negative and "break" it. In the same way, if a Stack has no elements left, you cannot use pop() since there is nothing included in the stack. 

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - The contents that are in a file.
2. tree - The equivalent of a directory; a combination of all the blobs into one place.
3. commit - A "version" of the repo that changes as changes are made to the repo.
4. repo - The place that all the version of the project is stored.
5. hash - A representation of an object in a repo.
