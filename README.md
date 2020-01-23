### linux self-study
  
###### [check version]
```sh
uname -a
#OR
cat /etc/issue
```
  
###### [access root authority]
```sh
su - root
#and then type password
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
