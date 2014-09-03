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

It should be ok to keep a local copy of the repo on a USB drive. This is because Git uses an index system that that does not strictly depend on file names. The same should be true for keeping it on the M: drive.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

If you had pushed the current version of your repo to github before you left for lab, you could log on to github and clone the repo to the lab computer. If you had your repo on the M: drive, you could download it from there.

#### 3. Morin, Exercise 1.1 (p. 25). NOTE: You should not actually implement the solution with code. Instead, explain your solution using English. Pay special attention to explaining which data structure you ought to use, and why.

1. Add each line to the beginning of the list using push_front(line). Then, write the list to the output file.

2. Declare a list of strings. While there is a next line, read the line, add line to top of list using push_front(line). If the size of the list == 50 or there is not a next line, call function to write lines in list, then clear the list.

3.  Declare a list of strings. While there is a next line, read the line, add line to list. If the size of the list == 43, check to see if line 42 is empty. If true, set line 42 equal to line 0, call function to write lines in list, then clear the list. Repeat until no lines are left.

4. Declare a USet. While there is a next line, add it to the USet (the USet will not add duplicates). When finished, call the function to write the USet.

5. Declare a USet and a list. While there is a next line, add it to the USet. If the next line is already in the USet, add it to the list. When complete, call function to write the list.

6. Declare a SSet, sorted by string length.While there is a next line, add it to the SSet (this will remove duplicates and sort by length). Starting with the set of lines with the shortest length, create a new SSet and sort by the usual sorted order and call function to write the set. Repeat until the set of lines with the max length is complete.

7. Declare a list. While there is a next line, add the line to the list. Sort the list by line length. Create new list for each group of lines of equal length, starting with the group minimum line length. Then, sort the list with the usual sorted order and write the list. Repeat until list containing max length lines is complete.

8. Declare two lists: evenList and oddList. Declare a counter = 0. While there is a next line, calculate counter % 2. If counter % 2 == 0, add line to evenList, else add line to oddList. Then write evenList followed by oddList.

9. Declare a list of size equal to the number of lines - 1. Declare a USet of size = number of lines - 1. Then generate random integers between (0, USet size) and add them to the USet. When the Uset is filled, read each line from the text file, and add it to the corresponding index in the USet of unique random integers. Then write the list. 

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

Exercise 1.2 

Starting from beginning of word
while (word has next +1 or -1) {
	get the next +1 or -1
		add this to the stack
}
remove the first element from the stack (pop())
add the remaining elements in the stack.
	If the sum of the stack is < 0, then the word is NOT a Dyck word.
	Else, the word IS a Dyck word.

Summary: Take the word and put it into a stack. Since the last +1 or -1 is at the top of the stack remove it; the remainder is the prefix. Add the remaining values, if the sum is negative, the word is not a Dyck word. Else, the word is a Dyck word. 
	
#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - Any file in the git repo is a blob.
2. tree - Git's version of a directory. Can contain blobs or other trees.
3. commit - Information relating to what changes were made on the repo along with who made the changes.
4. repo - A place where all the files for a git project are stored.
5. hash - Used for naming git objects. 
