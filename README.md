This repository is copy of oozie-examples.tar.gz present with standard Hortonworks installation of oozie. Usually located at /usr/hdp/current/oozie-server/doc/oozie-examples.tar.gz

Modify job.properties files as instructed in the file itself.

Replcace hive-site.xml with your cluster's hive-site ususally present at /etc/hive/conf/hive-site.xml

Copy hive-action directory to hdfs:

hdfs dfs -put hive-action

Run using below command:

oozie job -oozie http://<oozie-host>:<oozie-port>/oozie/ -config <local path of job.properties> -run 

