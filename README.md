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

I believe that it's okay to keep a clone of repo on a USB drive. However, this can be dangerous if the repo contains sensitive information as it's extremely easy to lose USB drives. Because of this, the M: drive would be more safe, would could still be problematic if you left yourself logged in. 

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

In this case, as long as I had my repo on github I could clone it to my computer and work on it there. If I didn't have at least some version of it on github, and only had it on my USB, then I messed up. 

#### 3. Morin, Exercise 1.1 (p. 25). NOTE: You should not actually implement the solution with code. Instead, explain your solution using English. Pay special attention to explaining which data structure you ought to use, and why.

1.1 I would use a LIFO queue (Stack). I would push in the data, and then pop it out through the use of a loop. Since the last bit of data pushed in is what we want to print first, the LIFO approach would be the best choice.  

1.2 I would again use a LIFO queue stack type process. However, I would have a counter that once it reached 50, would print out the data using the LIFO approach (so the last bit of data would be printed first) before continuing to push more data into the queue. The remaining lines would also be taken care of with this method. 

1.3 I would use a FIFO queue for this problem. I would first read in 42 lines of data through a loop. I would then read in the next line and check if it was blank. If it was blank I could replace it with the first line in the queue. If it wasn't blank I could remove the first line from the queue and add the line we just checked to the end. A FIFO queue would be useful because we're progressing through the data whilst maintaining a way to replace blank lines. 

1.4 I would use a USet for this problem. I would add the lines to the USet one line at a time. Because USets do not allow duplicates, only the first occurrence of each line would be recorded. Optionally, I could have a boolean that was initialized as false, and when I used the add(x) function I could change the boolean to represent if the line failed to add because of duplicates. After all of the lines were read in I would print everything in the USet.

1.5 For this I would also use a USet. I would start by inputing the first line into the USet. I would then input the second line and use the find(x) command on the USet to see if the line already exists in the USet. If it did exist already, the line would be printed. If it did not exist, it would be added. This process could be done with an if loop. 

1.6 I would use a SSet here because they represent a sorted set of elements. Duplicates would not be allowed since it is a set, and we could use the compare(x, y) function to create a sorted list. 

1.7 I would use a priority queue here. The smallest elements would be removed first and duplicates would be allowed. 

1.8 I would use a loop of some sort here with a list. The list would hold the elements and I could loop through it and print out the even numbers followed by the odd numbers. 

1.9 I would again use a list, and some random number generator to randomly pick a line to output.

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

A dyck +1 is similar to the stack push(x) option. Both add one 'thing' to their object, being either a dyck word or a queue. The connection between a -1 and a the pop() function is very similar. The -1 removes one value from dyck word and pop removes an element from the queue. 

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - A binary large object is a large amount of data that doesn't contain or store any structure. 
2. tree - A treee is one level of information inside of a blob. 
3. commit - A commit holds information about what kinds of changes were made in a repository. 
4. repo - A repository is a place where all the build information is held that is necessary to work on a project.
5. hash - A hash in a unique representation of a file's id.
