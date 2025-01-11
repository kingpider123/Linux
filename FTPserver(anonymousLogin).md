```
1. sudo yum install ftp

2. sudo yum install vsftpd

3. gedit /etc/vsftpd/vsftpd.conf
> set `anonymous enable = YES`

4. systemctl restart vsftpd

5. Using WinSCP and login with anonymous check
```