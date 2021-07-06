# slurmtools
A collection of my own slurm tools

These include various scripts which are collections of existing commands and tools, joined together with things like join and awk commands to consolidate output data to a desired output




## Slurm User
Script to show resource used and resource required by users, output looks something like the following:
```
Username    JobRun   NodeRun   CoreRun   JobPend   NodePend   CorePend   Limits   Queue 
ru2377      1        7         196       0         0          0          150      C... 
ru2910      0        0         0         2*        2*         8*                  ...V
ru8458      1        1         1         0         0          0                   C... 
ru1522      1        62        1736      1         64         64         10       C... 
ru5855      2        1         2         0         0          0                   ...V 
ru1934      1        60        1680      1         60         1680       8        C... 
ru8106      1        1         20        0         0          0                   .H.. 
ru1735      1        1         10        0         0          0                   .H.. 
ru4849      1        1         1         0         0          0                   ..G. 
```
