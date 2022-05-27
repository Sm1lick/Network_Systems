<<<<<<< HEAD
# Report for Program №1

Specifying the length of the array:
printf("Enter length of array: ");
scanf("%d", &length);

Allocation of memory for an array. If no memory is allocated, the malloc function returns NULL:
if ((array = (int * ) malloc(length * sizeof(int))) != NULL)

If everything went without errors, the program will clear the allocated memory:
if (array != NULL)
{
free(array);
}

=======
#Report for Program1

Specifying the length of the array:
printf("Enter length of array: ");
scanf("%d", &length);

Allocation of memory for an array. If no memory is allocated, the malloc function returns NULL:
if ((array = (int * ) malloc(length * sizeof(int))) != NULL)

If everything went without errors, the program will clear the allocated memory:
if (array != NULL)
{
free(array);
}

