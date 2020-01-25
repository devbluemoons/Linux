### linux self-study
  
###### [check version]
```sh
uname -a
#OR
cat /etc/issue
```
  
###### [access root authority]
```sh
sudo su
#OR
su - root
#and then type password
```
  
###### [empower root authority]
```sh
1. sudo su
2. vi /etc/sudoers

3. [일반계정명] All=(ALL:ALL) ALL
# ex) pi All=(ALL:ALL) ALL
# this file is set a option "readonly"
# we must save to use this command ":wq!" <-- !important

4. vi /etc/passwd
5. [일반계정명]:x:0(uid):0(gid)(...) 
# ex) pi:x:0:0(...)

6. vi /etc/group
7. root:0:[groupname]
# ex) root:x:0:pi
```
  
###### [chown]
```sh
#[sudo] chown [-R] username /directory/directory/*

chown root /var/lib/tomcat8/webapps/*
```
  
###### [check running port]
```sh
netstat -ntlp
```
  
###### [find directory or file name]
```sh
# sudo find / -name [name] 

sudo find / -name tomcat8
```
  
###### [service process]
```sh
# sudo service [process/-version] start or stop

sudo service tomcat8 start
sudo service tomcat8 stop
sudo service tomcat8 restart
```  
  
###### [port forwarding default port]
```sh
# for accessing server which has private ip need to port forwarding

# If we'll access to use ssh or (s)ftp, we should set a private IP port as 22
```
  
###### [check log]
```sh
# tail -f directory/directory/file name
tail -f tomcat/logs/catalina.out
```

