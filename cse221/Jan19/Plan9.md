# Plan 9 from Bell Labs
## UNIX:
### bad points

- network and GUI
- comparing about management model. If one issue appear, you need to update all and buy all new hardware. (Apple success to convince people to buy new device……)  Much easy for one system to maintain, not one unix for each different machine

## Plan 9 :
protocol - > 9P
everything is file:  even display, network

Not like UNIX  root directory, Plan 9 has execution environment
every execution environment has it own user space, (a little bit like hydra. content in particular name space)

Analogy -> your house, my house

#### UNION operate:
- unix
  - mount some file system  glue on others it together
- Plan 9
  - do not care what resource under this file. has union directory to one and glue all together

#### storage:
- plan 9 makes more file, the hardware company making more capacity. No worries here.
- backup system -> like time machine

> Netapp

## utf-8
