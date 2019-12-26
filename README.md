# update-resolv.conf

This script updates the /etc/resolv.conf using the configuration parameters that
are pushed by a openvpn-server. It is a modified version of the script update-resolv-conf
that ships with openvpn.

# Installation

Just copy update-resolv.conf into the directory /etc/openvpn and modify the permissions.

# Configuration


```
script-security 2
up '/etc/openvpn/update-resolv.conf'
down '/etc/openvpn/update-resolv.conf'
```

# Prevent updating the resolv.conf

Some mechanism like dhcp-clients might modify the resolv.conf. To prevent this it is possible to change the variable "IMMUTEABLE" to 1. This will simply call: 
```
chattr +i /etc/resolv.conf
```

The down-parameter will execute:
```
chattr -i /etc/resolv.conf
```


**Be aware that this file will be immuteable if openvpn isn't shut down properly.**
# License

GPL
