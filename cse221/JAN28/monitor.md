# monitor
## monitor is sync in JAVA

why called monitor is for os?
- because os is monitor on data, way to build os

monitor 
- key word of monitor : mutual exclusion
    - has a queue to keep track of prcosee want to get data.
    - condition variable: I need to wait for something, then block in the monitor
    
    monitor invariant? get monitor back to state to let others comes in 


    I  <= invariant (in the monitor)
    when you get in the monitor, you can mess it up . 
    if you want to leave the monitor, you need to make it back to same
    
    if you want to use a condition variable, you need to make sure invariant true
     I {b: wait} I & B 
     when you left, invariant must be true.     do not wake me up up until the condition is true
     
             |
             |
     I & B {b.signal} I 
     if I and B is true, then call signal b, when you come back, make the invariant
     
     
     
## Semaphore vs monitor

functionally equivalent 


## prombelm?
performance , context is expensive

##  rewrite , used in these days
    I {b wait} I 
    I & B { b signal } I 
    

     
     
    
    