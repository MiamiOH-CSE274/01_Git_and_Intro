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

It is okay to keep a local copy of your repo on a USB drive and just carry it around but if it doesn’t work, then you can't find the last point that your program was working. If you store it in your M: drive, then you can only access your repo if you have access to your M: drive.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

Use what you have saved on github to continue to work on what you left off with. Github stores your repos if you allow it to.

#### 3. Morin, Exercise 1.1 (p. 25). NOTE: You should not actually implement the solution with code. Instead, explain your solution using English. Pay special attention to explaining which data structure you ought to use, and why.

1. You would use the Last In First Out Queue in a loop that repeats for every line of code that you have until you run of lines of code. This method takes the most recently added element and then removes it first. You would just want to make sure that you make a copy of each line of code and print it before you remove it entirely.
2. For this example, you would use LIFO as mentioned in part one and have the loop start at the fiftieth line if it exists and increment fifty times. Then add 50 to that and run the loop again starting at line 100 and increment it 50 times. Continue until you run out of lines of code to work with.
3. Using a for loop, read each line individually and determine if the length of the line is 0 using an if statement. If not, then store that line of code in another file and continue to the next line. Using another if statement, test if the for loop is on it's 43rd increment after it has done everything else in the for loop. If so, then use the First In First Out queue in another for loop to remove the first line stored. Using another if statement in this for loop, determine if the length of the line is 0. If so, then print the first line of code in the file you have saved. This should increment until you run out of code to test.
4. Using a for loop to iterate through each line of code, also store each line of code in a different file. In each iteration of the for loop, test to see if that particular line of code matches any from the stored document using another for loop. If it does, then remove that line of code and do not write it to the output. If it doesn't match any of the previous lines of code, then write it to the output.
5. Using a for loop, iterate through each line of code and test whether it is identical to another line of code before it. If it is identical to another line of code, then write it to the output. If not, then skip to the next iteration.
6. Use a for loop to iterate through each line of code, store the length of the line at the end of the code, and store the line in another file. After all of the lines of code have been read, then go through them again with a new for loop and sort by the length of the line that is stored and print them smalles to largest. Using a loop, you can iterate through and find the smallest line, write it to the output, then remove it and resume with the loop to find the next smallest etc. Also test in that same for loop for duplicates of lines of code. If there is a duplicate, remove it from the list and continue.
7. Do the same as part 7 above but do not remove duplicates from the code.
8. Using a for loop, iterate through the lines of code one line at a time. Starting with the first line, write every other line to the output and then remove it from the code. Then iterate through the rest of the code, which should only be made up of the code that was originally on odd numbered lines, and write each line to the output in the order that it appears.
9. Using a random number generator in a for loop, take the number that was generated and use it to determine how many iterations of reading code to go through before it stops. The last line of code should then be printed and then removed from the document. Then repeat until there are no more lines to read.

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

	1.4

Using a for loop, you can take the element that was entered first into the stack and make a copy of it. Then push that copy to the other end of of the stack and pop the original copy. Continue doing this until all but the last element have been moved to the other side of the stack.




#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - holds the content of a file or files but doesn't keep track of the name of the file
2. tree - a folder that keeps track of the names of the files
3. commit - a version of a project
4. repo - (repository) - holds what you need to build a project
5. hash - also known as an object ID, it identifies each file with a 40 digit hexadecimal number
