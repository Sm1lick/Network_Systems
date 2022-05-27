# Report for Program 3

Memory allocation for an array of elements of type char
> char * c = (char * ) calloc(100, sizeof(char));

Then the application opens the file foo.txt for reading or creating
> int fd = open("foo.txt", O_RDONLY | O_CREAT);

After that, the value of the file descriptor is output
> printf("fd = %d/n", fd);

The application will read 10 bytes from the file and write the received amount of information to the variable sz
> sz = read(fd, c, 10);


The program will write terminal zero c[sz] = '\0' to the end of the array; and close the file
> f (close(fd) < 0)
> {
> perror("close file error:");
> exit(1);
> }
