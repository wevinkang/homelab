Updates and automatic security updateas:
``` bash
sudo apt update
sudo apt upgrade
sudo apt install unattended-upgrades
sudo dpkg-reconfigure --priority=low unattended-upgrades
```

Create a user with sudo priv instead of using root. However, I am securing a raspberry pi server and root login is default disabled and user with sudo priv was already configured during OS installation.

## Securing SSH
- Using publickey authentication and then requiring all password authentications to use 2FA/MFA.
- Configuring sshd_config settings securely

## Install UFW
- Deny all default, inbound, outound, forwarding
- Add allow rules for functionality

## Install PSAD 
- IDS/IPS
- Edit ufw files to log so PSAD can analyze

## Install Fail2Ban for app intrusion detection/prevention
- For now, mainly watching sshd

## Install AIDE for file integrity monitoring

## Configure email alerts from gmail account
WIP
