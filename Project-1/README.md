Student Info:
Name: Anthony Villalobos 
Student ID: 008394627 

Project 1: Remote GitHub Development and Performance Monitoring


Project Questions:


1. Which program is fastest? Is it always the fastest?

Based on the avg times of the trials it can be concluded that malloc was the fastes of these operations. On average it gave the fastest times although alloca was a close second except when given large lists it would take forever and sometimes crash. 

| Program | Avg Time Tested Using 20,000 blocks, O2 |
|----------|---------------------------------|
| malloc.out | 0.28 |
| alloca.out | 0.30 |
| new.out | 1.08 |
| list.out | 1.14 |

2. Which program is slowest? Is it always the slowest?

List would constintly be the slowest of the 4 

3. Was there a trend in program execution time based on the size of data in each Node? If so, what, and why?

There was a clear difference in the runtime when having small sized data and large sized data especially with alloca sometimes not being able to finish running when using very large data sets. But as the data set became larger then the runtime would also increase.

| MIN/MAX | Avg Time |
|------------------|--------------|
| 10 / 10 | 0.000385 |
| 32 / 4096 | 0.0825 |
| 256 / 8192 | 0.1706 |


4. Was there a trend in program execution time based on the length of the block chain?

Yes, there was a visable trend as the num of blocks increased then so did the avt time. If the num of blocks doubled then the avg time would also double. 
| NUM BLOCKS | Avg Time |
|-------------|--------------|
| 10,000 | 0.0423 |
| 20,000 | 0.0825 |
| 100,000 | 0.4081 |
| 1,000,000 | 4.0863 |

5. Consider heap breaks, what's noticeable? Does increasing the stack size affect the heap? Speculate on any similarities and differences in programs?

Since alloca allocates dirrectly on the stack it doesn't need as many breaks as compared to the other functions since they use heap memeory.

| NUM BLOCKS (20,000) | Heap Breaks |
|-------------|--------------|
| Alloca | 66 |
| Malloc | 381 |
| List | 385 |
| New | 385 |


6. Considering either the malloc.cpp or alloca.cpp versions of the program, generate a diagram showing two Nodes. Include in the diagram
the relationship of the head, tail, and Node next pointers.
show the size (in bytes) and structure of a Node that allocated six bytes of data
include the bytes pointer, and indicate using an arrow which byte in the allocated memory it points to.

head -> nodeA --> nodeB --> null
          |         |
      (6 bytes)  (6 bytes)
tail ----------------^




7. There's an overhead to allocating memory, initializing it, and eventually processing (in our case, hashing it). For each program, were any of these tasks the same? Which one(s) were different?

The programs all intialized it and hashed it the same however their allocation was different in all of the prorgrams like alloca, malloc, new, and list all useddifferent allocation methods. 

8. As the size of data in a Node increases, does the significance of allocating the node increase or decrease?

It decreases since we focus more on processing the large data that the time spent allocating become less important to the total runtime. 


