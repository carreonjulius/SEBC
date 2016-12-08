```
{
  "timestamp" : "2016-12-08T09:19:34.491Z",
  "clusters" : [ {
    "name" : "carreonjulius",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "612368384"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "612368384"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "3571397427"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "601"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-3-225.ap-southeast-1.compute.internal"
        }, {
          "name" : "hive_metastore_database_name",
          "value" : "hive"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "hive_passw0rd"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-0b61ada6fa4146229e04b6f1e268073b",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-f43eff53"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-4d91cd34a867cd9663eb6d34c760e8d5",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-fb3eff5c"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-5502241cda45c3983c4425031c855eee",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-f93eff5e"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-8ddafd4f9ba52289d190153ce339eb5e",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-f83eff5f"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-900493c596737dac1a5ec14f3a175732",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-fa3eff5d"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-0b61ada6fa4146229e04b6f1e268073b",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "i-f43eff53"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6z8rnxmnvpxcz2akr743tjdv1"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-0b61ada6fa4146229e04b6f1e268073b",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "i-f43eff53"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e430z59e9auk66ldol83nv46o"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "612368384"
          } ]
        } ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-0b61ada6fa4146229e04b6f1e268073b",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-f43eff53"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3fxohgeekhqbuufk532d9o1m5"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-4d91cd34a867cd9663eb6d34c760e8d5",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-fb3eff5c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9w3logz2i33eqpdxssbuxlsks"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-900493c596737dac1a5ec14f3a175732",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-fa3eff5d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c8ww40anrysda1ctpdxh5ty7e"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-3-225.ap-southeast-1.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "hue_passw0rd"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-NAMENODE-0b61ada6fa4146229e04b6f1e268073b"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-0b61ada6fa4146229e04b6f1e268073b",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "i-f43eff53"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9bm8yfmz4wsopja8yab8anhx6"
          }, {
            "name" : "secret_key",
            "value" : "bydxW9KnOZBlOdcNzlKIlAMu8FAOJt"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-3-225.ap-southeast-1.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "oozie_passw0rd"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "612368384"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-0b61ada6fa4146229e04b6f1e268073b",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "i-f43eff53"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5x1b2uwmlq59tgc7dd4jmgsbe"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "8"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "2"
          } ]
        }, {
          "roleType" : "JOBHISTORY",
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "612368384"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "nodemanager_local_data_directories_free_space_absolute_thresholds",
            "value" : "{\"warning\":2147483648,\"critical\":1073741824}"
          }, {
            "name" : "nodemanager_log_directories_free_space_absolute_thresholds",
            "value" : "{\"warning\":2147483648,\"critical\":1073741824}"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/mnt/disk3/yarn/nm,/mnt/disk4/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs,/mnt/disk3/yarn/container-logs,/mnt/disk4/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "4"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "3825"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "resource_manager_java_heapsize",
            "value" : "612368384"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "5250"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "90"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "sLZA5vVCzjpHYNEwG6zJ3taF5JrabG"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-0b61ada6fa4146229e04b6f1e268073b",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "i-f43eff53"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1kvgmep5mi0szhmn1fa4z7nd1"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-4d91cd34a867cd9663eb6d34c760e8d5",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-fb3eff5c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1iwhxsbatgbtgu7zx3tm148n9"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-5502241cda45c3983c4425031c855eee",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-f93eff5e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "58t2l6gq9ca1bevfib2lno2h1"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-8ddafd4f9ba52289d190153ce339eb5e",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-f83eff5f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8i504llg08oazpmpkn9ezi1w8"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-900493c596737dac1a5ec14f3a175732",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-fa3eff5d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cmtpo1dmgfxez0qtjuc0ln4dx"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-0b61ada6fa4146229e04b6f1e268073b",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "i-f43eff53"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "83"
          }, {
            "name" : "role_jceks_password",
            "value" : "63k2rqi35nf1vqpg9yo5jjoog"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "BALANCER",
          "items" : [ {
            "name" : "balancer_java_heapsize",
            "value" : "612368384"
          } ]
        }, {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_data_directories_free_space_absolute_thresholds",
            "value" : "{\"warning\":2147483648,\"critical\":1073741824}"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/mnt/disk3/dfs/dn,/mnt/disk4/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "1073741824"
          }, {
            "name" : "dfs_datanode_failed_volumes_tolerated",
            "value" : "1"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "612368384"
          }, {
            "name" : "role_config_suppression_namenode_java_heapsize_minimum_validator",
            "value" : "true"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "612368384"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "0ORY46CyAy7Jf6g9vrnczZ9MeetP1A"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "S5aTQMFDBOcdpS0xidTRK6OCjkLhfv"
        }, {
          "name" : "hdfs_canary_health_enabled",
          "value" : "false"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "ffd3b4cBck9W3fmBXJrzOXwNLAZcRJ"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "10"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-0b61ada6fa4146229e04b6f1e268073b",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "i-f43eff53"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-4d91cd34a867cd9663eb6d34c760e8d5",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-fb3eff5c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "97uvb06ws82tk66i27dal3031"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-5502241cda45c3983c4425031c855eee",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-f93eff5e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "76vcp0h0jj9p7sbjt3dvczo2x"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-8ddafd4f9ba52289d190153ce339eb5e",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-f83eff5f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bfmz72y94cudexz8i2y8jp750"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-900493c596737dac1a5ec14f3a175732",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-fa3eff5d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "53ik9a8bwkm4rwa4rdk8kaivr"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-0b61ada6fa4146229e04b6f1e268073b",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-f43eff53"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8nvmotpefv4vydw6hoaua7dsg"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-4d91cd34a867cd9663eb6d34c760e8d5",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-fb3eff5c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4o873y8xlr4pbv8bx7z9r3ekr"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-0b61ada6fa4146229e04b6f1e268073b",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-f43eff53"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c7io3nzwlxf5yonml36hxwfjt"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-8ddafd4f9ba52289d190153ce339eb5e",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-f83eff5f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6j09x234bp1sm0tabmgb4vv7k"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-900493c596737dac1a5ec14f3a175732",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-fa3eff5d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "b80cdk2eukd970mmdoo99e5th"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-0b61ada6fa4146229e04b6f1e268073b",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-f43eff53"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "85"
          }, {
            "name" : "role_jceks_password",
            "value" : "1lvod8varack72mkxc5c6uhi4"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-4d91cd34a867cd9663eb6d34c760e8d5",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-fb3eff5c"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "91"
          }, {
            "name" : "role_jceks_password",
            "value" : "64b8jf70xuss0j0xqi9vdk3cv"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "i-f43eff53",
    "ipAddress" : "172.31.3.225",
    "hostname" : "ip-172-31-3-225.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-fb3eff5c",
    "ipAddress" : "172.31.3.226",
    "hostname" : "ip-172-31-3-226.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-fa3eff5d",
    "ipAddress" : "172.31.3.227",
    "hostname" : "ip-172-31-3-227.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-f93eff5e",
    "ipAddress" : "172.31.3.228",
    "hostname" : "ip-172-31-3-228.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-f83eff5f",
    "ipAddress" : "172.31.3.229",
    "hostname" : "ip-172-31-3-229.ap-southeast-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-0b61ada6fa4146229e04b6f1e268073b",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "0e6bddc0b668b276db01389579b2b361bb267c268a330f892ea6201f85e728b7",
    "pwSalt" : 7074271560417867073,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-0b61ada6fa4146229e04b6f1e268073b",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "54cd33493d5e7454da654af7962e97f2dfa12b815485638a036cc2ae9f449d8a",
    "pwSalt" : -5445889368342486271,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-0b61ada6fa4146229e04b6f1e268073b",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "aceefeaeb208f2168adb04a1cc580439dc048c8ec8b201c0b05a3e0dbbd1af23",
    "pwSalt" : 801523699317333377,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-0b61ada6fa4146229e04b6f1e268073b",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "27eaec8694b1bd2066a2692946ce15b9824395dcab0cf22c5cb965b3771e3113",
    "pwSalt" : -8762496056601714373,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "bd235563e249779d1f8ef643e7d094ab9512a85629b72f13e2b184cdb94a2cf6",
    "pwSalt" : -1556625240799734714,
    "pwLogin" : true
  }, {
    "name" : "carreonjulius",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "bbb8647196384ab6e07e51e69b3dde0f58b77efe0d22fc7e35a7e8ab8222874b",
    "pwSalt" : 5854426285087025767,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "f3fcf7a55295496ff140d4b237eaca2d3623d98b574e1110d0a07295ff6321a7",
    "pwSalt" : -7879919193156183788,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.9.0",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20161006-1801",
    "gitHash" : "898a5e032c080e18833dfc58180761f6ef2ea351",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "ACTIVITYMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "536870912"
        } ]
      }, {
        "roleType" : "EVENTSERVER",
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "612368384"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "536870912"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "805306368"
        } ]
      }, {
        "roleType" : "NAVIGATOR",
        "items" : [ {
          "name" : "navigator_heapsize",
          "value" : "536870912"
        } ]
      }, {
        "roleType" : "NAVIGATORMETASERVER",
        "items" : [ {
          "name" : "navigator_heapsize",
          "value" : "536870912"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-3-225.ap-southeast-1.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "rman_passw0rd"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "612368384"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "536870912"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "805306368"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-0b61ada6fa4146229e04b6f1e268073b",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "i-f43eff53"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "ck87uv8ndugz1c4z3mvpemp04"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-0b61ada6fa4146229e04b6f1e268073b",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "i-f43eff53"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "f8j5ho13a8qxypg9eqxq56xu"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-0b61ada6fa4146229e04b6f1e268073b",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "i-f43eff53"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "7tpeprp01s6k8rc9w8pf1yh41"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-0b61ada6fa4146229e04b6f1e268073b",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "i-f43eff53"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "4dy8i0dwpmxrs8e9h7f2lt2lm"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-0b61ada6fa4146229e04b6f1e268073b",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "i-f43eff53"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "esuv00cz3r93mdhls95k3d4ep"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/27/2012 10:10"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/,http://ip-172-31-3-225:80/cdh5.8.2"
    } ]
  }
}
```