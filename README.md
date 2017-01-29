# oozie

To run hive action

Replace below values in job.properties as per your cluster.

<hdfs-site/dfs.namenode.rpc-address> with value of dfs.namenode.rpc-address in /etc/hadoop/conf/hdfs-site.xml. In case of Namenode HA use value of dfs.internal.nameservices

<yarn-site/yarn.resourcemanager.address> with value of yarn.resourcemanager.address in /etc/hadoop/conf/yarn-site.xml.

Copy hive-action directory to hdfs:

hdfs dfs -put hive-action

Run using below command:

oozie job -oozie http://<oozie-host>:<oozie-port>/oozie/ -config hive-action/job.properties -run 

Here hive-action is referring to local hive-action directory.
