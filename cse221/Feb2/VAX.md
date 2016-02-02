# VAX/VMS
For entire family hardware.


provie vm for all kinds of machine
## crazy difference
underpower mahine, slow cpu with large memory

scan the memory , walk through a lot of memory. LRU here is expensive.

Address space 


When you using a usr program, the kernel is in your memory address.
It is like sinlge address space. Of ource, there is hardware protection to prevent you modify the kernel.
However, evey process has a address space. how many process then there is how many address address.

## context switch?
it needs to copy the page table. But here page table takes virtual address, which depends on the size of the virtual address. The VAX/VMS has a huge virtual address space, hence, they do not want to
copy the page table here.

when context switch happens?

somepoint somewhere want to switch the between the process.
The schedular decides which should run, decide which process to run.
After the context switch, just user space space changes. The system space keeps the same.

## page table
The system page table and process table. 
The process page table is the virtual memory.
The system page table is in the system page table base register.
Each region has a page table and system has only one page table.

## multiable stack and space
sparse memory address. 


flush only the translation lookaside buffer (TLB)
A translation lookaside buffer (TLB) is a cache that memory management hardware uses to improve virtual address translation speed.

# page tables itself always in the memory?
No. 

The kernel page table is not pagable. This is not problem becuase the designer can define the size of the system page table.

The user page table is pagable and can be swapped out.

# which code actually implement the paging?

The part of code is implemented by the kernel.

## swapper
swapper is a user level program, is not in the kernel.
Why not in the kernel. Becucase they try to make teh kernel small. 
So the swapper is not always in the memory?
 You cannot swap out of the swapper, but you pager is always there. pager can get the page out of the 
memory.

Manage/pattern modle again.

## pictures on 38 
Compare this mecahnism with the FIFO and LRU. 

## process ask for pages, look for a available page list ? 

page list like a queue.
tail                                    head    
--------------------------------------
|                                      | <- get free page
----------------------------------------
----------------100------------------

if we keep this queue a length, just take 100 length of meory and reserve it as free and use it.

If there is a page fault, the OS will check the table. It may find that it is invlaid. However, it will check the free list of page table and find that it is atctually in the memory.
Hence, the OS can mark the memory valid.

This is second change algorithm in undergraduate OS!!

also on dirty pages
when they write the dirty page, it dees not wirte one by one. BUt write on the contagious pages.

Why am doing extra work on page faulting?
If i am page fauling, some process is waiting. Hence we need to consider this problem.
During the page fault, it puts it into queue and upate the valid bits in page table. 





