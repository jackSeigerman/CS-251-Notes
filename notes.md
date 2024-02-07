>COMP 251 NOTES


OS
-
OS doesnt run anything until woken up
to wake the kernal, interupt with: 

        ret = write (fd, buff, size);

user mode vs kernal mode
-
multiprogramming 
 a process is an os abstraction of a running program
 many os's support many programs running concurently

 to start a process:
 1. load instructions into ram, create and initialize new process, initialize cou state to run process

 kernal gets launched from bios, or booting

 kernal is core os fucntionalty for interfacing the hardware and I/O

tmux creates a new window with a consistent connection

you need another program or an interpertor to run code from python or java

c interpetor is 

        clang -o 

programming contraints
-
1. comments 
2. variables - initialization, delceration
3. I/O functions
4. statements (how they are indicated)
5. conditioanls - truth values
6. functions - call, define
7. loops
8. acess

/# include in c allows for pre compilation like import in PY

        #include <>

all variables and methods need to have a type

if method has no inputs then you put void in that spot

        int main(void)

haveing a return is like an error code for main

" is string literals and ' is used for chars


        #include <stdio.h>

        int main(void)
        {
                printf("Hello, World!\n");
                return 0;
        }

variable attributes
        name
        value
        size
        type
        location (in memory)
        scope
        lifetime

c does not have garbage collection (reallocation of unused memory automatically)

multiple declorations of variables on the same line

        long i, j, k;

other types are

1. int
2. long
3. char
4. float
5. double

chaining works in c (right to left)

        x=7
        i=j=k=x+2

all equal from right to left

asighnments return a value

0 is false and every other numver is true

ASCII encoding for letters to equal numbers

so char is technically sharing a value as an int so like 'A' is 1

format modifiers for printf
>(man 3 printf gives more info on the modifers)

/ is integer division "floor division"

unsighned before an int or double allows for no negative numbers but larger positive range

order of operations
-
1. x++ reads variable first then increments
2. ++x adds first then increments



        sizeof(x)

sizeof is an operator (not function) to find amount of bytes associates with type

        scanf("%d", &x);

the location in memory is gotten from the &

anything before the %d will be required as a must for input, almost like a password

curly braces are optional in an else to an if block ( if the else is one statement)

indents dont matter at all

when numbers are too large for their type, they roll over into the negatives for example 9999999999 would be less than 9, because it reads in that first number as some negative number

function prototype gives a signiture of a function doesnt define the function

there are no strings in c

man page sections
-
1. command line utilities (ls)
2. system calls (stat)
3. library calls (printf)


for project 1 (making ls) only have to worry about - or d (file or directory)

&& runs command directly after another

        gcc -o name name.c && name.c

        //this compiles and runs code in one line
 

types
-
- int
- float
- char
- double

arrays
-
name x, type int, values set equal to 0

- int x[5] = {0,0,0,0,0};
- int x[5]; x[0] = 0;

there is no bounds checking in C
- *"you better get your indexing correct"*

there is not index out of bounds error, rather going out of bounds goes to the next or prev or rather in relation memory in regaurds to how far you have gone. Basically all memory is kinda like a large array and going out of bounds just goes to a peice of memory.

- char [size] x;

sizeof(x) would return size if chars
but other size if other types, also only works in main

to tell size of an array you can counter variable

1. track size explicitly (direct)
>- loop through and send length with array into a function
2. sentinal value
>- add a single character at the end that tells when to stop a loop for counting '\0'.
>- name[0]= 'm'; name[1]='e'; name[2]='\0'; withe \0 being the sentinal value

segmentaion fault is when you start acessing memory that you are not supposed to, so if you call a length function on an array with no null terminator, it will go until it finds one, or maybe even never finds it.

STRINGS
-
strings can be made of an array of characters or Chars

- char [size] x;

sizeof(x) would return size if chars
but other size if other types, also only works in main

Look above for parsing and tracking string size
>string uses
- Strlen (find length)
        - returns length of array minus the sentinal value.

- Strcat (concatinate)
        -

- Strcmp (compare)
        - returns an int so that of two strings = then val  is 0, if s1 is less than s2 return -num else positive 

- Strcpy (copy)
        -

- Strdmp (something with pointers)
        -


Truth in C 
-
0 = false, everything else is true

        if(operation that = 1){
                //code executes
        }
-

        if(operation that = 0){
                //code doesnt execute
        }
-

        if(s[1] == 'j'){
                //code executes if that char is j
        }

Structures
-

closest thing C has to classes

        struct studentT
        {
                char name[65];
                int age;
                float gpa;
                int grad_yr;
        }

readdir returts a struct