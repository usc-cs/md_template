---
layout: default
title: Assignments
nav: assignments
---

##Assignments
Homework will be assigned roughly once per week. It will be graded, and require substantial work. The average student should expect to spend about 15 hours per homework. Homeworks will typically contain a mix of programming exercises and "theory" questions about data structures and their implementation. Roughly every third homework will contain a piece that contributes toward the class project, which is to build a simpler version of Netflix from scratch. As the project progresses, students may find it necessary to revisit and improve their earlier solutions, so good coding practices and documentation are strongly encouraged.

For detailed information on late submission policies, grace periods, and similar questions about assignments, check the [grading page]({{ site.url }}/grading.html).

Homeworks will from time to time contain "chocolate problems". Chocolate problems do not affect your grade in the course. They are intended to be significantly more challenging, for students looking for a challenge. Chocolate problems will be marked with a number of chocolate bars. Solutions that are (mostly) correct will lead to the solvers getting that number of chocolate bars. Chocolate problems can be solved in groups of up to 3 students (who will then share the chocolate). Chocolate problem submissions should be separate from the rest of the homework, and should be e-mailed directly to your instructor, as they will be graded by the instructor, not the TAs/graders. Feel free to mark your preferred type of chocolate with your submission, though we won't promise that we will meet all requests.

Each student will receive a private code repository on the course's [GitHub Organization](https://github.com/usc-csci104-fall2014) to use it for the development and submission of all assignments. You will be using the [git](http://git-scm.com/) source code management tool to maintain your homework code. 

###HW Schedule

|                      HW                          |           Topic                             |                Due Date                  |
| :----------------------------------------------: | :-----------------------------------------: | :-------------------------------------:  |
| [**HW01**]({{ site.url }}/assignments/hw1.html)  | Course Overview and Review                  | Fri. Sept. 5, 2014 @ 11:59PM (PST)        |
| [**HW02**]({{ site.url }}/assignments/hw2.html)  | Recursion, git, makefiles                  | Fri. Sept. 12, 2014 @ 11:59AM (PST)
| [**HW03**]({{ site.url }}/assignments/hw3.html)  | Linked Lists, ADTs, Map, Set               | Fri. Sept. 19, 2014 @ 11:59AM (PST)        |
| [Project, Part 1]({{ site.url }}/assignments/hw4.html)  | Part 1 of Project  | Wed. Oct. 1, 2014 @ 11:59AM (PST)        |
| [**HW05**]({{ site.url }}/assignments/hw5.html)  | Stacks, Running Time, Inheritance           | Thu. Oct. 09, 2014 @ 11:59PM Midnight (PST)        |
| [Project, Part 2]({{ site.url }}/assignments/hw6.html)  | Part 2 of Project  | Wed. Oct. 29, 2014 @ 11:59PM (PST, midnight)        |
| [Project, Part 3]({{ site.url }}/assignments/hw7.html)  | Part 3 of Project  | Fri. Nov. 07, 2014 @ 11:59PM (PST, midnight)        |
| [**HW08**]({{ site.url }}/assignments/hw8.html)  | Sorting, Runtime Analysis, Recursion, Searching, Heaps | Sun. Nov. 16, 2014 @ 11:59PM (PST, midnight)        |
| [**HW09**]({{ site.url }}/assignments/hw9.html)  | Search Trees, Graph Search | Wed. Nov. 26, 2014 @ 11:59PM (PST, midnight)        |
| [Project, Part 4]({{ site.url }}/assignments/hw10.html)  | Part 4 of Project | Mon. Dec. 8, 2014 @ 11:59PM (PST, midnight)        |
  
###Submission Instructions
In order to properly submit your assignment, please follow the course [submission instructions]({{ site.url }}/assignments/submission-instructions.html)

###Rubric
Each homework assignment generally asks for a set of features to be
implemented in C++. It also usually asks students to specifically
either use or not use some STL classes. Based on these requirements,
each assignment is going to have its own grading rubric. We also have
a general rubric which you need to consider for *all* assignments;
this captures issues that will be common to most of your projects,
like quality of your code. 

####General Rubric
**Coding problems**

 + Up to 3% deduction for using global variables inappropriately or extensively in your program.
 + Up to 5% deduction if your code compiles with warnings. It depends on the number of warnings and their severity. In order to see the compiler warnings, you need to compile with the `-Wall` switch. For example `g++ hw1.cpp -Wall -g -o hw1`. If you believe the warnings are unavoidable document it in your README file.
 + Up to 5% if you do not use command line arguments correctly (hard code or use cin).
 + Up to 3% deduction for each compiler error depending on the severity of mistake.
 + Up to 10% deduction for bad Makefile (once Makefiles are taught).
 + Up to 20% deduction for bad coding practices, code organization, indentation, naming, code file and header separation, code documentation, throwing non-exception types, etc.
 + Up to 10% deduction for repo organization, garbage files in repo, folder organization, repeated code files, missing data files, missing README file, etc.
 + Up to 10% deduction if your program is testable but crashes during execution, leaks memory, or is considerably slow. Depending on the nature of the assignment, you may lose more points if your program is slow or not scalable.
 + If one of the features of an assignment is not testable because it has major compile errors, you will likely lose at least half its points in addition to other coding mistakes. For example if we cannot test one of your data structure functions because it is missing the UI section (main function) or it has major compile errors, then the best we can do is to look at your code and see if it would work or not. In this scenario, we can give you at most half the points for that data structure function.
 + Similar to the previous rule, if your project is missing a key feature such that testing many other features depends on it, you will likely lose a lot of points. For example, imagine that your assignment is supposed to read data from a file and then process. If you finish the processing part and leave out the file I/O part, you are making it very difficult to test your project. If you want to leave out the file I/O (maybe because you do not have time), change your main function so that it generates some data (like an initial array) just to test the rest of your assignment. This actually makes it easier for yourself to test your assignment as you build. If you want to learn more about this, look up *unit testing*.

**Multiple choice problems**

 + If you miss 1 on a problem of several possible answers, you get 50%.
 + If you miss more than 1 on a problem with multiple correct answer, you get 0.
 + If you miss the 1 right answer (if there's only 1 correct answer), you get 0.
