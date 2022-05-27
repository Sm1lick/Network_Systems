# Report for Program 5

At the very beginning, the program receives a signal from the user and processes it.
Then a global counter variable is set
```
int counter = 0; 
```

Also in the program there are two processing functions - handler1
```
void handler1(int sig)
{
counter++;
printf("counter = %d\n", counter);
/* Flushes the printed string to stdout */
fflush(stdout);
kill(pid, SIGUSR1);
}
```

And the handler2 function
```
void handler2(int sig)
{
counter += 3;
printf("counter = %d\n", counter);
exit(0);
}
```

Processing: The program binds the first processing function to the current process.
Further, if the process turns out to be a child, the handler2 function will process the signal.
