### Server
```
getenforce

setenforce 0

systemctl status firewalld

systemctl status sshd
```
### Client (user@mycentos8-2)
```
ssh-keygen

ssh-copy-id user@mycentos8-2

ssh user@ipaddress
```