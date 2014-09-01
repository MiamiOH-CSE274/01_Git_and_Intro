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

Yes, it is okay to keep the local copy of your repo on your USB drive because this copy should be located wherever you plan to work on your project. Your local copy doesn’t need to be in any specific location, but rather the location from where you are working because you can send your progress to Github from any computer. With that being said: Yes, you can also keep your local copy on your M: drive if that is where you feel comfortable keeping it. 

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

As long as you submitted the last revision on your USB to GitHub you can easily clone the revision from Github on to the computer in the lab and continue to work on it with your friends. None of your progress should be deterred. 

#### 3. Morin, Exercise 1.1 (p. 25). NOTE: You should not actually implement the solution with code. Instead, explain your solution using English. Pay special attention to explaining which data structure you ought to use, and why.

1.3.1 I would use the LIFO Queue to solve this problem. I would push and pop the data through the use of a loop. Since we want to make the last line of the text file printed out first, the LIFO method would solve the problem the best.   

1.3.2 For this problem I would do something similar to the solution in 1.3.1, however I would have a counter in the loop to make sure only 50 lines of text are being reversed at a time. Once those lines are reversed more lines can be read into the loop. This solution would also reverse any remaining lines at the end of the text file.

1.3.3 I would approach this problem by using the FIFO Queue method. I would use a loop to process the first 42 lines of text and then I would read in the next line to see if it was blank. If the 43 line was blank, I would print out the first line in the queue and if it wasn’t blank, I would remove the first line in the queue. I would follow this process until the end of the text file was reached. 

1.3.4 I would use a USet for this problem. I would add one line at a time to the USet and since USets don’t allow duplicates there would only be one copy of each individual text line. Once all lines were added, I would print the USet. 

1.3.5 A USet would be used for this problem as well. I would start by adding the first line to the USet. Next I would add the next line to the USet and use the find(x) command to see if the second line is already present in the USet. If the line is present, I would print out the line. If the line is not present, I would add the line to the USet for comparison of later lines. 

1.3.6 I would use a SSet for sorting the text lines based on length. I would read in the first line of text making that the starting standard for comparison. Then using the compare(x,y) function I would sort the rest of the text lines based on their length. 

1.3.7 I think a Priority Queue would work best for this situation. I would use the same technique as the problem above, but duplicates would be allowed unlike in the SSet. 

1.3.8 I would use two individual loops to complete this task. The first loop would start at 0 and increment by 2 which would print the even lines. Then the second loop would start at 1 and increment by 2 which would print the odd lines. I would store all of the lines in a list. 

1.3.9 For this problem I would use just another simple list. Then I would use Math.Random() to determine a random number and print the line that corresponds to the number generated. This would ensure randomness among the lines printed to the list. 

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

1.2 Dyck words and the push(x)/pop() operations are similar because when you push(x) something to a Stack you are adding (+1) an element and when you pop() a Stack you are removing an element (-1). Also they are similar because you cannot pop() a Stack with no elements just as you cannot have a Dyck word if there are more -1’s then there are +1’s.

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - How a file is represented. Contraction of binary large object. Used to refer to a file that can contain any data whose internal structure is ignored by the program. 
2. tree - Represents one level of directory information. Records blob identifiers, path names, a small amount of metadata for all files in a directory. 
3. commit - Hold the metadata for each change introduced into the repo. Includes the author, committer, commit date, and log message. 
4. repo - Short for repository. A database containing all the information/files needed to retain and manage the changes and history of a given project.  
5. hash - 160-bit values represented as a 40-digit hexadecimal number. SHA1 or hash code. Each hash code is unique based on the contents of the file. 
