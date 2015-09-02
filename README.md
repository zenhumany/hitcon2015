In 2014, Microsoft introduced two new exploit mitigations, called Isolated Heap and MemoryProtection.
These mitigations greatly increases the difficulty of use-after-free(UAF) vulnerability exploit,
but there are still many ways to bypass the mitigations when the pointer to the freed block didn’t remains on the stack.

In order to completely prevent UAF vulnerabilities exploit，
Microsoft Edge browser introduced a new memory management called MemGC. 
MemGC Use the mark and sweep algorithm for memory management.

In this presentation, the first part will sketch the MemGC Internals by discussing about its data structure, 
its memory allocate, free, mark and sweep. The second part will discuss Why MemGC can effectively prevent the UAF'S exploit. 
The third part will discuss some weaknesses of MemGC.
