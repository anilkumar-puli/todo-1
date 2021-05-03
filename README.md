$sudo apt update -y
$mkdir todo
$cd todo
$git clone https://github.com/zelar-soft-todoapp/todo.git
$sudo apt install npm
$npm init -y
$npm install
$npm start

#vi /etc/systemd/system

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

# systemctl daemon-reload
# systemctl restart todo
# systemctl status todo





![image](https://user-images.githubusercontent.com/82602260/116801193-015ddb80-ab25-11eb-8bc5-7f1fab7f845a.png)


![Screenshot (261)](https://user-images.githubusercontent.com/82602260/116846946-1d39ae00-ac07-11eb-9a12-86d12263a082.png)


![Screenshot (263)](https://user-images.githubusercontent.com/82602260/116847041-625de000-ac07-11eb-8b69-37070fe574c8.png)



