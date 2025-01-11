### Server
```
1. yum install python3

2. vim echo_server.py

    #!/usr/bin/env python3
    import socket

    serv = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    serv.bind(('0.0.0.0', 9000))
    serv.listen()

    while True:
        conn, addr = serv.accept()
        print('Client from', addr)

        while True:
            data = conn.recv(1024)
            if not data: break
            conn.send(data)

        conn.close()
        print('Client disconnected')

3. chmod +x echo_server.py

4. vim /etc/systemd/system/echo_server.service

5. edit systemctl config

    [Unit]
    Description=Echo Server

    [Service]
    Type=simple
    ExecStart=/opt/echo_server.py
    Restart=always

    [Install]
    WantedBy=multi-user.target

6. chmod 644 /etc/systemd/system/echo_server.service

7. systemctl daemon-reload

8. systemctl start echo_server
```
### Client
```
nc server 9000
```