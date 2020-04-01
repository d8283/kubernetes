#部署前先保证远程存储服务已经安装（本例是nfs，使用pv）
#部署应用时可以使用kubectl apply -f .来整体执行

#删除应用时不能使用kubectl delete -f .来整体删除，因为StatefulSet属性不像PersistentVolumeClaim属性能删除pvc，pvc不删除就导致pv也不能删除，会一直卡在哪里。
#所以要先删除prometheus的pvc，kubectl delete pvc prometheus-data-prometheus-0 -n kube-system
