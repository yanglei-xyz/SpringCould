# SpringCloud学习笔记
> SpringCloud版本：Finchley.M2  
> SpringBoot版本：2.0.0.M3

## 1、eureka注册中心
+ module:eureka
+ 端口:8761
## 2、eureka-client客户端
+ module:eureka-client
+ 端口:8080
## 3、eureka-client高可用
+ module:eureka-client
+ 端口:8761、8762
+ 配置多个eureka，并设置eureka.client.server-url.defaultZone互相注册
> 高可用时，多个eureka直接会互相同步client注册信息，当一个eureka挂掉时活着的eureka会继续与client交互。
>client可以配置多个配置中心来保证一次注册到多个eureka上，防止要注册的注册中心挂掉导致注册失败。
>假如有3个eureka，可以每个eureka注册到另外两个上，达到大规模集群目的