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


