#部署前先保证远程存储ceph服务已经安装，集群里的ceph rbd的storageclass也已经部署

#因为是使用storageclass动态创建pv，所以不能删除pvc。

#删除时不要kubectl delete -f alertmanager-pvc.yaml删除alertmanager的pvc，这样会导致下次没法把pvc和原来的pv绑定，会丢失原来的数据。

#使用kubectl delete -f statefulset.yaml删除statefulset时不会删除volumeClaimTemplates创建的pvc

#要删除volumeClaimTemplates创建的pvc需使用kubectl delete pvc/xxxxxx命令删除
