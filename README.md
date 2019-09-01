
自动生成目录

+ maven 引入
`
<dependency>
    <groupId>com.github.houbb</groupId>
    <artifactId>markdown-toc</artifactId>
    <version>1.0.2</version>
</dependency>
`

+ 执行函数
`
AtxMarkdownToc.newInstance().genTocFile("D:\\工程\\github\\kubernetes-tools\\kubernetes常用命令.md");
`

apiVersion: v1
kind: Service
metadata:
  annotations:
    kubectl.kubernetes.io/last-applied-configuration: |
      {"apiVersion":"v1","kind":"Service","metadata":{"annotations":{},"labels":{"k8s-app":"kubernetes-dashboard","kubernetes.io/cluster-service":"true"},"name":"kubernetes-dashboard","namespace":"kube-system"},"spec":{"ports":[{"port":443,"targetPort":8443}],"selector":{"k8s-app":"kubernetes-dashboard"}}}
  creationTimestamp: "2019-08-30T13:37:44Z"
  labels:
    k8s-app: kubernetes-dashboard
    kubernetes.io/cluster-service: "true"
  name: kubernetes-dashboard
  namespace: kube-system
  resourceVersion: "373283"
  selfLink: /api/v1/namespaces/kube-system/services/kubernetes-dashboard
  uid: 12afc48a-1c2d-4ac9-a203-ad2db4ae34f5
spec:
  clusterIP: 10.233.24.20
  externalTrafficPolicy: Cluster
  ports:
  - nodePort: 32158
    port: 443
    protocol: TCP
    targetPort: 8443
  selector:
    k8s-app: kubernetes-dashboard
  sessionAffinity: None
  type: NodePort
status:
  loadBalancer: {}

  
 kind: ClusterRoleBinding
apiVersion: rbac.authorization.k8s.io/v1beta1
metadata:
  name: kubernetes-dashboard
subjects:
  - kind: ServiceAccount
    name: kubernetes-dashboard
    namespace: kube-system
roleRef:
  kind: ClusterRole
  name: cluster-admin
  apiGroup: rbac.authorization.k8s.io