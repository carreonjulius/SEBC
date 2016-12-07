# <center>System Configuration Checks 
# <center> 

1. Check vm.swappiness on all your nodes. Set the value to 1 if necessary
`[root@ip-172-31-3-225 ~]# cat /proc/sys/vm/swappiness`
`1`

2. Show the mount attributes of all volumes
<code>
	`[root@ip-172-31-3-225 ~]# cat /etc/fstab`
	`LABEL=centos_root               /        ext4      defaults         0 0`
	`devpts     /dev/pts  devpts  gid=5,mode=620   0 0`
	`tmpfs      /dev/shm  tmpfs   defaults         0 0`
	`proc       /proc     proc    defaults         0 0`
	`sysfs      /sys      sysfs   defaults         0 0`
	`/dev/xvdf /mnt/disk1 ext4 defaults 0 0`
	`/dev/xvdg /mnt/disk2 ext4 defaults 0 0`
</code>
3. Show the reserve space of any non-root, ext-based volumes
	`[root@ip-172-31-3-225 ~]# df -Th`
	`Filesystem     Type   Size  Used Avail Use% Mounted on`
	`/dev/xvde      ext4    30G   18G   11G  64% /`
	`tmpfs          tmpfs  7.4G     0  7.4G   0% /dev/shm`
	`/dev/xvdf      ext4   9.9G  151M  9.2G   2% /mnt/disk1`
	`/dev/xvdg      ext4   9.9G  151M  9.2G   2% /mnt/disk2`
	`cm_processes   tmpfs  7.4G  5.0M  7.4G   1% /var/run/cloudera-scm-agent/process`

4. Show that transparent hugepages is disabled
	`[root@ip-172-31-3-225 ~]# grep -i HugePages_Total /proc/meminfo`
	`HugePages_Total:       0`
	`[root@ip-172-31-3-225 ~]# cat /proc/sys/vm/nr_hugepages`
	`0`
	`[root@ip-172-31-3-225 ~]# grep AnonHugePages /proc/meminfo`
	`AnonHugePages:         0 kB`

5. Report the network interface attributes
	`[root@ip-172-31-3-225 ~]# ifconfig`
	`eth0      Link encap:Ethernet  HWaddr 02:13:7C:D6:C9:71`
          `inet addr:172.31.3.225  Bcast:172.31.15.255  Mask:255.255.240.0`
          `inet6 addr: fe80::13:7cff:fed6:c971/64 Scope:Link`
          `UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1`
          `RX packets:97654 errors:0 dropped:0 overruns:0 frame:0`
          `TX packets:69038 errors:0 dropped:0 overruns:0 carrier:0`
          `collisions:0 txqueuelen:1000`
          `RX bytes:21023044 (20.0 MiB)  TX bytes:16050158 (15.3 MiB)`
          `Interrupt:22`

	`lo        Link encap:Local Loopback`
          `inet addr:127.0.0.1  Mask:255.0.0.0`
          `inet6 addr: ::1/128 Scope:Host`
          `UP LOOPBACK RUNNING  MTU:16436  Metric:1`
          `RX packets:403004 errors:0 dropped:0 overruns:0 frame:0`
          `TX packets:403004 errors:0 dropped:0 overruns:0 carrier:0`
          `collisions:0 txqueuelen:0`
          `RX bytes:682427062 (650.8 MiB)  TX bytes:682427062 (650.8 MiB)`

6. Show forward and reverse host lookups using getent and nslookup
	getent
	`172.31.3.225    ip-172-31-3-225.ap-southeast-1.compute.internal`
	`172.31.3.226    ip-172-31-3-226.ap-southeast-1.compute.internal`
	`172.31.3.227    ip-172-31-3-227.ap-southeast-1.compute.internal`
	`172.31.3.228    ip-172-31-3-228.ap-southeast-1.compute.internal`
	`172.31.3.229    ip-172-31-3-229.ap-southeast-1.compute.internal`
	
	nslookup
	`Server:         172.31.0.2`
	`Address:        172.31.0.2#53`

	`Non-authoritative answer:`
	`Name:   ip-172-31-3-225.ap-southeast-1.compute.internal`
	`Address: 172.31.3.225`

	`Server:         172.31.0.2`
	`Address:        172.31.0.2#53`

	`Non-authoritative answer:`
	`Name:   ip-172-31-3-226.ap-southeast-1.compute.internal`
	`Address: 172.31.3.226`

	`Server:         172.31.0.2`
	`Address:        172.31.0.2#53`

	`Non-authoritative answer:`
	`Name:   ip-172-31-3-227.ap-southeast-1.compute.internal`
	`Address: 172.31.3.227`

	`Server:         172.31.0.2`
	`Address:        172.31.0.2#53`

	`Non-authoritative answer:`
	`Name:   ip-172-31-3-228.ap-southeast-1.compute.internal`
	`Address: 172.31.3.228`

	`Server:         172.31.0.2`
	`Address:        172.31.0.2#53`

	`Non-authoritative answer:`
	`Name:   ip-172-31-3-229.ap-southeast-1.compute.internal`
	`Address: 172.31.3.229`

7. Verify the nscd service is running
	`[root@ip-172-31-3-225 ~]# service ntpd status`
	`ntpd (pid  7054) is running...`

8. Verify the ntpd service is running
	`[root@ip-172-31-3-225 ~]# service ntpd status`
	`ntpd (pid  7054) is running...`