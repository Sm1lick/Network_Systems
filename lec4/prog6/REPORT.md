# Report for Program 6

The program creates an array of file descriptors.
After that, the application will check the correctness of the input and output an error message if there is one
```
if (argc != 2)
and
if (pipe(pipefd) == -1)
```

Then the program will call fork() of the child process PID of the child process. Next, the application will check the newly received PID. The child element has this ID equal to zero. Next, the parent process writes something
```
close(pipefd[0]);
write(pipefd[1], argv[1], strlen(argv[1]));
close(pipefd[1]);
wait(NULL);
exit(EXIT_SUCCESS);
```

And the child reads the data
```
if (pid == 0)
{
close(pipefd[1]);
while (read(pipefd[0], & buf, 1) > 0)
write(STDOUT_FILENO, & buf, 1);
write(STDOUT_FILENO, "\n", 1);
close(pipefd[0]);
_exit(EXIT_SUCCESS);
}
```

In this way, communication between processes is realized using a common channel.

