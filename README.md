This repository is copy of oozie-examples.tar.gz present with standard Hortonworks installation of oozie. Usually located at /usr/hdp/current/oozie-server/doc/oozie-examples.tar.gz

Modify job.properties as per your cluster. 

For nameNode replace the value with dfs.namenode.rpc-address in hdfs-site.xml, in case of Namenode HA use the value of dfs.internal.nameservices

For jobTracker replace the value with yarn.resourcemanager.address in yarn-site.xml, in case of Resourcemanager HA use the value of yarn.resourcemanager.address.rm1 or yarn.resourcemanager.address.rm2

Replcace hive-site.xml with your cluster's hive-site ususally present at /etc/hive/conf/hive-site.xml

Copy examples directory to hdfs:

```hdfs dfs -put examples .```

Run using below command:

```oozie job -oozie http://<oozie-host>:<oozie-port>/oozie/ -config <local path of job.properties> -run```
