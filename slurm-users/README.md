# Slurm User
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

Output shows:

1. Username
2. Number of jobs currently running
3. Number of nodes currently in use by the user
4. Number of cores currently in use by the user
5. Number of jobs pending for the user - an * indicates one or more of the jobs are array jobs
6. Number of nodes required for pending jobs to run
7. Number of cores required for pending jobs to run
8. Any specific user limits
9. Queues that are currently in use. In this case we have 4 queues compute (C), highmem (H), GPU type 1 (G), GPU type 2 (V)

The script also colours based on certain states:
* Any user with a job pending but no jobs running will be highlighted yellow
* Any user using more than 3000 cores (arbitary number) will be highlighted green
* Any user currently being limited by a 'limit' will be highlighted blue

It isn't the prettiest script, but it is effective!
