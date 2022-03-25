# etcd_demo

etcd_demo

## etcd 文档

[https://etcd.io/docs/](https://etcd.io/docs/)

## etcd 简介

etc 在linux系统中是配置文件目录名；etcd就是配置服务；

## etcd 作用

- 全局配置服务中心
- 分布式注册服务中心

- ...

## etcd 安装

以3.5.2 mac 为例 1.下载

```shell
wget "https://github.com/etcd-io/etcd/releases/download/v3.5.2/etcd-v3.5.2-darwin-amd64.zip"

unzip etcd-v3.5.2-darwin-amd64.zip 

cd etcd-v3.5.2-darwin-amd64
```

2.查看版本

```shell
./etcd version
```

3.运行etcd

```shell
./etcd
```

4.set key

```shell
./etcdctl put greeting "hello,etcd"
```

5.get key

```shell
./etcdctl get greeting
```

## etcd 权限控制

1.添加root角色

```shell
./etcdctl role add root
```

2.添加root用户

```shell
./etcdctl user add root 
```

3.给root用户授予root角色

```shell
./etcdctl user grant-role root root
```

4.激活auth

```shell
./etcdctl auth enable
```

5.激活auth后查询用户列表

```shell
./etcdctl --user root:(root密码)  user list 
```