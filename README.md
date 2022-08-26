  ###### [check version]
```sh
uname -a
#OR
cat /etc/issue

# detail info
cat /etc/os-release
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

(!보류)
# 4. vi /etc/passwd
# 5. [일반계정명]:x:0(uid):0(gid)(...) 
# ex) pi:x:0:0(...)

# 6. vi /etc/group
# 7. root:0:[groupname]
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
###### [check : directory file size]
```sh
du -h --max-depth=1
```
###### set-up env
```sh
## 리눅스 환경변수 설정

- 설치할 sh 파일을 vi 또는 cat 명령어로 오픈
  
  ex) vi test.sh

- 어느 위치에 설치할 것인지 확인가능 (파일 내부 확인) 

  ex) /usr/local/bin

- 현재 접속중인 최상위 디렉터리로 이동 및 파일 목록 검색

  ex) cd ~
  ex) ll -al

- .bashrc 파일에 환경변수 설정 추가 및 적용

  ex) vi .bashrc
  ex) PATH=$PATH:/usr/local/bin (.bashrc 파일 내부)
  ex) source .bashrc
```

## virtualbox

###### network 

- set adapter
[issue](https://forums.virtualbox.org/viewtopic.php?t=88980)

## search installed package (ubuntu)
```sh
dpkg -l | grep [package-name]

# ex) dpkg -l | grep docker
```

## network
```sh
vi /etc/netplan/***.yaml
vi /etc/hosts

netplan apply
```
