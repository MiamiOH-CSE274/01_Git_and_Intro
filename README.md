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

It wouldn't make sense to carry it around on a USB drive, because you can always clone your repo to your desktop. If you clone it to the m drive then you have an almost permanent copy of your repo. You can access it from any computer, and you wouldn't have to clone it multiple times. 

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

You can go to github and clone your repo to the local desktop. Or (and this would save a lot of future hassle) you could clone it to your m drive.

#### 3. Morin, Exercise 1.1 (p. 25). NOTE: You should not actually implement the solution with code. Instead, explain your solution using English. Pay special attention to explaining which data structure you ought to use, and why.

1. I would add each line to a stack, and once all the lines have been added, print them before removing them. A stack makes it so you have to remove 
the last piece of data added before you can access any data added before it. 

2. I would start with a for loop, making 50 the highest condition, and going through and stacking each line. This is like the first part of the question, but with a 
cap on how many lines can be stored. Again, a stack makes it so you have to remove the last added data before removing anything else. Once the for loop stops I would begin 
printing the lines right before removing them from the stack. When that was done, move on to the next 50 lines. 

3. This problem calls for a FIFO queue. Before adding to the queue I would have one variable measuring distance between lines (so it would count up to 43 at most) and one variable to store the "to-be-printed"
line. If there is not blank line, the "to-be-printed" line is added to the queue, and the line after it becomes the variable. 

4. There would need to be an if statement that would run through the queue checking for duplicates. If it was a duplicate it would be removed and the next input line would
take its place. 

5. Using an if statement, run through the queue to see if there are duplicates. Unlike the last question, if there is a duplicate, you can add to queue, and move to the
next input. 

6. The SSet interface will allow us to compare lines to one another. Giving one line a variable and the next line another variable we can compare them with: compare(x,y).
 Using an if statement to find if they are duplicates, keep both if they're not, delete one if they are. 

7. Again, using the SSet interface we can compare lines to see if they are duplicates. Except instead of deleting all the duplicates, print them.
So, if there are three duplicates, there will be four of the same line printed. 

8. With a for loop, every time i=an even number, the input line will be printed. When i=an odd number those lines would be queued, so when the for loop is finished we could
go ahead and print all the queued lines (which would be all the odd numbered lines).

9. Set is supposed to be an unordered set (unlike SSet). So if we add each line to a USet, then print them out they should be in a random order. Or we could
find(x) (x being a random number), print what we found, then remove the line from the set. 

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

[Your answer here]

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - Blobs are any arbitrary binary data. 
2. tree - A huge directory of paths (filled with information). It contains blobs, hashes, and commits.
3. commit - The action that finalizes the changes you made in a document. This puts the changes in the repo file(s).
4. repo - Contains the source code. You can take that source code and modify it, pushing it back to the repo (if you want). 
5. hash - Writes a specified-type-object into a tree without modifying the files in the work tree. If the type isn't stated, the hash becomes a blob.
