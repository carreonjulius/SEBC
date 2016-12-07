# <center>HDFS Lab: Test HDFS Snapshots
# <center>

- Create a precious directory in HDFS; copy the ZIP course file into it.  

	hadoop fs -mkdir /user/carreonjulius/precious
	hadoop fs -put SEBC-master.zip /user/carreonjulius/precious

- Enable snapshots for precious  

	sudo -u hdfs hdfs dfsadmin -allowSnapshot /user/carreonjulius/precious

- Create a snapshot called sebc-hdfs-test
	
	hadoop fs -createSnapshot /user/carreonjulius/precious sebc-hdfs-test

- Delete the directory

	hadoop fs -rmr /user/carreonjulius/precious  
	rmr: Failed to move to trash: hdfs://ip-172-31-3-225.ap-southeast-1.compute.internal:8020/user/carreonjulius/precious: The directory /user/carreonjulius/precious cannot be deleted since /user/carreonjulius/precious is snapshottable and already has snapshots

- Delete the ZIP file

	hadoop fs -rmr /user/carreonjulius/precious/SEBC-master.zip

- Restore the deleted file
	
	hadoop fs -cp /user/carreonjulius/precious/.snapshot/sebc-hdfs-test/SEBC-master.zip /user/carreonjulius/precious/