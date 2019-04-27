# Multiqueue Processing Experiements #

* V1. Multiprocessing vs Single process handling [Date 27 April 2019]

Matrix Multiplication Experiments using traditional method numpy vs Matrix multiplication using Multiprocessing and its benchmarks.

## Python Script Abbrevations
1. mp  --> Multiprocess
2. mq  --> Multiqueue
3. nx  --> Normal Execution

### *Single Thread Processing (Normal Execution)*

```console
root@raspberrypi:/usr/local/program/multithread# time ./nx
Dataset: [ 1  2  3  4  5  6  7  8  9 10 11 12 13 14]
Results: [          1           4          27         256        3125       46656
      823543    16777216   387420489  1410065408  1843829075  -251658240
 -1692154371 -1282129920]

real	0m0.678s
user	0m0.638s   --------------------------------->
sys	0m0.040s
root@raspberrypi:/usr/local/program/multithread#
```

### *MultiThread Processing*

```console
root@raspberrypi:/usr/local/program/multithread# time ./mq
Dataset: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14]
Result:  [1, 4, 27, 256, 3125, 46656, 823543, 16777216, 387420489, 10000000000, 285311670611, 8916100448256, 302875106592253, 11112006825558016]

real	0m0.462s
user	0m0.360s --------------------------------->
sys	0m0.036s
root@raspberrypi:/usr/local/program/multithread#
```

### Examples of Multithreading ###
```console
root@raspberrypi:/usr/local/program/multithread# ./mp
First Multi Process joe
Function process: 18210 ------------------------> Runs on a seperate thread
Main process: 12515 ----------------------------> Main program runs on the main thread
root@raspberrypi:/usr/local/program/multithread#
```

### *Appendix*

*real - time from start to finish of the call. It is the time from the moment you hit the Enter key until the moment the wget command is completed.
*user - amount of CPU time spent in user mode.
*sys - amount of CPU time spent in kernel mode.

https://docs.python.org/3.5/library/multiprocessing.html#
