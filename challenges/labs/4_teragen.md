Teragen Command
```
time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.9.0.jar teragen -Dmapred.map.tasks=8 -Ddfs.block.size=67108864 51200000 /user/raffles/tgen512m
```

Time
```
real    1m15.500s
user    0m6.219s
sys     0m0.713s
```

Number of blocks in tgen512m directory
```
Connecting to namenode via http://ip-172-31-1-105.ap-southeast-1.compute.internal:50070
FSCK started by raffles (auth:SIMPLE) from /172.31.1.105 for path /user/raffles/tgen512m at Fri Dec 09 03:30:00 UTC 2016
.........Status: HEALTHY
 Total size:    5120000000 B
 Total dirs:    1
 Total files:   9
 Total symlinks:                0
 Total blocks (validated):      80 (avg. block size 64000000 B)
 Minimally replicated blocks:   80 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          4
 Number of racks:               1
FSCK ended at Fri Dec 09 03:30:00 UTC 2016 in 7 milliseconds
```