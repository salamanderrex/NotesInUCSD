# mesa
TONY immedaite signal the first in the queue
Butler 

- user boradacast? 
    it will call all processes to resume. 

    memory out here? some boady asked for more , then needs to wait. If I have the enough memory, then signal. 
    (unicast signal). in this case, it may wake up a process asked for more memory.
    But if the signaled process asked for less memory, it can run.

    Of course, you can order the queue, let first is smallest. However, it need to restrcut the monitor.

- external procedure.
  becuae some needs mutial excusion, some does not.
  Like java. Some stuff does not need everything.
  
  
- 
    process of monitor can do two things, running or waiting.
    if monitor running parallel on other things. IF I have to kill a process
  
- exception handling in the monitor
    if an exception in the montor. if your monitor does not handle exception, you will buble hte exception up. what about monitor invariant. 
    We do not release lock, it is bad.
    We do leases lock , it is also bad. 
    
    Solutin: try - > catch . if catch cannot handle local, I am about to leave you, clean the mess up. So other came in.
    

|item| Hoare   |    Mesa|    JAVA|
|--:|----------|:-------------:|------:|
| Lock ? | everything    | entry | synchronize|
| condiion variables | y| y* | 1  | 
|  wait  | y | y* | y*|
|signal | inside the montior | inside and outside, broadbase | same as mesa|
|grandularity | code and data | monitor record| arbitrary + class instance|
|abort | No | y |  (java used to have stop(), but deprecate now. If a thread in monitor, then you ask to stop that thread. But montior does not know, hence stop all threads)| 
| nested call| No | yes | y| 


# Monior call as momnitor? how to deal?
Monitor has to wait what it is going to wake.
example:
foo calles                  bee 
    a: wait                              b.wait
    signal.b                             signal.a
    
    
    
# How to prevent deadlock?
define an order for resources
butler gives an example. The system can still running but in the wrong code.
Priority? Page 113

Solution: when thread is wait on the line, check not your prioirty, but the priority of thread calls you.
Java does not have this support.


# Question?
- why java has this monitor thing?
    - lower overhead context switching
    - single user 
    Same address space !!!!!!! (same as pilot, all thread runs int the same space) hence, what used in Pilot can be used on java