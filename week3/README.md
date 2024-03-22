# Week3 Overview for os

## Event handling

Two type of Event
Asynchronous and synchronous

From hardware will be Async Never know when will be called.
When this event is done give interrupt. Every OS has interrupt handler.

Sync: Know when the event is happend. So can called software makde interrupt.

### Exeptions = Synchronous Event

- Trap
  Make the exeptions when the software made for purpose.
- Fault
  recoverable Error. The memory should be there but not there. will call os to make the memory or data.
- Abort
  not recoverable Error. Os cannot handle. Memory bit corruption. Data broken.

### Assembly code

This is available to use in the c programming. Directly access to the system. Much faster. But this is very dangerous

### Dual-mode

Check if User-mode or Kernel-mode to check if it is safe kernel or user made.
This is changed when running system call. In first will be user-mode so cannot access to the memory directly even using assembly.

### process

Is where the program lyes.
Is data structure. program cannot run by itself. Program will be stored in data and ran by os.
The instruction will be very large has a lot of info. In linux will be called task instruct.

How to get to memory -> pointer

Inside the data structure of program will have all the address of the variable, Even the one that `malloc`.

The place recorded will be writen in address space. This will go to memory to run. And the metadata of the application. OS will only know this two.

### file

Is a where you put the data. Every thing about this file will be in metadata. Inside same space. Alongside file data. Filesystem is the one handle this file data structure.

### Services

Two things they do.

#### application call

through system call. Waiting for the service. Name will different for different OS.

- open() : system call
- fopen() : API (C language library)

System call will have to be used with one more process. using system call have to deal with different OS all the
time.

### Virtual machine

Made for developing OS. If using same one will lose many time if error happened cause have to re-install everything.

Now can be used for cloud.

Java virtual machine. Without knowing this can be used in anywhere everywhere.

### Project 1

Now for the homework learn how to do it from [Link to How to make system call](https://medium.com/@mahi12/adding-system-call-in-xv6-a5468ce1b463)
