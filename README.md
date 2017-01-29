# oozie-examples

To run hive action replace below values in job.properties as per your cluster.

\<hdfs-site/dfs.namenode.rpc-address> with value of dfs.namenode.rpc-address in /etc/hadoop/conf/hdfs-site.xml. In case of Namenode HA use value of dfs.internal.nameservices. Do not add port in case of using nameservice.

\<yarn-site/yarn.resourcemanager.address> with value of yarn.resourcemanager.address in /etc/hadoop/conf/yarn-site.xml.

Modify script.hql to replace \<table_name> with some existing table. You can add multiple queries.

Replcace hive-site.xml with /etc/hive/conf/hive-site.xml

Copy hive-action directory to hdfs:

hdfs dfs -put hive-action

Run using below command:

oozie job -oozie http://\<oozie-host>:\<oozie-port>/oozie/ -config hive-action/job.properties -run 

Here hive-action is referring to local hive-action directory.
