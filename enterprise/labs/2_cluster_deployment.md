```
curl -u wuminorb:cloudera http://ec2-35-161-229-49.us-west-2.compute.amazonaws.com:7180/api/v2/cm/deployment > v2deployment.json
```

``` json
{
  "timestamp" : "2017-05-12T10:36:08.340Z",
  "clusters" : [ {
    "name" : "wuminorb",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "1998585856"
          }, {
            "name" : "hive_metastore_server_max_message_size",
            "value" : "199858585"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "1983905792"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "2191681126"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "368"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-6-110.us-west-2.compute.internal"
        }, {
          "name" : "hive_metastore_database_name",
          "value" : "hive"
        }, {
          "name" : "hive_metastore_database_password",
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
        "name" : "hive-GATEWAY-599928e509f2cbf059b1b8e9767f4233",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "958566e4-ae22-4a6d-b0c6-05d112889ad5"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-8d54d81b398413f29411a85ee73b1ca9",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "c00d8938-1f44-4d1b-b3cd-8d02088b9e95"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-b15452ec6bf4ca890ebe56d4d34a0ead",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "db664ef4-6f6c-4d1d-8d84-39e50b94c908"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-c9c98ba48d1b44f2b093ef60bff9df98",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "bec2f50a-a1bb-4737-8531-7586ae095ec1"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-ea41d71377fbf06614ce96583a0cb704",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "5deaa19c-bb71-4307-b4dd-0acf1b367f9f"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-ea41d71377fbf06614ce96583a0cb704",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "5deaa19c-bb71-4307-b4dd-0acf1b367f9f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bmpjdztur9kbv2les781wdnbn"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-c9c98ba48d1b44f2b093ef60bff9df98",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "bec2f50a-a1bb-4737-8531-7586ae095ec1"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4ndvh11xt2h4ygk9ifuusfye4"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "enableSecurity",
          "value" : "true"
        } ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-599928e509f2cbf059b1b8e9767f4233",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "958566e4-ae22-4a6d-b0c6-05d112889ad5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "30652fq59pryppo73w3zm1g80"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-8d54d81b398413f29411a85ee73b1ca9",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "c00d8938-1f44-4d1b-b3cd-8d02088b9e95"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2thoufp5ak9kqa5k1icvgm77v"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-ea41d71377fbf06614ce96583a0cb704",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "5deaa19c-bb71-4307-b4dd-0acf1b367f9f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "n2snlnewkr23fca47n89btur"
          }, {
            "name" : "serverId",
            "value" : "1"
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
          "value" : "ip-172-31-6-110.us-west-2.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "hue"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-599928e509f2cbf059b1b8e9767f4233"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-c9c98ba48d1b44f2b093ef60bff9df98",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "bec2f50a-a1bb-4737-8531-7586ae095ec1"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "b1r9txreiphnuw9ta5wowb0s6"
          }, {
            "name" : "secret_key",
            "value" : "imVFpJBzLriATxUZbkji3e1dHrTEmk"
          } ]
        }
      }, {
        "name" : "hue-KT_RENEWER-c9c98ba48d1b44f2b093ef60bff9df98",
        "type" : "KT_RENEWER",
        "hostRef" : {
          "hostId" : "bec2f50a-a1bb-4737-8531-7586ae095ec1"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "arepjtoh0yfwd1shgym4s6fpz"
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
            "value" : "ip-172-31-6-110.us-west-2.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "oozie"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
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
        "name" : "oozie-OOZIE_SERVER-599928e509f2cbf059b1b8e9767f4233",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "958566e4-ae22-4a6d-b0c6-05d112889ad5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1sid1q90mybblclf1t04ltfzn"
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
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "4"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "2477"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "3051"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "4"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "Z8J8igS7fN0AdxzyMQAQxVdl8hSOrV"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-ea41d71377fbf06614ce96583a0cb704",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "5deaa19c-bb71-4307-b4dd-0acf1b367f9f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "983ln06q33h51z9g5jnlvkpxt"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-599928e509f2cbf059b1b8e9767f4233",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "958566e4-ae22-4a6d-b0c6-05d112889ad5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "eua8ook0g3h22p2x5tqkf0757"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-8d54d81b398413f29411a85ee73b1ca9",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "c00d8938-1f44-4d1b-b3cd-8d02088b9e95"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "229c6ad3ye7tw03li6evbq0ya"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-c9c98ba48d1b44f2b093ef60bff9df98",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "bec2f50a-a1bb-4737-8531-7586ae095ec1"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1o80mweqa7uabb8blcnwxx55e"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-ea41d71377fbf06614ce96583a0cb704",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "5deaa19c-bb71-4307-b4dd-0acf1b367f9f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3zid5yepfwf6pkj3diq2abnqc"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-8d54d81b398413f29411a85ee73b1ca9",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "c00d8938-1f44-4d1b-b3cd-8d02088b9e95"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "83"
          }, {
            "name" : "role_jceks_password",
            "value" : "uxww9ietbsq3naqux5uf3yaj"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_data_dir_perm",
            "value" : "700"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3157155020"
          }, {
            "name" : "dfs_datanode_http_port",
            "value" : "1006"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "2597322752"
          }, {
            "name" : "dfs_datanode_port",
            "value" : "1004"
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
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "1983905792"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_encrypt_data_transfer_algorithm",
          "value" : "AES/CTR/NoPadding"
        }, {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "vyTGwqsqmtK5EK7wKnL6pSU5f1CaVb"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "YoV4jdRgbPQ9LoGBAn5uNsw75WC71J"
        }, {
          "name" : "hadoop_security_authentication",
          "value" : "kerberos"
        }, {
          "name" : "hadoop_security_authorization",
          "value" : "true"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "AaUNTbPwnirXlVmo96fIIWEwmGQlvX"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-8d54d81b398413f29411a85ee73b1ca9",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "c00d8938-1f44-4d1b-b3cd-8d02088b9e95"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-599928e509f2cbf059b1b8e9767f4233",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "958566e4-ae22-4a6d-b0c6-05d112889ad5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5tewwb0miiq7j77ot0xdmdck1"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-8d54d81b398413f29411a85ee73b1ca9",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "c00d8938-1f44-4d1b-b3cd-8d02088b9e95"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "btdhpn11g1g6nny3l340hoexj"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-c9c98ba48d1b44f2b093ef60bff9df98",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "bec2f50a-a1bb-4737-8531-7586ae095ec1"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "a5l1a6lg6xsa2hsxdsrtdgc60"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-ea41d71377fbf06614ce96583a0cb704",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "5deaa19c-bb71-4307-b4dd-0acf1b367f9f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7sas5bp8pivkikw63drestrfn"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-b15452ec6bf4ca890ebe56d4d34a0ead",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "db664ef4-6f6c-4d1d-8d84-39e50b94c908"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9n8wehocnupmicxq4xtjhrkio"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-c9c98ba48d1b44f2b093ef60bff9df98",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "bec2f50a-a1bb-4737-8531-7586ae095ec1"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "a76cyc0kn3mjgvw7cq8zxt7si"
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-599928e509f2cbf059b1b8e9767f4233",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "958566e4-ae22-4a6d-b0c6-05d112889ad5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e0plof2hr0mwzjz3lvgwjl1x1"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-599928e509f2cbf059b1b8e9767f4233",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "958566e4-ae22-4a6d-b0c6-05d112889ad5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "40mc0zj8338yvappqyneivsnl"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-8d54d81b398413f29411a85ee73b1ca9",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "c00d8938-1f44-4d1b-b3cd-8d02088b9e95"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d2g04n0u1hvywvb9ngnac3a2i"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-ea41d71377fbf06614ce96583a0cb704",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "5deaa19c-bb71-4307-b4dd-0acf1b367f9f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2qafshg8exjgqcmisi4j6afxp"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-b15452ec6bf4ca890ebe56d4d34a0ead",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "db664ef4-6f6c-4d1d-8d84-39e50b94c908"
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
            "value" : "126bamvxntet0cx6fc0tz46yi"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-c9c98ba48d1b44f2b093ef60bff9df98",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "bec2f50a-a1bb-4737-8531-7586ae095ec1"
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
            "value" : "7sjyxa5u9xemjqaynqv4a02xc"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "db664ef4-6f6c-4d1d-8d84-39e50b94c908",
    "ipAddress" : "172.31.14.185",
    "hostname" : "ip-172-31-14-185.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "bec2f50a-a1bb-4737-8531-7586ae095ec1",
    "ipAddress" : "172.31.4.161",
    "hostname" : "ip-172-31-4-161.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "958566e4-ae22-4a6d-b0c6-05d112889ad5",
    "ipAddress" : "172.31.4.192",
    "hostname" : "ip-172-31-4-192.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "c00d8938-1f44-4d1b-b3cd-8d02088b9e95",
    "ipAddress" : "172.31.6.110",
    "hostname" : "ip-172-31-6-110.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "5deaa19c-bb71-4307-b4dd-0acf1b367f9f",
    "ipAddress" : "172.31.6.167",
    "hostname" : "ip-172-31-6-167.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-b15452ec6bf4ca890ebe56d4d34a0ead",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "c008bf9f3bc6dfd997a3b327ebe1360bf5a490694258cb119384fb7c56b2f29f",
    "pwSalt" : -644700095898530238,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-b15452ec6bf4ca890ebe56d4d34a0ead",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "213d299299e07eda284dec04cceaff70d72375ffe95e9c4d2d96099d4e0ccd43",
    "pwSalt" : -7421995489637465690,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-b15452ec6bf4ca890ebe56d4d34a0ead",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "8cb06bb50a4991eac9976387e74d60849deec22be243c4019f00d07b7121de77",
    "pwSalt" : 1471153491211119731,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-b15452ec6bf4ca890ebe56d4d34a0ead",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "b67ce17a3e050a7433fd00dfd90f15270c707cd5727ea15af09b9a3764aa46a7",
    "pwSalt" : 4689741828678573734,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "60a727aff10b9d61d8d695f84b1bac460cfe9350b50298840a4175362916aaf1",
    "pwSalt" : 2896340816631641591,
    "pwLogin" : true
  }, {
    "name" : "wuminorb",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "4a717c4d81f2f2fae347a32745265b1008d44cd8fa47e1de500ccc503627b7a9",
    "pwSalt" : 2250640243986633247,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.9.2",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170330-1814",
    "gitHash" : "822da28bff818f57fc1bfc3eafe3a550300ef1b0",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-6-110.us-west-2.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "cdh"
        }, {
          "name" : "headlamp_database_password",
          "value" : "cdh"
        }, {
          "name" : "headlamp_database_user",
          "value" : "cdh"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-b15452ec6bf4ca890ebe56d4d34a0ead",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "db664ef4-6f6c-4d1d-8d84-39e50b94c908"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "exct06ixk3lvuhwcdjrz2j1ca"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-b15452ec6bf4ca890ebe56d4d34a0ead",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "db664ef4-6f6c-4d1d-8d84-39e50b94c908"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "bojcs5oo4hzlfgm1qsl1pch6z"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-b15452ec6bf4ca890ebe56d4d34a0ead",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "db664ef4-6f6c-4d1d-8d84-39e50b94c908"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "eysza1ek8sj1va7615me20d2f"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-b15452ec6bf4ca890ebe56d4d34a0ead",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "db664ef4-6f6c-4d1d-8d84-39e50b94c908"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "bw7tfaidgam0r49f02r14ibe2"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-b15452ec6bf4ca890ebe56d4d34a0ead",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "db664ef4-6f6c-4d1d-8d84-39e50b94c908"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "965td0sx3yfwl5us2e1uavgul"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "AD_USE_SIMPLE_AUTH",
      "value" : "false"
    }, {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/22/2012 0:20"
    }, {
      "name" : "KDC_ADMIN_PASSWORD",
      "value" : "BQIAAAA6AAEAC3d1bWlub3JiLmNuAAxjbG91ZGVyYS1zY20AAAABWRT5QgEAFwAQIhjHKqM6GDyU+xhiBdYuzg=="
    }, {
      "name" : "KDC_ADMIN_USER",
      "value" : "cloudera-scm@wuminorb.cn"
    }, {
      "name" : "KDC_HOST",
      "value" : "ip-172-31-6-110.us-west-2.compute.internal"
    }, {
      "name" : "KRB_ENC_TYPES",
      "value" : "arcfour-hmac"
    }, {
      "name" : "KRB_MANAGE_KRB5_CONF",
      "value" : "true"
    }, {
      "name" : "MAX_RENEW_LIFE",
      "value" : "604800"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,http://localhost/cdh5.10/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    }, {
      "name" : "SECURITY_REALM",
      "value" : "wuminorb.cn"
    } ]
  }
}
```