#本例的持久化存储采用的是hostpath模式，把Prometheus/alertmanager和grafana的数据映射到NAS（data目录是挂载的nas目录）,其中prometheus也可以映射到宿主机本地磁盘以提高数据读写IO性能。


#创建后端存储目录mkdir /data/xingyun/pub/data/{grafana,prometheus,alertmanager} -p
