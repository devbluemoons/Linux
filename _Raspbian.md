### Raspbian
```sh
sudo apt-get update       # 패키지 인덱스 정보 갱신
sudo apt-get upgrade      # 설치된 패키지 업그레이드
sudo apt-get dist-upgrade # 자동 업그레이드 수행 못한 패키지 업그레이드
```
  
###### set-up ftp
```sh
[sudo] apt-get install vsftpd

vi /etc/vsftpd.conf

anonymous_enable=NO
local_enable=YES
write_enable=YES
local_umask=022
chroot_local_user=YES
chroot_list_enable=YES
chroot_list_file=/etc/vsftpd.chroot_list

sudo vi /etc/vsftpd.chroot_list

# type "pi" and then :wq

sudo service vsftpd restart
# OR
sudo systemctl restart vsftpd

sudo systemctl status vsftpd
```
