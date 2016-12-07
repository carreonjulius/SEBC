# <center>HDFS Lab: Test HDFS performance
# <center>

**Teragen**

	time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.8.2.jar teragen -Dmapred.map.tasks=4 -Ddfs.block.size=33554432 107374182 /user/carreonjulius/teragen_result
	
	real    2m32.927s
	user    0m6.246s
	sys     0m0.735s

**Terasort**
	
	time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.8.2.jar terasort /user/carreonjulius/teragen_result /user/carreonjulius/terasort_result
	
	real    5m58.863s
	user    0m9.606s
	sys     0m1.024s