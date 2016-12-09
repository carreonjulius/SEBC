hdfs dfs -ls /user

```
Found 6 items
drwxrwxrwx   - mapred  hadoop           0 2016-12-09 03:12 /user/history
drwxrwxr-t   - hive    hive             0 2016-12-09 03:13 /user/hive
drwxrwxr-x   - hue     hue              0 2016-12-09 03:13 /user/hue
drwxrwxr-x   - oozie   oozie            0 2016-12-09 03:13 /user/oozie
drwxr-xr-x   - orchard orchard          0 2016-12-09 03:16 /user/orchard
drwxr-xr-x   - raffles raffles          0 2016-12-09 03:16 /user/raffles
```


CM API Call
```
{
  "items" : [ {
    "hostId" : "i-5326e6f4",
    "ipAddress" : "172.31.1.105",
    "hostname" : "ip-172-31-1-105.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-1-106.ap-southeast-1.compute.internal:7180/cmf/hostRedirect/i-5326e6f4",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "i-5026e6f7",
    "ipAddress" : "172.31.1.106",
    "hostname" : "ip-172-31-1-106.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-1-106.ap-southeast-1.compute.internal:7180/cmf/hostRedirect/i-5026e6f7",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "i-5126e6f6",
    "ipAddress" : "172.31.1.107",
    "hostname" : "ip-172-31-1-107.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-1-106.ap-southeast-1.compute.internal:7180/cmf/hostRedirect/i-5126e6f6",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "i-5626e6f1",
    "ipAddress" : "172.31.1.108",
    "hostname" : "ip-172-31-1-108.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-1-106.ap-southeast-1.compute.internal:7180/cmf/hostRedirect/i-5626e6f1",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "i-5726e6f0",
    "ipAddress" : "172.31.1.109",
    "hostname" : "ip-172-31-1-109.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-1-106.ap-southeast-1.compute.internal:7180/cmf/hostRedirect/i-5726e6f0",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  } ]
}
```