### check state
``` bash
curl -u wuminorb:cloudera http://ec2-35-161-229-49.us-west-2.compute.amazonaws.com:7180/api/v12/clusters/wuminorb/services/hive/
```

``` json
{

    "name": "hive",
    "type": "HIVE",
    "clusterRef": {
        "clusterName": "cluster"
    },
    "serviceUrl": "http://ip-172-31-6-110.us-west-2.compute.internal:7180/cmf/serviceRedirect/hive",
    "roleInstancesUrl": "http://ip-172-31-6-110.us-west-2.compute.internal:7180/cmf/serviceRedirect/hive/instances",
    "serviceState": "STARTED",
    "healthSummary": "GOOD",
    "healthChecks": [
        {
            "name": "HIVE_HIVEMETASTORES_HEALTHY",
            "summary": "GOOD",
            "suppressed": false
        },
        {
            "name": "HIVE_HIVESERVER2S_HEALTHY",
            "summary": "GOOD",
            "suppressed": false
        }
    ],
    "configStalenessStatus": "FRESH",
    "clientConfigStalenessStatus": "FRESH",
    "maintenanceMode": false,
    "maintenanceOwners": [ ],
    "displayName": "Hive",
    "entityStatus": "GOOD_HEALTH"

}
```

### stop hive

```
curl -u wuminorb:cloudera ec2-35-161-229-49.us-west-2.compute.amazonaws.com:7180/api/v12/clusters/wuminorb/services/hive/commands/stop/
```

``` json
{
  "id" : 812,
  "name" : "Stop",
  "startTime" : "2017-05-13T06:56:54.459Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
```

### start hive

```
curl -u wuminorb:cloudera ec2-35-161-229-49.us-west-2.compute.amazonaws.com:7180/api/v12/clusters/wuminorb/services/hive/commands/stop/
```

``` json
{
  "id" : 819,
  "name" : "Start",
  "startTime" : "2017-05-13T06:58:05.610Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
```