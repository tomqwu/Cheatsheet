# Share Host VPN with Guest
## Note that uuid
```
$ VBoxManage list vms 
```
## Now try to ping that VPN domain name
```
$ VBoxManage modifyvm <uuid here> --natdnshostresolver1 on
```
