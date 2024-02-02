COMP 251 NOTES

OS doesnt run anything until woken up
to wake the kernal, interupt with: 

        ret = write (fd, buff, size);

user mode vs kernal mode

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

1. x++ reads variable first then increments
2. ++x adds first then increments

.

        sizeof(x)

sizeof is an operator (not function) to find amount of bytes associates with type

        scanf("%d", &x);

the location in memory is gotten from the &

anything before the %d will be required as a must for input, almost like a password

curly braces are optional in an else to an if block ( if the else is one statement)

indents dont matter at all

when numbers are too large for their type, they roll over into the negatives for example 9999999999 would be less than 9, because it reads in that first number as some negative number

function prototype gives a signiture of a function doesnt define the function