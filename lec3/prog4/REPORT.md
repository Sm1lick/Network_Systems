# Report for Program 4

First, the program calls the fork() function, which creates a child process
> int pid = fork();

Then the application will output the PID of the processes in which it is located
> printf("my pid =%i, returned pid =%i\n", getpid(), pid);
