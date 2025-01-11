Must use Bridged Network, connect to your phone's Hot Spot, and get ipv6 address
```
1. Go to dynv6.com register a domain name

2. yum install epel-release mod_ssl

3. yum install certbot

4. certbot certonly --webroot -w /var/www/html -d domain_name --email user@gmail.com

5. Type Y and N in this order.

6. Congratulations mean you have succeeded.

7. gedit /etc/httpd/conf.d/ssl.conf

8. SSLCertificateFile /etc/letenscrypt/live/yourdomainname/cert.perm (Under SSLCertificateFile /etc/pki/tls/certs/localhost.crt )

9. SSLCertificateKeyFile /etc/letenscrypt/live/yourdomainname/priv.key (Under SSLCertificateKeyFile /etc/pki/tls/private/localhost.key)

10. SSLCACertificateFile /etc/letenscrypt/live/yourdomainname/fullchain.pem (Under SSLCACertificateFile /etc/pki/tls/certs/ca-bundle.crt)

11. systemctl restart httpd

12. Go to Google and type https://yourdomainname
```