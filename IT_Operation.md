## 数据中心

#### Large-scale cluster operation

- distributed
- utilization
- stability
- scalability



#### Architecture

- SPOF(Single point of failure)



A/B测试

SRE(Site Reliability Engineering)







## Network

- IP
  - v4 & v6
  - Address
- ARP
- Subnet Musk
- Router
- DNS SERVER







#### NAT(Network Address Translation)

- DNAT(Destination NAT)  内网接收外部的 TCP/IP，需要单独制定端口映射
- SNAT(Source NAT)  内网向外部发 TCP/IP ，子网默认打开SNAT

TCP包的交互基本都存在

四层负载均衡





#### NAT VS Proxy

- Proxy
  - 4th layer （通过IP地址和port做包的转发，更快一点）
    - F5,Array(hardware)
    - Nginx (用户态)
    - lvs （内核态）
    - HAProxy
  - 7th layer（根据包的头部做解析，慢一点，但是能更细粒度的控制）
    - Nginx（基于http）
    - HAProxy（基于tcp/ip）



- 4th Layer

  ​										  tcp

  A——————>Proxy——————>B



- 7th Layer

  ​		tcp								tcp

​		A——————>Proxy——————>B



​		Canary Release



##### Advanced Network Techs

- InfiniBand
- RDMA
- Spot Instance



##### CQRS(读写分离)

REST Api和数据库

数据库一般是做4th Layer

REST Api 做隔离用的是七层代理



浏览器查看某个网站的DNS之前，会先在本机查看hosts的表





www.sjtu.edu.cn->hosts->DNS->....



HBA存储网络





##### Distribute Storage

Solutions:

- GFS	SOSP  2003
- Ceph	OSDI  2006



hdfs



k8s

自动伸缩算法，冷却值



zookeeper，etcd







## 资源管理

CPU	Memory	Storage	Network	...



#### Isolation Technologies：

- Virtual Machine (一般是整数的cpu)
- Container (更好的隔离度，可以0.5个cpu) （cgroup + namespace）

#### Orientation

- Resources (Hardware)
- Application (Software)



#### K8s可做基于容器的，也可做基于虚拟机的 (资源管理的理念)



#### Workload

- Long-running Services
- Batch Jobs



#### K8s 原型	——	Borg	Omega



#### K8s



#### Centralized VS Decentralized（Distributed，Hierarchy）

Centralized	--	long-running services

Decentralized	--	high utilization



自己搭镜像库

image slim



HA VS Utilization



监控各个资源使用情况
