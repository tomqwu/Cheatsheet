# Cluster VM
## config host-only in adaptor 2 
```
192.168.56.1
255.255.255.0
```

## config VM /etc/network/interfaces
```
auto eth1
iface eth1 inet static
address 192.168.56.101
netmask 255.255.255.0
network 192.168.56.0
broadcast 192.168.56.255
```

## add /etc/hosts
```
192.168.56.101    myserver1
192.168.56.102    myserver2
```

## restart eth1 or reboot
```
ifdown eth1
ifup eth1
```



# Centos minimal running on Virtualbox
```
vi /etc/sysconfig/network-scripts/ifcfg-eth0
```
## change to 
```
NM_CONTROLLED="NO"
ONBOOT="YES"
BOOTPROTO="dhcp"
```
