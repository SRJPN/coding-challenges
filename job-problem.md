# Find minimum time to finish all jobs with given constraints
*Difficulty Level : Hard*

Given an array of jobs with different time requirements. There are K identical assignees available and we are also given how much time an assignee takes to do one unit of the job. Find the minimum time to finish all jobs with following constraints.
 

An assignee can be assigned only contiguous jobs. For example, an assignee cannot be assigned jobs 1 and 3, but not 2.
Two assignees cannot share (or co-assigned) a job, i.e., a job cannot be partially assigned to one assignee and partially to other.

*Input :*
``` text

K:     Number of assignees available.
T:     Time taken by an assignee to finish one unit 
       of job
job[]: An array that represents time requirements of 
       different jobs.

```

*Examples:*

``` text 
Input:  k = 2, T = 5, job[] = {4, 5, 10}
Output: 50

The minimum time required to finish all the jobs is 50.
There are 2 assignees available. We get this time by 
assigning {4, 5} to first assignee and {10} to second 
assignee.


Input:  k = 4, T = 5, job[] = {10, 7, 8, 12, 6, 8}
Output: 75

We get this time by assigning {10} {7, 8} {12} and {6, 8}
```