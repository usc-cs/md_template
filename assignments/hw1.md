---
layout: default
title: Homework 1
nav: assignments
---

##Homework 1

+ Due: Sept. 5, 2014, 11:59am (PST)
+ Directory name for this homework (case sensitive): `hw1`

###Problem 1 (Course Policies, 15%)
Carefully study the information on the [course web site]({{ site.url }}/index.html), then answer the following questions about course policies:

####Part (a): 
Which of the following are acceptable behaviors in solving homeworks/projects?

1. Looking up information relevant to the course online.
1. Looking up or asking for sample solutions online.
1. Talking to my classmates about the problems.
1. Copying code from my classmates, and then editing it significantly.
1. Asking the course staff for help.
1. Sharing my code with a classmate.

####Part (b): 
Which of the following are recommended ways of writing code?

1. gedit
1. emacs
1. Eclipse
1. vim
1. Microsoft Visual Studio
1. notepad

####Part(c): 
What is the late submission policy?

1. One hour late submission still yields full credit for each assignment.
1. Each assignment can be submitted up to three days late for 50% credit.
1. Each student can submit up to 3 homeworks a day late for full credit.
1. Students need to get an approval before submitting an assignment late.

####Part (d): 
Is there a grace period to submit assignments?

1. No
1. There is an hour grace period per assignment for 50% credit.
1. Yes, but only if there is a technical difficulty with submission.
1. There is a day grace period upon approval.

####Part (e): 
Which C++ compiler do you have to use?

1. I have to use g++.
1. I can use any compiler I want, so long as it works on my machine.
1. I can use any compiler I want, but the submission has to work with g++ on the course VM in the end.


###Problem 2 (Git, 15%)
Carefully review and implement the steps discussed in [Lab1](#). Then, answer the following questions:

####Part (a): 
Which of the following git user interfaces are accepted and supported in this course?

1. Git Bash (Windows)
1. GitHub Desktop Client
1. Terminal (Mac or Linux)
1. Eclipse eGit
1. Tower Git Client

####Part (b): 
Provide the appropriate git command to perform the following operations:

1. Stage an untracked file to be committed. The file is called 'hw1q2b.cpp'.
1. Display the details of the last three commits in the repository.

####Part (c) 
Let's say you staged three files to be committed. Then, you ran the following command: 

`git commit`

What will git do?


###Problem 3 (Review Material)
Carefully review recursion and dynamic memory management from your CSCI 103 notes and textbook. You may also find Chapters 2 and 5 from the textbook, and the C++ Interlude 2, helpful.

###Problem 4 (Strings and Streams, Dynamic Memory, 30%)
Write a program that reads in a text file and outputs, for each line, the number of words on that line. However, it will have to do this in reverse order of the lines. The program must get the name of the text file as a command line argument; do not hard-code the filename, and do not ask the user with `cin` or `scanf`. 

For the text file, the first line contains the number of lines in the file; let's call it n. This will be followed by n lines. Each line has at most 80 characters, which will be only letters (upper or lower case) and white spaces (space, tab, newline). A line may contain many words. Two words are separated by any white space character. 

We will not give you an upper bound on n, and you should not hard-code one. Nor can you use types such as `vector` or `list` from the STL. In other words, you must use your own dynamically allocated memory to solve this problem.

The following is a sample input and output of the program.

+ Input text file: hw1q4.txt

```
3
Hello World
I have four     words
But I have   five  words
```

+ Compiling the program

```
> g++ -g hw1q4.cpp -o hw1q4
```

+ Running the program and the output

```
> ./hw1q4 hw1q4.txt
5
4
2
```

As you can see from the sample, the text file has the number 3 as the first line, which indicates there are three text lines in the file. The program is printing the number of words in each line in reverse. It is initially printing the number of words in the last line and so on.

**Hint**: In order to read the filename as a command line argument in C++, you need to use a slightly different syntax for your `main` function: `int main (int argc, char * argv[])`. Here, `argc` is the total number of arguments that the program was given, and `argv` is an array of strings, the parameters the program was passed. `argv[0]` is always the name of your program, and `argv[1]` is the first argument. 

###Problem 5 (Dynamic Memory, Strings, 40%)
In this problem, we consider a bunch of buckets, each of which contains a sequence of integers. You have three operations: (1) empty a bucket, (2) put a new sequence of integers into an empty bucket, and (3) output the content of a bucket. What makes this non-trivial is that you will only be given the number of buckets at run time, and the sequences of integers will also have different lengths that you only find out when you read the input file. 

The input file should have the following format: the first line contains two numbers <var>b</var> and <var>c</var>. <var>b</var> is the number of buckets, and <var>c</var> is the number of commands in the sequence. We will not give you upper bounds on either of those numbers. All buckets start empty. Next, we have <var>c</var> lines. Each line contains one of the following three commands:

1. `EMPTY i`: This commands empties bucket <var>i</var>. If there is no bucket <var>i</var>, then it outputs an error `Error - bucket i does not exist`.
2. `PUT i k n1 n2 n3 ... nk`: This commands puts the integer sequence <var>n1</var> <var>n2</var> ... <var>nk</var> into bucket <var>i</var> if bucket <var>i</var> is empty right now; if bucket <var>i</var> is not empty, it outputs an error message `Error - bucket i is not empty` instead. The number <var>k</var> of entries in the sequence will always be at least 1. If bucket <var>i</var> does not exist, then it outputs an error.
3. `OUTPUT i`: Outputs the current content of bucket <var>i</var>. If bucket <var>i</var> does not exist, then it outputs an error.

In your solution, you cannot use any STL functionality, in particular, you cannot use the `vector`, `deque`, or `list` data types. Instead, you should be using `int` and pointers, and dynamically allocate and deallocate memory. A very important part of this assignment is to make sure that your solution does not leak memory. You will lose significant points for memory leaks.

Example:

+ Input text file: hw1q5.txt

```
3 10
PUT   1 4 6 2 2 3
PUT 1   2 5 7
PUT 3  1 0
OUTPUT   1
EMPTY  1
PUT 1   2 5 7
OUTPUT  0
OUTPUT  1
OUTPUT 2 
OUTPUT     3

```

+ Compiling the program:

```
> g++ -g hw1q5.cpp -o hw1q5
```

Running the program:

```
> ./hw1q5 hw1q5.txt
Error - bucket 1 is not empty
6 2 2 3
Error - bucket 0 does not exist
5 7
empty
0
```
