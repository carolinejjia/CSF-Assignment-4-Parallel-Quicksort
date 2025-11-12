CONTRIBUTIONS

Senuka: task 3 and 4
Caroline: task 1, 2, 4

REPORT
As the parallel threshold decreases, each array is divided into smaller partitions,
resulting in more recursive calls running in parallel across multiple CPU cores.
This improves performance at moderate thresholds as the workload is spread out more.
However, at lower thresholds, the performance begins to worsen because the overhead 
created by each fork() takes time and system resources that cancel out the benefit of 
parallelism. 

Looking at the data, the runtime decreases from the largest threshold of 2097152 and a 
runtime of 0.839s and reaches its lowest value at a threshold of 65536, with 0.182s.
The lowest threshold of 16384 has a runtime of 0.195s, slightly higher than the next 
highest threshold, signifying that the overhead created by the additional fork() calls
outweighs the efficiency benefit of additional parallelism.

Test run with threshold 2097152
real    0m0.839s

Test run with threshold 1048576
real    0m0.405s

Test run with threshold 524288
real    0m0.278s

Test run with threshold 262144
real    0m0.222s

Test run with threshold 131072
real    0m0.196s

Test run with threshold 65536
real    0m0.182s

Test run with threshold 32768
real    0m0.188s

Test run with threshold 16384
real    0m0.195s

