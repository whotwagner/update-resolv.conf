# update-resolv.conf

This script updates the /etc/resolv.conf using the configuration parameters that
are pushed by a openvpn-server.

# Installation

Just copy update-resolv.conf into the directory /etc/openvpn

# Configuration


```
script-security 2
up '/etc/openvpn/update-resolv.conf'
down '/etc/openvpn/update-resolv.conf'
```

# License

GPL
