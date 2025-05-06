---
layout: post
title: Simple Shell
description: I revisit material from Penn's Operating Systems course.
---

I recently submitted an application to be a TA for [CIS 4480](https://catalog.upenn.edu/courses/cis/#:~:text=CIS%C2%A04480%20Operating%20Systems%20Design%20and%20Implementation): Penn's Operating Systems course, which I took in the fall of 2023, my sophomore year. 

A few things have changed about this course. First, back then it was called CIS 3800, and second, I didn't have ChatGPT to help me figure out the bug in my C code causing it to segfault. What hasn't changed is the homework assignments: implementing various cool things such as a [fully-fledged shell](https://www.seas.upenn.edu/~cis5480/25sp/projects/02/shell) and operating system.

A few weeks after I submitted my application, I received an invitation to interview for the course. Like other standard TA interviews, first I had to answer a few questions they had for me, then do a mock office hours debugging session. The questions were all behavioral, and after preparing some responses, I turned my attention towards the more interesting part: debugging. Here were the instructions:

> As a TA, you would go to office hours knowing what the project is, so I will give you a brief summary of the "assignment". The student will be working on a simple shell program, that reads in user-input from the terminal, and executes the specified command with the specified command line args, puts the forked process in its own process group, and tries to
run it in the 'foreground'. You can assume there are no background jobs in this simple shell. This shell will not have to do much other than that, this means that there are no: pipes or redirection, etc that need to be handled by the shell.

Along with a list of the commands the student could use: malloc/free, exit, fork, kill, execvp, waitpid, setpgid/getpid/getpgid, tcsetpgrp, sigaction, sigprocmask, sigsuspend, sigaddset, sigdelset, sigemptyset, getline, strtok, strcmp, printf.

I thought: no better way to prepare for this interview than writing this shell program myself. And so I did, and, well, [here's the result](https://github.com/zminsc/simple-shell).

Here's a few things I liked about writing C:
- I enjoyed the extensive documentation in the Linux manual pages.
- I loved having that extra sense of control over my code.
- I felt extra satisfied building something from the ground up and knowing how it worked.
- Memory management, within the scope of `malloc` and `free` comes very naturally to me.

Here's a few things that sucked:
- Strings. Parsing strings without library functions can be a pain in the butt.
- Signals. I'm still not quite sure how those work in practice and to use them effectively.

All in all, it was good to get some of that practice in my hands before I showed up for the interview. The logical next step is reimplementing the penn-shell homework, but I'll do that when I have more time.

