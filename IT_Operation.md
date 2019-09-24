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



**Advanced Network Techs**

- InfiniBand
- RDMA
- Spot Instance

