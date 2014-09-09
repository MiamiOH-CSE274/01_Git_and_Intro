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

There's no reason preventing you from keeping your Repo on either a flash drive or your M: drive, although it is inadvisable.  Getting things off your M: drive once they're their requires Netdisk use which is awfully clunky.
Meanwhile, a flash drive makes sense but you'd have to access the GitHub on each different computer you use.  It makes the most sense to just have your repo locally on whatever device you plan to do all your coding.


#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

There's a few things could do, the simplest of which to go get your USB and come back.  However, assuming that's not an option you could always create a new repo on whichever device was currently available to you and clone the latest pushed commit off of GitHub.

#### 3. Morin, Exercise 1.1 (p. 25). NOTE: You should not actually implement the solution with code. Instead, explain your solution using English. Pay special attention to explaining which data structure you ought to use, and why.

The following exercises should be completed by using the given data interfaces as indicated.

1. Using a Stack (or Deque) interface, the simple filo treatment should be satisfactory.  Simply input each line of code into the Stack using add(x), then retrieve them all using remove() once they've all been added properly.
You could also use List for this sort of thing and just perform the role of Stack but with List operations.

2. This could be done rather complicatedly with a List interface, using Stack-like operations for each group of 50 (as described in No. 1) and Queue-like operations for to move from each group of 50.
Alternatively, and I'm not sure if this is possible, but if you could use these interfaces as means of structuring other interfaces; you could simply create a Queue of Stacks.

3. Using a for loop and an if clause, cycle through a List using the following convention...  For lines Xi, starting with Xi equalling the 43rd line in the List, if Xi is blank return the line in the List located at Xi-42.  
If Xi is greater than size() the task is completed.  Otherwise, increase Xi by 1.

4. Add and return each line 'x' to an unsorted set only if find(x) returns nil.  Otherwise, move to the next line.

5. Return each line 'x' to an unsorted set only if find(x) returns y.  Otherwise, add(x).  At some later point, it's probably advisable to remove everything in the USet.

6. Create or find a way to compare two lines, including a tie-breaker such as alphabetic priority.  Add each line to a sorted set and sort them using this convention, but only if find(x) returns nil.
Otherwise, move on to the next line.  After the last line, print everything in the SSet in order.

7. Use the exact same methodology as No. 6 except add all lines to the SSet regardless of find(x).

8. Input each line 'x' into a List, then use a for loop to to remove(x) and output each of the even lines, then simply print and remove(x) the remaining odd lines.

9. Add each line to an unsorted set with no regard for order, then simply remove and print each line however the unsorted set appropriates such a thing.

(Note: I fear I've misinterepreted this entire exercise...! Comments and criticisims would be 100% appreciated)

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

Exercise 1.4:

Assume we have a filled Stack interface 's' and an empty Queue interface 'q'.  To reverse the order of the values currently in Stack s is actually rather simple.

First we must remove each item from "top" to "bottom" in the Stack using pop(). We immediately take this "popped" value and throw it in the Queue using add(x) before "popping" the next value.

Eventually, our Queue should be filled and our Stack should be empty.  From there we do the exact opposite to reverse the original order of the Stack by removing the values from the Queue (using remove()) and adding them to the Stack (in reverse order!) using push(x).

And voila!

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - Any file, the contents of which are negligble to the program git.  For example, this very README.md file bears absolutely no impact on the git operations I perform on it.  It's just a file.  ('blob' is short for "binary large object")
2. tree - Represents and conveys a level of directory info, ie. a folder.  Records each blob in it's directory using a blob identifier, as well as other trees, ergo, subdirectories.
3. commit - The data representation of a change to the repository.
4. repo - The location in cyberspace for storing and sharing data or code.
5. hash - A method of identification assigned to all types of objects used by Git, as well as in many other programs.
