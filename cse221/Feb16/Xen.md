XEN

L4 linux also modify system to accrodiate haredware 
here you modify guest os 






 guest  guest  guest  
====================
VMM/ hypervisor
==================
haredware
================
bare metal hypovisor

what we use in daily life?
Like L4
Fusion  (VMM)   Guest1 Guest2
OS X 
HW 
============
hosted VMM


# change os not ABI (system calls)


resource isolation 


# why not full virtualization 
MMU 
silently rather than causing a convenient trap (user process meets exception to system, hypervisor need to virtualization all it.  )

CPU 
has  own schduler 


memory in XEN
Xen does not care the virtual memory but if he guest os want to use the physical address directly. It will check whether the OS visit the haredware which is assigned to.



ballon driver 
