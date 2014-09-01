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
I suppose it is acceptable to carry around the local copy as long as you store the copy on Git, as it is held safe on the Internet even if your copy of the local files is on your flash drive. I would go as far to say as lonf as you consistently store your files on Git, your local files can stay wherever you like. As long as you don't get hacked or whatever your Git files should be safe.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?
As long as you save your files often (which is always a good thing), the most recently updated version of your repository should be on Github at all times. If you log onto Github, you can clone your repo onto any device your have with you and progress from the same point.

#### 3. Morin, Exercise 1.1 (p. 25). NOTE: You should not actually implement the solution with code. Instead, explain your solution using English. Pay special attention to explaining which data structure you ought to use, and why.
1. This would best be done in a stack structure, which orders elements in a LIFO format, meaning a last-in-first-out structure. If the last element to be added was to be the first to be retrieved, a LIFO structure such as Stack would be utilized. An input mechanism would append a string whenever new input was read, then the Stack would output the information.
2. A loop would iterate 50 times, inputting a string in a Stack each iteration,  then outputting the string in a LIFO manner after each full run of the 50-iteration loop (for-loop would be easiest). Inside the for-loop would be a check to make sure there are more strings to input. If there are not, end the loop and proceed to output the strings in LIFO style.
3. A for-loop iterating 42 times inputs each line or string regardless of content. After that, each line is checked to see if the length is 0. If not, ignore it and step to the next line. An integer variable will be tracking the line number from the first line index. If the length is 0, the program will output the string at the index 42 lines previous than the current integer value of the index.
4. This program will add each input string to a queue and ouput each string, but only after checking through the queue to assure this exact line has not been input before. If it has, ignore it. No repeated line will be read more than once as any replicate will be ignored.
5. A queue will be implemented in a similar fashion to the previous question (1.1, #4), but each line will be input as long as it is not contained in the queue already, and if it is, then output the repeated string and do not add it to the queue again. No memory will be required after outputting repeated string, so many repeats doesn't require extra memory.
6. All lines will be input into a set sorted by length, then by normal sorting style (alphabetical, etc.). Each line will be checked to make sure no duplicate lines are present, and if a line is already present, dequeue it from the list. Once all lines are sorted by length then alphabetically, output them in that order.
7. All lines will be input into a set sorted by length, then by normal sorting style (alphabetical, etc.). Duplicate lines will be placed chronologically (by order of input, FIFO) Once all lines are sorted by length then alphabetically, output them in that order.
8. This program will read and input all lines of text. Then a for-loop will be implemented starting with zero and increasing by two each time until the iterating variable is past the number of lines. Then, another 
9. A for-loop will be implemented to input all lines of text into an unsorted set of text lines. Next, a loop will shuffle the lines by randomly selecting a number from 0 to one less than the current number of lines of text, transferring the line to a second queue each time a number is selected. Also, when a line is transferred, the length decreases by one, so each time a new random number is drawn, it is between 0 and the current length of the original list. That way, each element in the set has an equal chance of transferring to the randomized queue each time. Once the last element has been transferred, output all lines in the newly randomized queue of lines.

#### 4. Your choice: Morin, Exercise 1.2
Dyck words can never be negative. Once they are zero, another -1 cannot be set. In the same fashion, once a Stack has zero elements, the pop() operation cannot be used. The push(x) operation can be used anytime, just as how a Dyck word can always add a +1, but taking away a value (-1 and pop()) are not allowed if there is no value left (Stack has no elements or Dyck word has a value of 0).

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - A blob (contraction of binary large object) holds a file but contains no information or metadata pertaining to the file itself. Just a placeholder for a file.
2. tree - A tree is a placeholder for a category of files and/or information. A tree can point to many connected nodes of info, files, or other (sub)trees.
3. commit - Commit objects hold metadata including the author, committer, commit date, and log message at the instant the commit is made. A commit points to a tree object of information pertaining to a sort of snapshot of the git files being committed, saving all information in the commit at that exact moment.
4. repo - A git repository is a database containing information about all files in the repository such as trees and tree files, as well as metadata contained in commits regarding the information in the repository at any moment the repo was committed.
5. hash - A hash-object in Git stores [whatever data the user wishes to send] in the .git directory then returns the key associated with said data.
