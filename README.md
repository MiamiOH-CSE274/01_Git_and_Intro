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

You should keep multiple copies so that it's backed up in case something were to happen to your flash drive or hard drive. One can be kept on the m drive if wanted, since it can be accessed from school and home.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

Clone another local repo from github using git.

#### 3. Morin, Exercise 1.1 (p. 25). NOTE: You should not actually implement the solution with code. Instead, explain your solution using English. Pay special attention to explaining which data structure you ought to use, and why.

1.1.1 For this one you'll want to use Stack because its function pop() automatically returns the last line inputed, so it is very easy to reverse the order by using stack.

1.1.2 You'll want to use Stack again for this one. First reading in the first 50 lines, then using pop() to print them out in reverse order, and repeating the process until all of the lines have been read. 

1.1.3 This program will want to implement the Queue interface. After reading in the first 42 lines, the next line read in will be done so using the add(x) function and then you'll remove the first one read in with the remove() function. If the line is blank, then you can use the remove function and print out whatever it returns. 

1.1.4 You'll want to use a Uset interface for this program as you can tell if the line is unique when you use the add(x) function. If it returns true, then it is unique and you can find(x) and print the result. Otherwise, it is not unique and you don't need to print it.

1.1.5 You can also use a Uset interface for this program. You canuse the add(x) function and if it returns true, then it was the first case of that unique line. Ohterwise it is not the first case, and you can print that line using find(x).

1.1.6 You should use an SSet here, where the set is sorted by length. You can add inputs using add(x) and then since it's already sorted, just print them by using remove(x).

1.1.7 You can do the same thing as in the last one, and then just keep track of how many times a duplicate exists and print it out that many times.

1.1.8 You'll want to implement the Deque interface. You can use the addLast(x) method to add a line of code, then for every other line, removeLast() and print the results. Then when you're done reading all the lines, use removeFirst() and print the results until all of the lines are printed.

1.1.9 You can use the Deque interface and interchangeably use addFirst(x) and addLast(x), which will put it in a random order. Then just use removeFirst() and print results.

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

1.2 Dyck words are similar to Stack push(x) and pop() because Dyck words add 1's and then randomly remove the last 1 that they added, just like how push(x) adds an input, and then pop(0 removes the last inputed line.

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - TODO
2. tree - TODO
3. commit - TODO
4. repo - TODO
5. hash - TODO
