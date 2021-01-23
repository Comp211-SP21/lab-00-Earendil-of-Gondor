# Lab 00

## Part 0

#### Set Up Your Environment
To complete the labs for this course, you will need to learn how to work with a 
UNIX command-line interface. Go to the Readings section of Sakai and read Chapter 0 of *Learn a Command-line Interface* by Kris Jordan:
[Getting Started](https://sakai.unc.edu/access/content/group/bcb48c3b-5188-4ec4-ac95-ac2b53652fc7/Readings/learn-a-cli-ch0-getting-started-1.pdf) (also available in this repository). Go through the *Getting 
Started* section, to set up an ubuntu Docker image on your computer. Having 
everyone use the same UNIX environment simplifies the coding and grading process.

*Note: if you use a Linux-based operating system, you can follow the instructions 
for macOS, just find the respective Linux Docker installation instructions.*

#### Learn the CLI
Read Chapters 1 and 2 of *Learn a Command-line Interface* by Kris Jordan: [The Sorcerer's Shell](https://sakai.unc.edu/access/content/group/bcb48c3b-5188-4ec4-ac95-ac2b53652fc7/Readings/learn-a-cli-ch1-sorcerers-shell.pdf) and [Directories, Files, and Paths](https://sakai.unc.edu/access/content/group/bcb48c3b-5188-4ec4-ac95-ac2b53652fc7/Readings/learn-a-cli-ch2-directories-files-paths.pdf). This will teach you everything you need to know about running programs and navigating directories in your UNIX environment. Make sure you practice running the commands in the environment! The shell will be your playground for the semester, so gain familiarity with it.

#### Learn Vim
Vim is an extensible text-editor program that is included in most UNIX systems.
It is designed to make changing any kind of text very efficient, though it may not
seem so at first. Start your ubuntu environment that you set up earlier and type
`vimtutor`. When you press enter, a tutorial document will be opened with `vim`
explaining how to use it.

It will take a while before you remember 
everything from the tutor. We recommend you just learn enough from `vimtutor` to
be comfortable enough to complete Part 1 of the assignment in vim, then you can go
back to `vimtutor` or look at online guides for the next two weeks to learn more as you go.

If you cannot learn vim or another terminal-based editor for religious reasons, 
you can open your preferred graphical text editor and edit files from 
`learncli211/workdir`. 

**Mac/Linux:** When you run `./learncli.sh` and start the Docker image,
Docker will create the `workdir` directory that is bridged between the image and your native 
operating system, where you can copy and move files between the the two.

**Windows:** When you run `./learncli.ps1` and start the Docker image,
Docker will create the `workdir` directory that is bridged between the image and your native 
operating system, where you can copy and move files between the the two.

The following labs will assume that you are using vim, and we encourage you to 
take the opportunity to get a basic familiarity with vim during this class. Even 
if you do not become proficient in `vim`, a basic understanding will (probably) 
help you in later courses and in life.


*Note that the `vim` in your Docker image has been optimized for the C programming language and may look different than `vim` on your home computer.*


## Part 1. Hello World
First, clone this Git repository within your shell with the command `git clone respository_url` In place of where `respository_url`, you should enter the URL of your repository; e.g. `git clone https://github.com/Comp211-SP21/lab-00-username`.

In your repository, use `mkdir` to make a new directory named exactly `0-hello-world`. Use `cd` to change your working directory to be this
subdirectory. For reference on how to carry out either of these tasks, please refer to Chapter 2: *Directories, Files, and Paths*.
Next, you’ll want to edit a new file named hello.c. To begin editing this file in vim, simply run the command:
```
vim hello.c
```
Each source file in COMP211 will begin with the standard header comment below. Note this header is checked by the
autograder for an exact match. Please be sure to format your PID as a single 9-digit number with no spaces nor
dashes. Additionally, be sure your capitalization and punctuation of the honor code pledge are correct. Since we do
grade manually for style we do not include names on code listings to avoid biasing the grading.
```
// PID: 9DigitPidNoSpacesOrDashes
// I pledge the COMP211 honor code.
```
Now refer to section 1.1 of *C Programming Language* to complete the rest of the assignment.

#### `hello.c` Requirements
The purpose of hello.c is to slightly extend the book’s (*C Programming Language*) implementation of the same program on Page 9. Your
implementation should print “hello, world” on one line, “welcome to c!” on another line, and return `EXIT_SUCCESS`.
To return `EXIT_SUCCESS` you will need to import `stdlib.h`, the header file which defines this constant. When main
returns `EXIT_SUCCESS` it indicates the program completed successfully via a success exit status. We will explore the
idea of exit statuses later this semester. Additionally, in 211 we expect all function return types to be defined and
main should return an int.

#### Compiling and Executing
You can compile and execute your program with the following shell commands:
```
gcc -Wall hello.c
./a.out
```
The `-Wall` flag tells `gcc` to print out all warnings.
Once your program compiles without warnings and meets the requirements, you can continue on.

## Submit your assignment
Assignment submissions will be made through [GradeScope](https://www.gradescope.com).

You should already be enrolled in the COMP 211 Spring 2021 course on GradeScope. If you are not, you may join with the entry code: **6PZ4E8**.

To submit your assignment, you must commit and push your work to this repository using git. You are likely unfamiliar with git at this point, so just follow these steps:

1. Navigate to the base folder of the repository within Docker. Enter the command `ls` to confirm that it contains the directory `0-hello-world` and ensure that the file `hello.c` is in that folder.
2. Type `git status`. You should see a list of changes that have been made to the repository.
3. Type `git add *`. This signals that you want to place all modified / new files on the "stage" so that their changes can take effect.
4. Type `git commit -m "Your Message Here"`. This shows that you are "committing" to the changes you put on the stage. Instead of Your Message Here, you should write a meaningful message about what changes you have made.
5. Type `git push origin main`. This takes the commit that was made locally on your machine and "pushes" it to GitHub. Now, when you view this repository on GitHub you should be able to see the changes you've made, namely the addition of `hello.c`!
6. Go to the COMP 211 course in GradeScope and click on the assignment called **Lab 00**.
7. Click on the option to **Submit Assignment** and choose GitHub as the submission method. You will be prompted to sign in to your GitHub account to grant access to GradeScope. When this occurs, **make sure to grant access to the Comp211-SP21 organization**.
8. You should see a list of your public repositories. Select the one named **lab-00-yourname** and submit it.
9. Your assignment should be autograded within a few seconds and you will receive feedback.
10. If you receive all the points, then you have completed this preliminary lab! Otherwise, you are free to keep pushing commits to your GitHub repository and submit for regrading up until the deadline of the lab.

## Check your understanding
The purpose of this lab is to make sure you have some basic familiarity with the tools of this course, namely: your ubuntu environment, vim, and git. You will earn full credit for this lab by simply submitting the short `hello.c` program, but it would behoove you to spend some extra time learning the shell commands, vim keystrokes and understanding git. If you would like to learn more beyond what was included in the lab writeup, here are some additional resources created by Kris Jordan:

* [What is vim? A brief history and motivation](https://www.youtube.com/watch?v=zGArLWTHWRw&list=PLKUb7MEve0TjHQSKUWChAWyJPCpYMRovO&index=2)
* [Starting and Exiting vim Sessions](https://www.youtube.com/watch?v=CLzVPdg0lF8&list=PLKUb7MEve0TjHQSKUWChAWyJPCpYMRovO&index=3)
* [The Grammar of vim - an introduction to the fundamental movements and actions](https://www.youtube.com/watch?v=cSeQY5x-hbo&list=PLKUb7MEve0TjHQSKUWChAWyJPCpYMRovO&index=6)
* [What is a version control system? What is git?](https://www.youtube.com/watch?v=h2xylPqXO8M&list=PLKUb7MEve0TjHQSKUWChAWyJPCpYMRovO&index=4)
* [git Fundamentals - add, commit, branch, checkout, merge](https://www.youtube.com/watch?v=R8E29zB8tMc&list=PLKUb7MEve0TjHQSKUWChAWyJPCpYMRovO&index=5)
