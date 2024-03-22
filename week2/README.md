# System review

### Interrupt Cycle

Need the interrupt for asynchronous events. Such as Mouse.

When Doing interrupt need to remember the before interrupt location. Put in stack and go back after handling interrupt. This is called context. This is so fast we cannot even Feel it.

### IO

For OS is to set the value to the buffer and read from the buffer.
For File system will be the one who give the input to buffer.

Writing and Reading is asynchronous Event.

OS does not know when the IO will finish.
Without interrupt OS will keep waiting for the IO to finish it's work. This will cause busy wait.
Interrupt will solve this problem. OS will tell the IO to do certain job and go back to previous work and when interrupt comes, do that work.

For the volumn need the copy as interrupt for buffer to volumn.

For short-IO using interrupt will allow cpu not wasting time.
However IO is really long. IO might change the sequence of the order. When 1 is the first and 3 is next, the IO might give 3 first and 1 last leading IO error.

So we have to wait for IO and this is causing the rest.

Programming and Task.

Multiprogramming is how to run the code separately and Multitask is ho much it can do

### CORE

Is CPU. MultiCore = Many core packaged in one CPU

### Cache

Faster access. Mount frequently used data.

L1 caching is inside the CPU very small.
L2 caching is bit far.
L3 is outside the CPU.

Coherence Problem. When writing cache memory is not updated.

- Writing through is not gonna work because
- Write back. When have multi core this will also cause problem because it is not updated the memory.
