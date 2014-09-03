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

Yes, it is okay to keep your local repo on a flash drive so long as you are keeping your repo updated and pushing all your changes back it does not matter where you store it, so the M: drive is just as viable.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

So long as you are properly and constantly maintaining your github version of your repo with commits and pushing to your github repo you can simply clone your repo to your local machine and continue to work on it.

#### 3. Morin, Exercise 1.1 (p. 25). NOTE: You should not actually implement the solution with code. Instead, explain your solution using English. Pay special attention to explaining which data structure you ought to use, and why.

1. This can easily be accomplished pushing every line that you read onto the stack, and then after you have read every line, popping each line off the stack and output the line.

2. You can once again push each line onto the stack, and using a loop with a counter in it. Once the counter % 50 is equal to 0 (once the counter reaches 50) pop each item off the stack and output it, repeating until complete.

3. You can read each line off and store it in a queue. Once you reach 42 lines remove the 1st item from the queue, and once you reach a blank line output the first item from the queue.

4. Store each item in a sorted set so that duplicate items would be removed, and as it is entered and compared against the sorted set to make sure it is unique, output it.

5. Store each item in a sorted set similar to the last one, however if the item is a duplicate, output it, and if it is unique, add it to the sorted set.

6. Store each item in a sorted set and output them in sorted order, comparing each item to the previous entry to check for duplicates, in which case, do not output.

7. Store each item in a sorted set and simply iterate through every item in the set and output it.

8. Store each line into an unsorted set, then after storing each of the lines, iterate through the even numbered lines with a loop, outputting them, then iterate through the odd numbered lines and output them.

9. Store each line into an unsorted set, and after all lines are stored, use a random number generator to print off random lines. 
#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

1.4: An easy way to reverse the order of a stack is by using a queue. Simply push all the data onto the stack, and after all the data has been pushed, pop it off into the queue, and then dequeue the data by pushing it back onto the stack, thereby reversing it.

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - A "binary large object", or some variable or file that contains data but the actual structure of the data is ignored by the program.
2. tree - An object that contains information about a level of a directory, including all the files' metadata
3. commit - Contains data about every change to a repo, who changed it, and what they changed.
4. repo - The main directory where a project is stored, and contains every file in the project.
5. hash - How objects in git are named.