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

It is possible to keep a copy of your repo on a USB drive. However, if that is your only copy it is probably not advisable. If the USB drive is lost, the repo is lost. Keepint the local copy of the repo on the M: drive is a better choice, because a user's M: drive can be accessed from multiple computers. So if one crashes, another machine can be used and the repo is not lost.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

Assuming you have been using GitHub and using git push to keep the remote repo up to date, you can simply clone the repo onto a computer in the lab. 

#### 3. Morin, Exercise 1.1 (p. 25). NOTE: You should not actually implement the solution with code. Instead, explain your solution using English. Pay special attention to explaining which data structure you ought to use, and why.

1. For this problem you would use a Stack. You would push all the lines onto the Stack and them use the pop() operation to remove the lines in reverse order.
2. A Stack interface would also be helpful here. The lines would be pushed onto the Stack 50 lines at a time, then you would again use the pop() operation to remove the lines in reverse order.
3. For this problem a Queue would be useful. The Queue should hold up to 43 lines. Lines are added to the end of the queue with add(x); if a line is blank, the remove() operation would be used to then print out the line 42 lines prior to the blank one (the first one).
4. A USet should be used here. USets do not support duplicate elements, so it would be easier with this data structure to only write the lines to the output if they are not duplicates.
5. A USet would be helpful. Before adding a line to the set, first use find(x) to see if there is a duplicate. If there is not one, add it to the set. If there is one, print the line in the output.
6. An SSet should be used here. The lines need to be sorted by length, but duplicates should only be printed once. The SSet does not have duplicate elements, but does have a compare(x,y) method that would be useful here when to lines have the same length and need to be ordered according to the usual "sorted order."
7. A Queue with the priority queueing discipline would be most helpful here. Since duplicate elements do need to be printed, once all elements are in the Queue the remove() method will remove the shortest lines first, thus sorting them.
8. Two Queues with a FIFO queueing discipline should help in this problem. Even lines should be added to an "even" queue, while odd lines can be added to a separate "odd" queue. Then the even lines can be printed first using the dequeue() operation for the "even" queue, followed by dequeueing the "odd" queue.
9. A Dequeue interface is a good choice here. It can be randomly computed whether each line should be added to the front or the back of the queue, thus randomizing the lines before outputting them.

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

Ex. 1.4 - If you have a Stack s of elements that need to be reversed, you should use a loop to pop() all the elements out of s and add them using enqueue(x) to the FIFO Queue. Then you can use another loop to dequeue() the elements out of the FIFO Queue. Since the last elements of s were added to the FIFO Queue first, they will be the first elements to be outputted, thus reversing the original Stack.

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - A "blob," or "binary large object," holds a file's data but does not contain any information about the file, such as its name. Git stores information by using the hash of the data within the file and not based on the file names. Thus Git uses blobs as the base of its object store.
2. tree - A tree object holds blob identifiers, path names, and metadata for all files in one directory. It can also reference other tree objects to build a hierarchy of files. In Git, tree objects reference blob objects and sometimes other tree objects (such as when there is a subdirectory).
3. commit - The commit object holds data for each change to the repository. This information could include the author, commit date, and commit message. Every commit points to a tree object that represents the state of the repo at the time of the commit. Only the first commit has no parent; the rest point back to an earlier parent commit.
4. repo - A repo, or repository, holds all the information required to manage and retain the revision history of a single project. In Git, repos contain complete copies of projects.  Each repo contains two data structures - the object store, which contains the information required to rebuild any version of the project, and the index, which is a dynamic, temporary binary file that captures the project's overall structure at a point in time.
5. hash - SHA1 hash values are 160-bit values represented by 40-digit hexadecimal numbers. The same SHA1 hash value will be computed for two objects with identical content, regardless of where they are stored. In Git's object store each object has a SHA1 hash value that is unique to its content. These hash values are used as a name for the object (whether it be a blob, tree, or commit) in the object store.