#本例的持久化存储采用的是hostpath模式，把Prometheus/alertmanager和grafana的数据映射到NAS（data目录是挂载的nas目录）,其中prometheus也可以映射到宿主机本地磁盘以提高数据读写IO性能。


#创建后端存储目录mkdir /data/xingyun/pub/storage/{grafana,prometheus,alertmanager} -p

#prometheus.yaml里修改要监控的主机IP地址

#grafana导入3个模板

#①Node Exporter for Prometheus Dashboard CN（8919）主机资源监控（直接加载下载的0530版本json）

#②Kubernetes Deployment Statefulset Daemonset metrics（8588）Pod资源监控

#③Kubernetes cluster monitoring（315）微服务资源负载排行
