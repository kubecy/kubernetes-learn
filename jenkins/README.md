# Jenkins部署

deploy目录中的配置文件，用于将Jenkins部署于Kubernetes集群之上，它依赖于：

1. Kubernetes集群上部署有基于nfs-csi的存储服务，且创建了名称为nfs-csi的StorageClass资源。
2. Kubernetes集群上部署有Ingress Nginx Controller。

~~~shell
root@A-YYYPT-K99-M01 /gitee/kubernetes-learn/jenkins/deploy:~ # tree
.
├── 01-namespace-jenkins.yaml
├── 02-pvc-jenkins.yaml
├── 03-rbac-jenkins.yaml
├── 04-deploy-jenkins.yaml
├── 05-service-jenkins.yaml
├── 06-pvc-maven-cache.yaml
└── 07-ingress-jenkins.yaml
~~~



### 部署命令

~~~shell
kubectl apply -f deploy/
~~~







