```
 yum install samba samba-client samba-common -y

 1. cd /
 2. mkdir test_samba  
 3. chown nobody ./test_samba/  
 4. chmod 777 ./test_samba/  
 5. ll ./test_samba/ -d  

 6. vim /etc/samba/smb.conf

 [test]
        comment = for test  
        path = /test_samba  
        read only = no  
        guest ok = yes  
        browseable = yes  

 7. testparm
 8. sudo systemctl start smb
 9. sudo netstat -tunlp | grep smb 
 10. sudo smbpasswd -a user 
```