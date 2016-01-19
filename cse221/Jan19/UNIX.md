# The UNIX Time Sharing System

## File system

** I/O as file  **

- UNIX : open read write in order sequentially
- MULTIS:  M map, read file into memory, read and modify file in memory

filename: use /

** buffer **: buffer cache , read entire block .

> ** problem **:  - inconsistent , what is on buffer what is on disk
                            read one byte there, read another there, buffer read a block each time, inefficiently

User cannot create directory?

```
rwxrwxrs_x  root sys  mkdir ( SET-user-UID did bit )
rwxrwxsrwx nobody     mkdir
```

Process:
Keep files to the child

```
$command < file1 > file2
```
```
this will invoke a child process,                                                                                parent (shell)
          call pid = fork()                                                                                                         wait(pid)
          open(“file1”)  -> stdin
          open(“file2”)  -> stdout
          in child, execute the command, exec(“command”)
```

```
$command < file 1 > file2    & <—run in the backend
```

why &?
` command < file1 > file2 & command2 & command3 `

Windows does not have fork…. shell will open the file , then send stdin , stdout  out

UNIX is the u version of MULTIX  ………., unix discard something from MULTIX to make a simplified MULTIX

No lock in unix:
multiple copies to be modified

## Hardware:

- TENEX modifies the hardware to run the OS
- UNIX run the OS without modification of OS
- cheap hardware

## Difference nowadays UNIX
### iNode
in papaer
```
iNode - >direct pointer
      or - >indirect pointer
```

But Now, we use
```
iNode - >iNode -> iNode - >
```

### Protection

- No group, only user and other users

## Virtual memory system
```
UNIUX:   images , no paging -> No paging hardware
TENEX: BBN, paging
```

## Network:
No network in paper
