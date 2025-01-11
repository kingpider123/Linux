### Server
```
1. cd /
2. mkdir /data -p : -p 如果資料夾已經存在那就不做
3. sudo yum install nfs-utils -y
4. sudo systemctl enable rpcbind
5. sudo systemctl enable nfs
6. sudo systemctl start rpcbind
7. sudo systemctl start nfs
8. vim /etc/exports
9. /data 192.168.1.1/24 (rw,sync,no_root_squash,no_all_squash)

10. systemctl restart nfs
11. showmount -e localhost

```
### Client
```
1. cd /
2. mkdir /nfs-data -p
3. sudo yum install nfs-utils
4. sudo systemctl enable rpcbind
5. sudo systemctl start rpcbind
6. showmount -e 192.168.1.104
7. sudo mount -t nfs 192.168.1.104:/data /nfs-data
```