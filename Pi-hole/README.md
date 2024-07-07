Updates:
``` bash
sudo apt update && sudo apt upgrade
```
Set a static IP for your server on your router with DHCP reservation. This can be done a few ways, but I simply like to go to the router's IP address on the web page.
Installation command:
``` bash
curl -sSL https://install.pi-hole.net | bash
```
Go through the Pi-Hole prompted settings to meet your needs.
You'll be provided a password, which we will want to change:
``` bash
pihole -a -p newpassword
```

OPTIONAL
#
