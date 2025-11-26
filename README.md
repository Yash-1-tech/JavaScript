# JavaScript
### Index 
1. Pointer Compression
---
#### pointer compression 
Pointer compression is a memory saving technique that is used when the heap size is smaller then 64 bit address space (ofty upto 32 bits).
This works by encoding pointers as offsets of or relative to a base address, which are a contiguous region of memory known as a "heap cage" or "base address".
When accessed the compressed pointer decompresses by adding the base address to the offset, effectively reconstructing the original full pointer.
In V8 this saves upto 70% of heap memory, does limit the heap size 4 GB could be overridden.
