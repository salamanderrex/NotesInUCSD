# Singularity

## previous shortcoming:
- widespread security vulnerabilities;
- unexpected interactions among applications;
-  failures caused by errant extensions, plug-ins, and
drivers, and
- a perceived lack of robustness. (blue screen)




- First, the pervasive use of safe
programming languages eliminates many preventable defects,
such as buffer overruns. 
- Second, the use of sound program
verification tools further guarantees that entire classes of
programmer errors are removed from the system early in the
development cycle.
- Third, an improved system architecture stops
the propagation of runtime errors at well-defined boundaries,
making it easier to achieve robust and correct system behavior


### software-isolated process:

previous paper: microkernel 

Differetnce, it is on software not use hardware protection. not like on the hardware (seperate hardware space) previously on the HYDRA.

### Why not hardware? 

Communication between SIPs incurs low overhead and SIPs are
inexpensive to create and destroy, as compared to hardware
protected processes 


### how to communicate?

Channel based on exchange heap.

Communication between SIPs occurs by `transferring the exclusive
ownership of data in messages`. A linear type system and a special
area of memory known as the exchange heap allows lightweight
exchange of even very large amounts of data, but no sharing.


# kernel runs on user sapce with other use applicaion. How to keep kernel GC sperate from other ?
when system call, kernel still at the user heap. But there is a red line seperate them

## contract-base band
only send what agree to send


## unsafe code tax
