installation of npm 
```
$sudo apt update -y
$mkdir todo
$cd todo
$git clone https://github.com/zelar-soft-todoapp/todo.git
$sudo apt install npm
$npm init -y
$npm install
$npm start
```
creating service file
```
#cd /etc/systemd/system
#vi todo.service

[Unit]
Description=todo Service
[Service]
User=todo
Environment=REDIS_HOST=172.31.48.48
Environment=AUTH_API_PORT=8080
ExecStart=/bin/node /home/todo/final/todo/server.js
SyslogIdentifier=todo
[Install]
WantedBy=multi-user.target
```
start service 

```
# systemctl daemon-reload
# systemctl start todo
# systemctl status todo
```





![Screenshot (259)](https://user-images.githubusercontent.com/82602260/116847233-bff22c80-ac07-11eb-83a5-06748c88e631.png)


![Screenshot (261)](https://user-images.githubusercontent.com/82602260/116846946-1d39ae00-ac07-11eb-9a12-86d12263a082.png)


![Screenshot (263)](https://user-images.githubusercontent.com/82602260/116847041-625de000-ac07-11eb-8b69-37070fe574c8.png)



