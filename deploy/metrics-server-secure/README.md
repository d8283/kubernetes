#使用安全证书访问方式，要先把证书导入secret，挂载到/cert目录下

#kubectl create secret generic metrics-server-certs --from-file=/etc/kubernetes/ssl/metrics-proxy.crt --from-file=/etc/kubernetes/ssl/metrics-proxy.key -n kube-system
