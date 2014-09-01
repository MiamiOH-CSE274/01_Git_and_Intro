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

Yes it is okay to keep the local copy of your repo on a USB drive, however, you should always have a backup of your repos in some other format on another device. The /M: drive would be a less ideal place to keep your repos because there may be networking problems that prevent you from accessing what is saved on the /M: drive.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

You can log in to github.com, where you hopefully have kept a copy of all the repos that you have been working on, and make a copy of the repo that you need to a lab computer.

#### 3. Morin, Exercise 1.1 (p. 25). NOTE: You should not actually implement the solution with code. Instead, explain your solution using English. Pay special attention to explaining which data structure you ought to use, and why.

1. In this situation it would be best to use a LIFO Queue. A LIFO queue stands for Last-In-First-Out queue which means that the last element added will be the one that is next removed. This works nicely with reading in a line of text, applying a reversing operation on the text, and then printing it back out.
2. A Deque would be appropriate for this situation because you will need to store up to 50 elements and then remove them with the removeLast() command.
3. A Deque will also be appropriate for this situation. Elements will be stored and once a blank line is encountered the first element will have to be removed.
4. This situation calls for the use of a USet interface. The USet interface will store unique elements in an unordered fashion. Order is not important to this situation, only  keeping duplicates out is and USet will only add an element if it is found to be unique.
5. USet will work well for this because it has ways to manage duplicate entries. 
6. In order to compare elements a SSet interface should be used. It will allow comparisons between the elements to determine the shortest strings.
7. A SSet interface will be needed so that comparisons between the elements sizes can be made.
8. A Deque should be used because of its flexibility to remove elements.
9. Use a USet interface because it stores elements in a random order.

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)
1.3 In order to determine whether a string of "[],{},()" are matched correctly (as in "{[{}]}") I would send each element of the string to a single stack. Then I would make an exact copy of that stack. From there I would remove the first element of one stack and compare that to the last element removed from the copied stack. By iterating this process to the end of the stacks I could determine if a string is a matched string.

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

[Your answer here]

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - TODO
2. tree - TODO
3. commit - TODO
4. repo - TODO
5. hash - TODO
