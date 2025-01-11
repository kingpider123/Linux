```
1. yum install epel-release  

2. yum install snapd

3. systemctl enable --now snapd.socket

4. snap install ngrok  #

5. wget https://bin.equinox.io/c/bNyj1mQVY4c/ngrok-v3-stable-linux-amd64.tgz --no-check-certificate

6. tar xvfz ngrok-v3-stable-linux-amd64.tgz

7. ./ngrok config add-authtoken 2Fc3eFFyuuBla5103xkmrD9Zdu4_6JWnRE5ZgPx5Gi6ehP3V6

8. ./ngrok http 80
```