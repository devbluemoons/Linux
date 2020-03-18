### CentOS 7.x
  
###### register service
```sh
# create service file
vi /usr/lib/systemd/system/myApp.service

# service file Start Point
[Unit]
Description=myApp
After=syslog.target

[Service]
User=root
Group=root
WorkingDirectory=/opt/projectPath

ExecStart=/usr/bin/java -jar /opt/projectPath/myApp-0.0.1-SNAPSHOT.jar
SuccessExitStatus=143

[Install]
WantedBy=multi-user.target
# service file End Point

# reload systemctl
systemctl daemon-reload

# auto reload when system restart
systemctl enable myApp.service

# start, stop, status
systemctl start myApp
systemctl stop myApp
systemctl status myApp
```
[참조] https://nalpari0628.tistory.com/entry/CentOS%EC%97%90-SpringBoot-jar%ED%8C%8C%EC%9D%BC-%EC%84%9C%EB%B9%84%EC%8A%A4-%EB%93%B1%EB%A1%9D%ED%95%98%EA%B8%B0
