# gms
why has space to store information?
becuase has idle node 

# if you lose a page 
sprite if you former process dies, matters a lot 
but for GMS, info in at disk, only need to load from disk

# send to global 
it must make sure it is clean, not dirty (at 3.3)

# 4 cases 
global pages elsewhere 
- swap global pages    L+ G - 
- swap LRU local  L == G ==


pages on teh disk somewhere 
- SWAP global LRU page

shared page on other swap
- P evict a global page     L+  G-

how could a shared page happen?
two client ask for same file for share file server. according to NFS system.

# why not follow the algorithm? They do what instead? 
p203 
cost function of LRU, hence approximate it based on age and store
seperate push and put pages


# use weights 
p203
1. duration elapse  
2. global pages have been replaced 
3. the age information is detected to be inaccurate

# some trick 
minage - save time. if it is bigger than min age, then it must be old 


