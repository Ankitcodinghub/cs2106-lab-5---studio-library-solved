# cs2106-lab-5---studio-library-solved
**TO GET THIS SOLUTION VISIT:** [CS2106 Lab 5 – studio Library Solved](https://www.ankitcodinghub.com/product/cs2106-operating-systems-solved-3/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;114547&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS2106 Lab 5 – studio Library Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
&nbsp;

Important:

o Exercise 2: 2% [Lab Demo Exercise]

o Exercise 3: 1% o Exercise 4: 1%

– The assignment write-up is adapted to be run on Ubuntu 16.04.

– Lab 5 will be tested on the lab machines (Ubuntu 16.04).

Section 1. Overview

The purpose of this lab is to deepen your understanding of the standard file operations and to introduce you to the concept of dynamic libraries. There are four exercises in this lab and solving them will produce your own mini-stdio library. This library creates a wrapper over the system calls open, close, read, write, and lseek. The purpose of having this library is to reduce the number of system calls made to the OS when working with files.

General outline of the exercises:

• Exercise 1: Defining and initializing the MY_FILE data structure

• Exercise 2: my_fread() + Demo

• Exercise 3: my_fwrite()

• Exercise 4: my_fflush() + my_fseek()

It is strongly recommended to read the whole document before starting to work on this assignment. Before you start, you also need to appropriately setup your environment (as described in this document) to avoid difficulties when compiling your code later.

1.1 Grading

Note that you are not allowed to use the library calls fopen, fclose, fread, fwrite, fseek, fflush for this lab. You need to make use of the system calls (open, close, read, write, lseek) to implement your file operations.

1.2 Compilation and Running

We provide a Makefile to make the process of compilation easier. Running make in the main folder of the assignment compiles the source codes and produces the library libmy_stdio.so, as well as the runner and demo executables. You can then execute ./runner to test your code against a set of tests and check whether your code is working as expected.

Steps in the Makefile:

1. Compiles the ex1-4.c source files into libmy_stdio.so. Note that only files ex14.c and my_stdio.h will be considered for grading and your code should only be added into those files.

2. Compiles runner.c and demo.c linking the my_stdio library. In general, if you want to link the library when compiling your code, you must specify this during the compilation of your code by adding: -L&lt;path_to_libmy_stdio.so&gt; lmy_stdio

3. You can run make clean to remove the files that were produced during compilation.

Before you can successfully execute ./runner, you must set the environment variable LD_LIBRARY_PATH to prompt the loader to search for libraries in the current directory as well when starting programs. Otherwise, if the loader cannot locate libmy_stdio.so, it won’t be able to execute the programs that use it. We propose two ways to set LD_LIBRARY_PATH:

1. Updating your .bashrc file. From lab5 folder (containing the library and the executable), run the following command (one time only):

$ echo ‘export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:.’ &gt;&gt;

~/.bashrc; source ~/.bashrc

You can verify that .bashrc has been properly updated by running:

$ tail –n 1 ~/.bashrc

After this, you can compile and execute the runner after each change in your code:

$ make

$ ./runner &lt; input1.in

Note that runner and libmy_stdio.so must be in the same directory!

$ chmod +x call_runner.sh

After this, you can compile and run the runner after each change in your code:

$ make

$ ./call_runner.sh input1.in

Note that call_runner.sh creates a new process that sets the LD_LIBRARY_PATH and then calls your runner. However, the variable is set only for that process and thus the modification is not persistent.

If you don’t set up your LD_LIBRARY_PATH accordingly, you will encounter this error when trying to execute the runner:

./runner: error while loading shared libraries: libmy_stdio.so:

cannot open shared object file: No such file or directory

1.3 Dynamic Libraries

A dynamic or shared library is created with the purpose of being linked at run-time by other programs. The library can be linked by many programs at the same time, despite having only one instance of it loaded in memory – this can greatly reduce the memory consumption.

On Unix-like systems, dynamic libraries have the extension .so, from (dynamic) shared object, whereas their counterparts on Windows have the extension .dll, from dynamic-link library. Our focus will be on dynamic libraries for Unix-like systems.

Creating a dynamic library

To create a dynamic library, the –fPIC flag must be used during compilation. PIC stands for Position Independent Code and ensures that the generated machine code does not require to be located at a specific virtual memory address in order to work properly. This allows multiple processes to share the library code because they can map it anywhere in their own virtual address space without affecting the proper functionality of the library.

$ gcc –Wall –fPIC –o foo foo.c

Next, we have to turn the resulting object file foo.o into a shared library, which we shall call libfoo.so. To do so, we run:

$ gcc –shared –o libfoo.so foo.o

The –shared flag allows us to create a shared object that can later be linked by other files to form an executable.

Using a dynamic library

To allow bar.c to use functionalities defined in libfoo.so, we have to link libfoo.so during the compilation of bar.c using the –l option. In addition, we also have to specify where the library is located in the system using the –L option. Thus, the compilation command will look similar to this:

gcc -L/path/to/foo -Wall -o bar bar.c -lfoo

GCC assumes libraries to be starting with lib and end with .so or .a, thus –lfoo will look for libfoo.so.

The last step is to inform the loader (i.e., the part of the OS that’s responsible for loading programs and libraries) that it should be looking in /path/to/foo as well when searching for libraries during the program loading. This can be done by adding to /path/to/foo to the LD_LIBRARY_PATH environment variable. Earlier, we instructed you to add ., i.e., the current directory, to the LD_LIBRARY_PATH, so whenever you try running the runner or demo, the directory from which you are running the command will also be searched for libraries.

Miscellaneous ldd: The ldd command prints the dynamic libraries required by a program. You can test it on the runner executable before and after setting up LD_LIBRARY_PATH!

$ ldd runner

Section 2. Implementing the Assignment

The goal of this assignment is to produce a toy version of the stdio library, so all the function names and data structures have the same names defined by the stdio library prefixed by the string my_, capitalized when needed, e.g., instead of having FILE *f = fopen(), we will now have MY_FILE *f = my_fopen(). Your task is to implement buffered file operations that wrap around the primitive file operations. The buffered version essentially maintains an internal intermediate storage in memory (i.e. buffer) to store user read/write values from/to the file.

The data structure MY_FILE is defined in my_stdio.h, together with the prototypes of all the functions you have to implement.

2.1 Exercise 1: Defining and initializing your MY_FILE structure

You can find TODO comments in my_stdio.h and ex1.c to point out what you need to do for this exercise. You can add code in any parts of the code in my_stdio.h and ex1.c.

A MY_FILE structure has been defined in my_stdio.h; at the moment, the structure has only one member, fd. Your first job is to enhance this structure with whatever fields you deem necessary to solve the assignment. We strongly recommend reading all the requirements of the assignment before starting the implementation.

In ex1.c, the function my_fopen and my_fclose have been mostly implemented for you but there is still some work to be done. You are implementing buffered file operations. The buffer size (capacity) is 4096 bytes!

We took the necessary steps to create a file descriptor fd and associate it with the MY_FILE structure. Your job is to initialize the remaining fields of your structure based on how you define it.

int my_fclose(FILE *stream): flushes the stream pointed to by stream and

closes the underlying file descriptor. If successful, the function returns 0, otherwise it returns MY_EOF. The only thing you need to do related to this function is free any memory that your MY_FILE structure used.

You can modify my_stdio.h and ex1.c as you find necessary as long as you ensure that the Makefile still compiles your code successfully. We will use the same Makefile to create your libmy_stdio.so during grading.

2.2 Exercise 2: Implementing my_fread()

Part 1: my_fread() functionality (1 mark)

Your task for this exercise is to implement the functionality of the fread() function; we will call this newly defined function my_fread().

size_t my_fread(void *ptr, size_t size, size_t nmemb, MY_FILE

*stream): The function reads nmemb items of data, each size bytes long, from the stream pointed to by stream, storing them at the location given by ptr. The function returns the number of items read, or –1 if an error occurs.

The purpose of my_fread() is to use the buffer to reduce the number of read() system calls; a correct implementation of my_fread() should call read() only when needed.

Part 2: Demo (1 mark)

Do you remember the behaviour observed in Lab 2 ex1? In this lab, we will replace the fread() calls with my_fread() calls (done for you in demo.c). Your task is to explain what the MY_FILE data structure contains for the parent and child processes, and to specify what will be read for both CASE A and CASE B:

• CASE A: there is an my_fread call done before fork

• CASE B: no my_fread done before fork

demo.c is compiled and linked by the Makefile provided to you. To run the demo, call:

$ ./demo input1.in 4

Or

$ ./call_demo.sh input1.in 4

2.3 Exercise 3: Implementing my_fwrite()

Your next task is to implement my_fwrite() function such that it mimics the functionality of the standard fwrite() function.

size_t my_fwrite(const void *ptr, size_t size, size_t nmemb,

MY_FILE *stream): The function writes nmemb items of data from the location given by ptr, each item having size bytes, to the stream pointed to by stream. Note that if a file is opened in append mode, all writes should be performed at the end of the file regardless of repositioning operations.

The function returns the number of items written, or –1 if an error occurs.

The purpose of my_fwrite() is to use the buffer to reduce the number of write() system calls; a correct implementation of my_write() should call write() only when needed.

2.4 Exercise 4: Implementing my_fflush() and my_fseek()

Your task in this exercise is to implement my_fflush() and my_fseek() functions that mimic the fflush() and fseek() functionalities, respectively.

Part 1: my_fflush

int my_fflush(MY_FILE *stream): The function forces the buffered data for the given output stream pointed by stream to be written via the stream’s underlying write function (i.e., my_fwrite()). For input streams, my_fflush() discards any buffered data that has been fetched from the file. The function should return 0 if the operation is successful, or MY_EOF otherwise.

You can see an instance of my_fflush() being used when my_fclose() is called.

Part 2: my_fseek

int my_fseek(MY_FILE *stream, long offset, int whence): the

function sets the file position indicator for the stream pointed to by stream. The new position, measured in bytes, is obtained by adding offset bytes to the position specified by whence. The whence can take 3 values:

− SEEK_SET: offset is relative to the start of the file

− SEEK_CUR: offset is relative to the current position indicator

− SEEK_END: offset is relative to the end-of-file

The standard fseek() function returns 0 upon success and –1 if an error occurs. However, the value returned by my_fseek() should indicate the new value of the file offset as measured from the beginning of the file, or –1 if an error occurs. You should implement my_fseek() using lseek() system calls.

The SEEK_SET, SEEK_CUR and SEEK_END values are defined in unistd.h and take the values 0, 1, and 2 respectively. Note that the runner expects these values to be given as numbers.

2.5 Testing Your Implementation

Nota bene: When a file allows both reading and writing operations, the standard specifies that:

• fread() cannot follow fwrite() without a prior call to fflush() or positioning function (e.g., fseek())

• fwrite() cannot follow fread() without first calling a positioning function.

We will follow the same convention in testing your implementations for my_fread and my_fwrite.

You can test your implementation by using runner.c. The runner reads commands from an input file; the commands specify what file operation to be performed in the following template:

− my_fopen &lt;file-name&gt; &lt;mode&gt;

− my_fclose &lt;file-name&gt;

− my_fread &lt;file-name&gt; &lt;number-of-items&gt;

− my_fwrite &lt;file-name&gt; &lt;number-of-items&gt;

− my_fflush &lt;file-name&gt;

−

my_fseek &lt;file-name&gt; &lt;position&gt; &lt;whence&gt;

Note that when writing, the runner will write the letters from a to z repeatedly until it writes as many bytes required by my_fwrite() function call (each letter is one byte).

Executing each command prints a message to STDOUT, prefixed by the letter S or F, specifying whether the command was executed successfully, or the command failed (i.e., an error has occurred). Note that an S does not necessarily mean the output is correct, it only specifies that no errors were encountered while executing the command. Similarly, an F does not mean the output is wrong, it simply indicates that executing the command resulted in an error. There are a few errors that will immediately terminate your program, e.g., incomplete commands or if the runner is unable to allocate memory. Failure to allocate a MY_FILE is not considered a fatal error since it can also happen if the file is opened for reading but the file does not exist.

You can redirect the output of the runner to another file using &gt;, e.g., you can call runner like this:

$ ./runner &lt; input1.in &gt; input1.out or

$ ./call_runner input1.in &gt; input1.out

The correct output for input1.in can be found in input1.out. You can check that your output matches the correct one using diff, e.g., diff –b input1.out &lt;youroutput&gt;.

Input:

my_fopen runner.c r my_fread runner.c 101 my_fopen rummer.c r my_fopen test.txt w+ my_fwrite test.txt 5 my_fseek test.txt 3 0 my_fread test.txt 1 my_fseek test.txt 0 2 my_fwrite test.txt 4096 my_fflush test.txt my_fclose test.txt my_fopen test.txt a my_fwrite test.txt 10 my_fflush test.txt my_fclose test.txt my_fclose runner.c my_fopen test.txt r my_fread test.txt 3

my_fclose test.text my_fclose test.txt

Expected output follows:

S: File runner.c is now open

S: 101 bytes were read from file runner.c

F: Could not open file rummer.c

S: File test.txt is now open

S: 5 bytes were written to file test.txt

S: File offset of file test.txt is now at position 3

S: 1 bytes were read from file test.txt

S: File offset of file test.txt is now at position 5

S: 4096 bytes were written to file test.txt

S: File test.txt was flushed

S: File test.txt is now closed

S: File test.txt is now open

S: 10 bytes were written to file test.txt

S: File test.txt was flushed

S: File test.txt is now closed

S: File runner.c is now closed

S: File test.txt is now open

S: 3 bytes were read from file test.txt

F: File test.text is not open

S: File test.txt is now closed

Section 3. Submission

Zip the following files as E0123456.zip (use your NUSNET id, NOT your student no

A012…B, and use capital ‘E’ as prefix):

a. my_stdio.h

b. ex1.c

c. ex2.c

d. ex3.c

e. ex4.c

Do not add additional folder structure during zipping, e.g. do not place the above in a “lab5” subfolder etc.

Please ensure you follow the instructions carefully (output format, how to zip the files etc). Deviations will be penalized.
