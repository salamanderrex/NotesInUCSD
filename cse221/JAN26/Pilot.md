# Pilot
No sehculding between users because only one user
## mesa couple with system 
## file
## virtual memeory: single memory address No memory proectection between apps
    Mesa is a strong type lanuage
    what good comes with strongly type message ?
        memory allocation is simplified
        Operation on pointer can be checked before dereference (different from c)
        put restrictions on the compiler on the compiling time
       
       Hints in Virtual memory?
       Active 
       Deavtive 
       Kill
       Becuase it provides more support and improve performance
       
       Why muiltiprogram cannot use this?
        Pilot is only one user. 
        Timesharing can also provide hint if it only impact itself.

mesa is the where the scheduler is. Pilot does not cover the schdeduler. it give to the mesa run time to deal with it.
   becuase mesa is the only language of the system. 

reading file:
    - UNIX: everything is file. 
    - alternative: memory map   
 Pilot is memmory mapping. 
 
 what get from memeory mapping?
    use all protection system for memory.
    use vm system as dispatch buffer cache.
    Not too much overhead to read,write, seek.
    
    
Couple bits of the files?
- size
- type
- permancene :  swapper space can save data if system break
- immutability: file name is unqiue, if you wan to share a file. If two files have same name and content. If set immutable, then no one can modify the file


# Network
Pop protocal 
 Unix call it pip , here called streams, but a slight different
 Nowadays, Unix has both pip and stream.
 
 
 # virtual memory implemntation
 djsk - layer but problem is that : circular dependency. (I have a page falut, call page system, but page system is alse swapped. then circular )
 there - manager/kernel.  Sepeate low level and high level.   
                just like policy/mechanism. recall policy/mechanism   (Hydra. mechasnism how you actully make things done)
                

If there is a windows, it has a problem like blue scree.
but here, it will go the a debugger. called coPilot. You can fix it.
               
The notion of the personal computer is just like the cellphone we are using. for example, our cellphone nearly does not have the multitasking. It will kill the app when you run other app.

                
 



         
        

