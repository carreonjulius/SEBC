# <center>System Configuration Checks 
# <center> 

1. Check vm.swappiness on all your nodes. Set the value to 1 if necessary                   <br />
<code>                                                                                      <br />
[root@ip-172-31-3-225 ~]# cat /proc/sys/vm/swappiness                                       <br />
1                                                                                           <br />
</code>                                                                                     <br />
2. Show the mount attributes of all volumes                                                 <br />
<code>                                                                                      <br />
	[root@ip-172-31-3-225 ~]# cat /etc/fstab                                                <br />
	LABEL=centos_root               /        ext4      defaults         0 0                 <br />
	devpts     /dev/pts  devpts  gid=5,mode=620   0 0                                       <br />
	tmpfs      /dev/shm  tmpfs   defaults         0 0                                       <br />
	proc       /proc     proc    defaults         0 0                                       <br />
	sysfs      /sys      sysfs   defaults         0 0                                       <br />
	/dev/xvdf /mnt/disk1 ext4 defaults 0 0                                                  <br />
	/dev/xvdg /mnt/disk2 ext4 defaults 0 0                                                  <br />
</code>                                                                                     <br />
3. Show the reserve space of any non-root, ext-based volumes                                <br />
<code>                                                                                      <br />
	[root@ip-172-31-3-225 ~]# df -Th                                                        <br />
	Filesystem     Type   Size  Used Avail Use% Mounted on                                  <br />
	/dev/xvde      ext4    30G   18G   11G  64% /                                           <br />
	tmpfs          tmpfs  7.4G     0  7.4G   0% /dev/shm                                    <br />
	/dev/xvdf      ext4   9.9G  151M  9.2G   2% /mnt/disk1                                  <br />
	/dev/xvdg      ext4   9.9G  151M  9.2G   2% /mnt/disk2                                  <br />
	cm_processes   tmpfs  7.4G  5.0M  7.4G   1% /var/run/cloudera-scm-agent/process         <br />
</code>                                                                                     <br />
4. Show that transparent hugepages is disabled                                              <br />
<code>                                                                                      <br />
	[root@ip-172-31-3-225 ~]# grep -i HugePages_Total /proc/meminfo                         <br />
	HugePages_Total:       0                                                                <br />
	[root@ip-172-31-3-225 ~]# cat /proc/sys/vm/nr_hugepages                                 <br />
	0                                                                                       <br />
	[root@ip-172-31-3-225 ~]# grep AnonHugePages /proc/meminfo                              <br />
	AnonHugePages:         0 kB                                                             <br />
</code>                                                                                     <br />
5. Report the network interface attributes                                                  <br />
<code>                                                                                      <br />
	[root@ip-172-31-3-225 ~]# ifconfig                                                      <br />
	eth0      Link encap:Ethernet  HWaddr 02:13:7C:D6:C9:71                                 <br />
          inet addr:172.31.3.225  Bcast:172.31.15.255  Mask:255.255.240.0                   <br />
          inet6 addr: fe80::13:7cff:fed6:c971/64 Scope:Link                                 <br />
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1                                <br />
          RX packets:97654 errors:0 dropped:0 overruns:0 frame:0                            <br />
          TX packets:69038 errors:0 dropped:0 overruns:0 carrier:0                          <br />
          collisions:0 txqueuelen:1000                                                      <br />
          RX bytes:21023044 (20.0 MiB)  TX bytes:16050158 (15.3 MiB)                        <br />
          Interrupt:22                                                                      <br />
                                                                                            <br />
	lo        Link encap:Local Loopback                                                     <br />
          inet addr:127.0.0.1  Mask:255.0.0.0                                               <br />
          inet6 addr: ::1/128 Scope:Host                                                    <br />
          UP LOOPBACK RUNNING  MTU:16436  Metric:1                                          <br />
          RX packets:403004 errors:0 dropped:0 overruns:0 frame:0                           <br />
          TX packets:403004 errors:0 dropped:0 overruns:0 carrier:0                         <br />
          collisions:0 txqueuelen:0                                                         <br />
          RX bytes:682427062 (650.8 MiB)  TX bytes:682427062 (650.8 MiB)                    <br />
</code>                                                                                     <br />
6. Show forward and reverse host lookups using getent and nslookup                          <br />
<code>                                                                                      <br />
	getent                                                                                  <br />
	172.31.3.225    ip-172-31-3-225.ap-southeast-1.compute.internal                         <br />
	172.31.3.226    ip-172-31-3-226.ap-southeast-1.compute.internal                         <br />
	172.31.3.227    ip-172-31-3-227.ap-southeast-1.compute.internal                         <br />
	172.31.3.228    ip-172-31-3-228.ap-southeast-1.compute.internal                         <br />
	172.31.3.229    ip-172-31-3-229.ap-southeast-1.compute.internal                         <br />
	                                                                                        <br />
	nslookup                                                                                <br />
	Server:         172.31.0.2                                                              <br />
	Address:        172.31.0.2#53                                                           <br />
                                                                                            <br />
	Non-authoritative answer:                                                               <br />
	Name:   ip-172-31-3-225.ap-southeast-1.compute.internal                                 <br />
	Address: 172.31.3.225                                                                   <br />
                                                                                            <br />
	Server:         172.31.0.2                                                              <br />
	Address:        172.31.0.2#53                                                           <br />
                                                                                            <br />
	Non-authoritative answer:                                                               <br />
	Name:   ip-172-31-3-226.ap-southeast-1.compute.internal                                 <br />
	Address: 172.31.3.226                                                                   <br />
                                                                                            <br />
	Server:         172.31.0.2                                                              <br />
	Address:        172.31.0.2#53                                                           <br />
                                                                                            <br />
	Non-authoritative answer:                                                               <br />
	Name:   ip-172-31-3-227.ap-southeast-1.compute.internal                                 <br />
	Address: 172.31.3.227                                                                   <br />
                                                                                            <br />
	Server:         172.31.0.2                                                              <br />
	Address:        172.31.0.2#53                                                           <br />
                                                                                            <br />
	Non-authoritative answer:                                                               <br />
	Name:   ip-172-31-3-228.ap-southeast-1.compute.internal                                 <br />
	Address: 172.31.3.228                                                                   <br />
                                                                                            <br />
	Server:         172.31.0.2                                                              <br />
	Address:        172.31.0.2#53                                                           <br />
                                                                                            <br />
	Non-authoritative answer:                                                               <br />
	Name:   ip-172-31-3-229.ap-southeast-1.compute.internal                                 <br />
	Address: 172.31.3.229                                                                   <br />
</code>                                                                                     <br />
7. Verify the nscd service is running                                                       <br />
<code>                                                                                      <br />
	[root@ip-172-31-3-225 ~]# service ntpd status                                           <br />
	ntpd (pid  7054) is running...                                                          <br />
</code>                                                                                     <br />
8. Verify the ntpd service is running                                                       <br />
<code>                                                                                      <br />
	[root@ip-172-31-3-225 ~]# service ntpd status                                           <br />
	ntpd (pid  7054) is running...                                                          <br />
</code>                                                                                     <br />
</code>