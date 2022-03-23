
https://hakaveret.education.gov.il/

https://hakaveret.education.gov.il/auth/saml/login.php?manual


## Testing Env

Branch Repo for general moodle 
https://dev.azure.com/CET-Tech/Moodle/_git/moodle_azure_2021
Branch: dev310

Branch Repo for kaveret moodle
https://dev.azure.com/CET-Tech/Moodle/_git/moodle_hakaveret 
Branch: hakaveret310dev

172.17.41.202 - develop host server (use winscp to connect)

https://hakaveretnew.testing.cet.ac.il/

localhost/moodle_hakaveret/

## set up dev env
VirtualBox 
Machine Name: MoodleTPL
OS: Ubuntu 20 LTS
Installation: Moodle 3.10.4+ (Build: 20210701)

Terminal user history
```bash
1  sudo apt install gnome-tweak-tool
2  gnome-tweaks
3  sudo apt install apache2 wget unzip
4  sudo apt install php php-zip php-json php-mbstring php-mysql
5  sudo systemctl enable apache2
6  sudo systemctl start apache2
7  sudo apt update
8  sudo apt install mariadb-server
9  cd /var/www/html/
10  ll
11  mv index.html index1.html
12  cd ../
13  chmod -r 777 html/
14  sudo chmod -r 777 html/
15  exit
16  dmesg
17  sudo ufw status
18  sudo ufw enable
19  shutdown
20  mysql --version
21  history
```

Terminal root history 
```bash
1  mysql
2  systemctl stop mariadb.service
3  systemctl status mariadb.service
4  sudo systemctl set-environment MYSQLD_OPTS="--skip-grant-tables --skip-networking"
5  sudo systemctl start mariadb
6  mysql
7  sudo systemctl edit mysql
8  sudo systemctl daemon-reload
9  sudo systemctl start mysql
10  mysql
11  history
```


For H5P increase memory size : https://connectwww.com/how-to-change-php-file-upload-size-limit-in-ubuntu/5087/



### VSCode extensions
SQLTools


### Config hosts file
edit /etc/hosts

C:\Windows\System32\drivers\etc

Open as root / administrator (notepad++) and add:

    172.17.41.202 hakaveret-ori.dev.cet.ac.il

### Database
Install MariaDB 

create a database:

    $ sudo mysql
    MariaDB [(none)]> show databases;
    MariaDB [(none)]> create database hakaveretdb;
    MariaDB [(none)]> exit;

[Change root user password tutorial](https://www.digitalocean.com/community/tutorials/how-to-reset-your-mysql-or-mariadb-root-password-on-ubuntu-20-04)

