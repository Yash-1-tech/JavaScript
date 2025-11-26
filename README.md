# JavaScript
### Index
1. Constructors, Objectr and deconstructors
2. Pointer Compression
---
#### Constructors
Are used as a blueprint of how a new object would be built.
//first letter capital to signify that its constructor
const Construct(x='a',y='b'){
this.x = x,
this.y = y
}
Object store litrals for properties and and fuctions as methods
const car ={
brand: 'brand',
price:'price',
method: function() {return this.brand +'is for Rs.'+this.price;}
}
#### pointer compression 
Pointer compression is a memory saving technique that is used when the heap size is smaller then 64 bit address space (ofty upto 32 bits).
This works by encoding pointers as offsets of or relative to a base address, which are a contiguous region of memory known as a "heap cage" or "base address".
When accessed the compressed pointer decompresses by adding the base address to the offset, effectively reconstructing the original full pointer.
In V8 this saves upto 70% of heap memory, does limit the heap size 4 GB could be overridden.
