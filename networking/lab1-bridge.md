# How to create a Bridge network

## How to create a bridge network called "net1"

```
$docker network create -d bridge net1
```

## How to create a bridge network "net2"

```
$docker network create -d bridge net2
```

## How to inspect IP Address of net1 bridge?

```
$ docker network inspect --format='{{json .IPAM.Config}}'  net1
[{"Subnet":"172.19.0.0/16","Gateway":"172.19.0.1"}]
```

## How to inspect IP address of net2 bridge network?

```
$ docker network inspect --format='{{json .IPAM.Config}}'  net2
[{"Subnet":"172.20.0.0/16","Gateway":"172.20.0.1"}]
```
