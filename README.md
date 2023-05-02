Download Link: https://assignmentchef.com/product/solved-comp3300-assignment-2-creating-and-testing-process-status
<br>
The aim of this assignment is to help students understand how to create processes and how to trace the status of a process. Students will obtain hands-on experience in process creation through the fork system-call and follow up of processes via other system calls in UNIX.

<strong>Tasks: </strong>

<ol>

 <li>Using either a UNIX or a Linux system, write a C program that forks a child process that ultimately becomes a zombie process. This zombie process must remain in the system for at least 10 seconds. Process states can be obtained from the command:</li>

</ol>

ps –l

The process states are shown below the S column; processes with a state of Z are zombies. The process identifier (pid) of the child process is listed in the PID column, and that of the parent is listed in the PPID column.

The easiest way to determine that the child process is indeed a zombie is to run the program that you have written in the background (using the &amp;) and then run the command ps –l to determine whether the child is a zombie process. Because you do not want too many zombie processes existing in the system, you will need to remove the one that you have created. The easiest way to do that is to terminate the parent process using the kill command. For example, if the process id of the parent is 4884, you would enter

kill -9 4884

<ol start="2">

 <li>Write another C program that does #1 automatically. That is, you do not have to enter the commands ps and kill manually. But your program has to: (a) create zombie processes by running your C program of #1, (b) Obtain the state of each process and find if there is any process that is zombie, (c) Show a list of processes with their states, (d) kill the parent of any process that is zombie, and (e) show the updated list of processes with their states.</li>

</ol>