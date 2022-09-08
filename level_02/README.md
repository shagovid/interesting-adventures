# Тестовые задания

## Подготовка к выполнению

1. Подключиться к vm по ssh через любой клиент (порт 2235 порт)

2. Установить пакет firewalld

<details> 
  <summary>[root@sh-centos7cs ~]# yum install firewalld </summary>

```bash 
[root@sh-centos7cs ~]# yum install firewalld

Loaded plugins: fastestmirror
Determining fastest mirrors
base                                                     | 3.6 kB     00:00
epel                                                     | 4.7 kB     00:00
extras                                                   | 2.9 kB     00:00
selectel-openstack                                       | 2.9 kB     00:00
updates                                                  | 2.9 kB     00:00
(1/6): epel/group_gz                                       |  97 kB   00:00
(2/6): epel/updateinfo                                     | 1.0 MB   00:00
(3/6): selectel-openstack/primary_db                       | 6.6 kB   00:00
(4/6): extras/primary_db                                   | 250 kB   00:00
(5/6): epel/primary_db                                     | 7.0 MB   00:00
(6/6): updates/primary_db                                  |  17 MB   00:00
Resolving Dependencies
--> Running transaction check
---> Package firewalld.noarch 0:0.6.3-13.el7_9 will be installed
--> Processing Dependency: python-firewall = 0.6.3-13.el7_9 for package: firewalld-0.6.3-13.el7_9.noarch
--> Processing Dependency: firewalld-filesystem = 0.6.3-13.el7_9 for package: firewalld-0.6.3-13.el7_9.noarch
--> Processing Dependency: ipset for package: firewalld-0.6.3-13.el7_9.noarch
--> Processing Dependency: ebtables for package: firewalld-0.6.3-13.el7_9.noarch
--> Running transaction check
---> Package ebtables.x86_64 0:2.0.10-16.el7 will be installed
---> Package firewalld-filesystem.noarch 0:0.6.3-13.el7_9 will be installed
---> Package ipset.x86_64 0:7.1-1.el7 will be installed
--> Processing Dependency: ipset-libs(x86-64) = 7.1-1.el7 for package: ipset-7.1-1.el7.x86_64
--> Processing Dependency: libipset.so.13(LIBIPSET_4.8)(64bit) for package: ipset-7.1-1.el7.x86_64
--> Processing Dependency: libipset.so.13(LIBIPSET_2.0)(64bit) for package: ipset-7.1-1.el7.x86_64
--> Processing Dependency: libipset.so.13()(64bit) for package: ipset-7.1-1.el7.x86_64
---> Package python-firewall.noarch 0:0.6.3-13.el7_9 will be installed
--> Processing Dependency: python-slip-dbus for package: python-firewall-0.6.3-13.el7_9.noarch
--> Running transaction check
---> Package ipset-libs.x86_64 0:7.1-1.el7 will be installed
---> Package python-slip-dbus.noarch 0:0.4.0-4.el7 will be installed
--> Processing Dependency: python-slip = 0.4.0-4.el7 for package: python-slip-dbus-0.4.0-4.el7.noarch
--> Running transaction check
---> Package python-slip.noarch 0:0.4.0-4.el7 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

================================================================================
 Package                   Arch        Version               Repository    Size
================================================================================
Installing:
 firewalld                 noarch      0.6.3-13.el7_9        updates      449 k
Installing for dependencies:
 ebtables                  x86_64      2.0.10-16.el7         base         123 k
 firewalld-filesystem      noarch      0.6.3-13.el7_9        updates       51 k
 ipset                     x86_64      7.1-1.el7             base          39 k
 ipset-libs                x86_64      7.1-1.el7             base          64 k
 python-firewall           noarch      0.6.3-13.el7_9        updates      355 k
 python-slip               noarch      0.4.0-4.el7           base          31 k
 python-slip-dbus          noarch      0.4.0-4.el7           base          32 k

Transaction Summary
================================================================================
Install  1 Package (+7 Dependent packages)

Total download size: 1.1 M
Installed size: 4.5 M
Is this ok [y/d/N]: y
Downloading packages:
(1/8): ebtables-2.0.10-16.el7.x86_64.rpm                   | 123 kB   00:00
(2/8): ipset-libs-7.1-1.el7.x86_64.rpm                     |  64 kB   00:00
(3/8): firewalld-filesystem-0.6.3-13.el7_9.noarch.rpm      |  51 kB   00:00
(4/8): ipset-7.1-1.el7.x86_64.rpm                          |  39 kB   00:00
(5/8): firewalld-0.6.3-13.el7_9.noarch.rpm                 | 449 kB   00:00
(6/8): python-slip-dbus-0.4.0-4.el7.noarch.rpm             |  32 kB   00:00
(7/8): python-firewall-0.6.3-13.el7_9.noarch.rpm           | 355 kB   00:00
(8/8): python-slip-0.4.0-4.el7.noarch.rpm                  |  31 kB   00:00
--------------------------------------------------------------------------------
Total                                              7.4 MB/s | 1.1 MB  00:00
Running transaction check
Running transaction test
Transaction test succeeded
Running transaction
Warning: RPMDB altered outside of yum.
  Installing : ebtables-2.0.10-16.el7.x86_64                                1/8
  Installing : ipset-libs-7.1-1.el7.x86_64                                  2/8
  Installing : ipset-7.1-1.el7.x86_64                                       3/8
  Installing : python-slip-0.4.0-4.el7.noarch                               4/8
  Installing : python-slip-dbus-0.4.0-4.el7.noarch                          5/8
  Installing : python-firewall-0.6.3-13.el7_9.noarch                        6/8
  Installing : firewalld-filesystem-0.6.3-13.el7_9.noarch                   7/8
  Installing : firewalld-0.6.3-13.el7_9.noarch                              8/8
  Verifying  : ipset-7.1-1.el7.x86_64                                       1/8
  Verifying  : python-slip-dbus-0.4.0-4.el7.noarch                          2/8
  Verifying  : firewalld-filesystem-0.6.3-13.el7_9.noarch                   3/8
  Verifying  : firewalld-0.6.3-13.el7_9.noarch                              4/8
  Verifying  : python-slip-0.4.0-4.el7.noarch                               5/8
  Verifying  : python-firewall-0.6.3-13.el7_9.noarch                        6/8
  Verifying  : ipset-libs-7.1-1.el7.x86_64                                  7/8
  Verifying  : ebtables-2.0.10-16.el7.x86_64                                8/8

Installed:
  firewalld.noarch 0:0.6.3-13.el7_9

Dependency Installed:
  ebtables.x86_64 0:2.0.10-16.el7
  firewalld-filesystem.noarch 0:0.6.3-13.el7_9
  ipset.x86_64 0:7.1-1.el7
  ipset-libs.x86_64 0:7.1-1.el7
  python-firewall.noarch 0:0.6.3-13.el7_9
  python-slip.noarch 0:0.4.0-4.el7
  python-slip-dbus.noarch 0:0.4.0-4.el7

Complete!
```

</details>

#### При работе ssh через порт 2235 необходимо перед стартом firewalld перевести ssh на 22 порт
#### Запустить firewalld, добавить исключение, потом перевести обратно, иначе грозит потерей доступа!!!
#### [root@sh-centos7cs ~]# firewall-cmd --add-port=2235/tcp FirewallD is not running
#### При не запущенном firewalld это сделать нельзя!!!

3. Запустим firewalld и добавим в автозагрузку при старте ОС.

```bash
[root@sh-centos7cs ~]# systemctl enable firewalld.service
[root@sh-centos7cs ~]# systemctl start firewalld.service
```

4. На мастере разрешим подключаться к серверу по tcp порту 3306, на котором работает mysql сервер + 2235 ssh

```bash
[root@sh-centos7cs2 sid]# firewall-cmd --permanent --add-port=3306/tcp
success
[root@sh-centos7cs2 sid]# firewall-cmd --permanent --add-port=2235/tcp
success
```

5. Проверим статус сервиса firewalld.

```bash
[root@sh-centos7cs2 sid]# systemctl status firewalld

● firewalld.service - firewalld - dynamic firewall daemon
   Loaded: loaded (/usr/lib/systemd/system/firewalld.service; enabled; vendor preset: enabled)
   Active: active (running) since Mon 2022-09-05 18:37:58 UTC; 1min 5s ago
     Docs: man:firewalld(1)
 Main PID: 7832 (firewalld)
   CGroup: /system.slice/firewalld.service
           └─7832 /usr/bin/python2 -Es /usr/sbin/firewalld --nofork --nopid

Sep 05 18:37:57 sh-centos7cs2.ru-central1.internal systemd[1]: Starting firew...
Sep 05 18:37:58 sh-centos7cs2.ru-central1.internal systemd[1]: Started firewa...
Sep 05 18:37:58 sh-centos7cs2.ru-central1.internal firewalld[7832]: WARNING: ...
Hint: Some lines were ellipsized, use -l to show in full.
```

## Задание 1.1

Установить Community Server на предоставленную ВМ.

## Решение задания 1.1

1. Версия Centos + просмотр версии ядра Linux

```bash 
[root@sh-centos7cs ~]# cat /etc/centos-release
CentOS Linux release 7.9.2009 (Core)
[root@sh-centos7cs ~]# uname -r
3.10.0-1160.53.1.el7.x86_64
```

2. Текущая версия Python

```bash 
[root@sh-centos7cs ~]# python -V
Python 2.7.5

[root@sh-centos7cs ~]# python3 --version
Python 3.6.8
```

3. Скачиваем файл скрипта Р7-Офис. Сервер. Профессиональный для CentOS

```bash 
[root@sh-centos7cs ~]# wget https://download.r7-office.ru/repo/install-RedHat.sh

--2022-09-05 19:50:24--  https://download.r7-office.ru/repo/install-RedHat.sh
Resolving download.r7-office.ru (download.r7-office.ru)... 5.178.85.228
Connecting to download.r7-office.ru (download.r7-office.ru)|5.178.85.228|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3210 (3.1K) [application/x-sh]
Saving to: ‘install-RedHat.sh’

100%[======================================>] 3,210       --.-K/s   in 0s

2022-09-05 19:50:24 (499 MB/s) - ‘install-RedHat.sh’ saved [3210/3210]
```

4. Установим все компоненты и модули Р7-Офис. Сервер. Профессиональный
Требуется более 40Гб свободного места на диске!
При установке одному скрипту понадобилась версия Python 3.7 и выше!

```bash 
[root@sh-centos7cs2 sid]# bash install-RedHat.sh

................................................

Trying to establish MySQL connection... OK
Restarting services...
r7-officeJabber.service
OK
6144+0 records in
6144+0 records out
6442450944 bytes (6.4 GB) copied, 54.754 s, 118 MB/s
Setting up swapspace version 1, size = 6291452 KiB
no label, UUID=3122a50b-070c-4c17-8b75-5255ba2cfdb2
firewalld-0.6.3-13.el7_9.noarch
success
success

Спасибо за инсталляцию Р7-Офис. Сервер
Вы можете сконфигурировать ваш портал используя Р7-Офис. Панель управления.
Если у вас есть какие-либо вопросы вы можете связаться с нами через http://wwww.r7-office.ru
```

5. Проверим работу Р7-Офис через браузер

![img1](img/img1.png)

---

## Задание 1.2

Перевести портал на https, добавив самоподписной сертификат. 

## Решение задания 1.2

1.  Создадим сертификат, подписанный Центром Сертификации letsencrypt и переключим портал на протокол HTTPS

```bash 
[root@sh-centos7cs2 sid]# bash /var/www/r7-office/Tools/letsencrypt.sh kuberwars.online
Saving debug log to /var/log/letsencrypt/letsencrypt.log
Account registered.
Requesting a certificate for kuberwars.online

Successfully received certificate.
Certificate is saved at: /etc/letsencrypt/live/kuberwars.online/fullchain.pem
Key is saved at:         /etc/letsencrypt/live/kuberwars.online/privkey.pem
This certificate expires on 2022-12-05.
These files will be updated when the certificate renews.
Certbot has set up a scheduled task to automatically renew this certificate in the background.

- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -
If you like Certbot, please consider supporting our work by:
 * Donating to ISRG / Let's Encrypt:   https://letsencrypt.org/donate
 * Donating to EFF:                    https://eff.org/donate-le
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -
Generating DH parameters, 2048 bit long safe prime, generator 2
This is going to take a long time
.........................+.........+.................................++*++*
```

2. Проверим сертификат для сервера Р7-Офис через браузер

![img2](img/img2.png)

---

## Задание 1.3

Добавить и настроить nginx в качестве реверс прокси.

## Решение задания 1.3

1. Похоже что реверс прокси сконфигурирован из коробки

<details> 
  <summary>root@sh-centos7cs2 conf.d]# cat /etc/nginx/conf.d/r7-office.conf </summary>

```bash 
root@sh-centos7cs2 conf.d]# cat /etc/nginx/conf.d/r7-office.conf
upstream fastcgi_backend_apisystem {
        server unix:/var/run/r7-office/r7-officeApiSystem.socket;
        keepalive 32;
}

upstream fastcgi_backend {
        server unix:/var/run/r7-office/r7-office.socket;
        keepalive 64;
}

fastcgi_cache_path /var/cache/nginx/r7-office
        levels=1:2
        keys_zone=r7-office:256m
        max_size=1024m
        inactive=1d;

geo $ip_external {
     default 1;
     127.0.0.1 0;
}

map $http_host $this_host {
  "" $host;
  default $http_host;
}

map $http_x_forwarded_proto $the_scheme {
  default $http_x_forwarded_proto;
  "" $scheme;
}

map $http_x_forwarded_host $the_host {
  default $http_x_forwarded_host;
  "" $this_host;
}

map $request_uri $header_access_control_allow_origin {
  ~*^/(api\/2.0|products\/crm\/httphandlers\/webtoleadfromhandler.ashx|products\/files\/httphandlers\/filehandler.ashx|products\/files\/chunkeduploader.ashx|thirdparty\/plugin) "*";
  default "";
}

map $request_uri $header_x_frame_options {
  ~*^/(favicon\.ico|products\/files\/share\.aspx|products\/files\/saveas\.aspx|products\/files\/filechoice\.aspx|products\/files\/doceditor\.aspx|thirdparty\/plugin) "";
  default "SAMEORIGIN";
}

server {
        listen 0.0.0.0:80 default_server;
        listen [::]:80;

        server_name _;
        server_tokens off;

        root /nowhere; ## root doesn't have to be a valid path since we are redirecting

        location / {
                if ($ip_external) {
                                ## Redirects all traffic to the HTTPS host
                                 rewrite ^ https://$host$request_uri? permanent;
                        }

                        client_max_body_size 100m;

                        proxy_pass https://127.0.0.1;
                        proxy_http_version 1.1;
                        proxy_set_header Upgrade $http_upgrade;
                        proxy_set_header Connection "upgrade";
                        proxy_set_header Host $host;
                        proxy_set_header X-Real-IP $remote_addr;
                        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
                        proxy_set_header X-Forwarded-Host $server_name;
                        proxy_set_header X-Forwarded-Proto $scheme;
                        proxy_ssl_verify off;
        }
}

server {
        listen 0.0.0.0:443 ssl http2;
        listen [::]:443 ssl http2 default_server;

        charset utf-8;

        server_tokens off;

        ## Increase this if you want to upload large attachments
        client_max_body_size 100m;

        ssl_certificate /var/www/r7-office/Data/certs/r7-office.crt;
        ssl_certificate_key /var/www/r7-office/Data/certs/r7-office.key;
        ssl_verify_client off;
    ssl_session_timeout 1d;
    ssl_session_cache shared:MozSSL:10m;  # about 40000 sessions
    ssl_session_tickets off;

        ssl_protocols TLSv1.2;
    ssl_ciphers ECDHE-ECDSA-AES128-GCM-SHA256:ECDHE-RSA-AES128-GCM-SHA256:ECDHE-ECDSA-AES256-GCM-SHA384:ECDHE-RSA-AES256-GCM-SHA384:ECDHE-ECDSA-CHACHA20-POLY1305:ECDHE-RSA-CHACHA20-POLY1305:DHE-RSA-AES128-GCM-SHA256:DHE-RSA-AES256-GCM-SHA384;
        ssl_prefer_server_ciphers off;

        add_header Strict-Transport-Security "max-age=63072000; includeSubDomains; preload" always;
    add_header X-Frame-Options $header_x_frame_options;
        add_header X-Content-Type-Options nosniff;
        add_header Access-Control-Allow-Origin $header_access_control_allow_origin;

        ssl_stapling on;
        ssl_stapling_verify on;
        ssl_trusted_certificate /var/www/r7-office/Data/certs/stapling.trusted.crt;
        resolver 8.8.8.8 8.8.4.4 127.0.0.11 valid=300s; # Can change to your DNS resolver if desired
        resolver_timeout 10s;

        ssl_dhparam /var/www/r7-office/Data/certs/dhparam.pem;

        large_client_header_buffers 4 16k;

        set $X_REWRITER_URL $the_scheme://$the_host;

        if ($http_x_rewriter_url != '') {
                set $X_REWRITER_URL $http_x_rewriter_url ;
        }

    include /etc/nginx/includes/r7-office-communityserver-*.conf;
}
```

</details>

---

## Задание 1.4

Настроить репликацию бд mysql master - slave.

## Решение задания 1.4

1. Вносим правки в my.cnf на основном сервере.  

```bash
[root@sh-centos7cs2 ~]# sudo vi /etc/my.cnf
[root@sh-centos7cs2 sid]# cat /etc/my.cnf
# For advice on how to change settings please see
# http://dev.mysql.com/doc/refman/8.0/en/server-configuration-defaults.html

[mysqld]
default-authentication-plugin = mysql_native_password
collation_server = utf8_general_ci
character_set_server = utf8
max_allowed_packet = 1048576000
group_concat_max_len = 2048
max_connections = 1000
sql_mode = 'NO_ENGINE_SUBSTITUTION'
#
# Remove leading # and set to the amount of RAM for the most important data
# cache in MySQL. Start at 70% of total RAM for dedicated server, else 10%.
# innodb_buffer_pool_size = 128M
#
# Remove the leading "# " to disable binary logging
# Binary logging captures changes between backups and is enabled by
# default. It's default setting is log_bin=binlog
# disable_log_bin
#
# Remove leading # to set options mainly useful for reporting servers.
# The server defaults are faster for transactions and fast SELECTs.
# Adjust sizes as needed, experiment to find the optimal values.
# join_buffer_size = 128M
# sort_buffer_size = 2M
# read_rnd_buffer_size = 2M
#
# Remove leading # to revert to previous value for default_authentication_plugin,
# this will increase compatibility with older clients. For background, see:
# https://dev.mysql.com/doc/refman/8.0/en/server-system-variables.html#sysvar_default_authentication_plugin
# default-authentication-plugin=mysql_native_password

datadir=/var/lib/mysql
socket=/var/lib/mysql/mysql.sock

log-error=/var/log/mysqld.log
pid-file=/var/run/mysqld/mysqld.pid

# выбираем ID сервера, произвольное число, лучше начинать с 1
server-id = 1
# путь к бинарному логу
log_bin = /var/log/mysql/mysql-bin.log
# название базы данных, которая будет реплицироваться
binlog_do_db = r7-office
```

2. Перезапускаем Mysql.  

```bash
[root@sh-centos7cs2 sid]# sudo systemctl restart mysqld
```

3. Авторизуемся в mysql (root ei7veeChu4bo!) и посмотрим список баз на основном сервере. 

```bash
[root@sh-centos7cs2 sid]# mysql -u root -p
mysql> SHOW DATABASES;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| r7-office          |
| sys                |
+--------------------+
5 rows in set (0.01 sec)
```

4. Cоздадим на основном сервере учетную запись (slave_user), от имени которой будет работать репликация 

```bash
mysql> CREATE USER 'slave_user'@'45.94.123.5' IDENTIFIED BY 'ei7veeChu4bo!';
Query OK, 0 rows affected (0.01 sec)

mysql> GRANT replication slave ON *.* TO 'slave_user'@'45.94.123.5';
Query OK, 0 rows affected (0.00 sec)
```

5. Блокируем все таблицы в нашей базе данных. 

```bash
mysql> FLUSH TABLES WITH READ LOCK;
Query OK, 0 rows affected (0.00 sec)
```

6. Cделаем дамп базы данных r7-office на основном сервере.  

```bash
[root@sh-centos7cs2 sid]# mysqldump -u root -p r7-office > r7-office.sql

[root@sh-centos7cs2 sid]# ls
install-RedHat.sh  r7-office.sql
```

7. Проверяем автоустановленную версию MySQL на основном сервере.  

```bash
[root@sh-centos7cs2 sid]# mysql -V
mysql  Ver 8.0.30 for Linux on x86_64 (MySQL Community Server - GPL)
```

8. Проверяем и удаляем MariaDB на сервере для репликации БД.  

```bash
[root@sh-mysqlforcentos7cs ~]# rpm -qa | grep mariadb
mariadb-libs-5.5.68-1.el7.x86_64

[root@sh-mysqlforcentos7cs ~]# rpm -e --nodeps mariadb-libs-5.5.68-1.el7.x86_64
```

9. Скачаем mysql сервер 8.0.30 на сервер для репликации БД.  

```bash
[root@sh-mysqlforcentos7cs ~]# wget https://dev.mysql.com/get/mysql80-community-release-el7-7.noarch.rpm

100%[======================================>] 11,196      --.-K/s   in 0s

2022-09-07 20:53:11 (185 MB/s) - ‘mysql80-community-release-el7-7.noarch.rpm’ saved [11196/11196]
```

10. Добавим репозиторий MySQL Yum в список хранилищ системы.  

```bash
[root@sh-mysqlforcentos7cs ~]# yum localinstall mysql80-community-release-el7-7.noarch.rpm
Loaded plugins: fastestmirror
Examining mysql80-community-release-el7-7.noarch.rpm: mysql80-community-release-el7-7.noarch
Marking mysql80-community-release-el7-7.noarch.rpm to be installed
Resolving Dependencies
--> Running transaction check
---> Package mysql80-community-release.noarch 0:el7-7 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

================================================================================
 Package             Arch   Version
                                  Repository                               Size
================================================================================
Installing:
 mysql80-community-release
                     noarch el7-7 /mysql80-community-release-el7-7.noarch  10 k

Transaction Summary
================================================================================
Install  1 Package

Total size: 10 k
Installed size: 10 k
Is this ok [y/d/N]: y
Downloading packages:
Running transaction check
Running transaction test
Transaction test succeeded
Running transaction
Warning: RPMDB altered outside of yum.
** Found 2 pre-existing rpmdb problem(s), 'yum check' output follows:
2:postfix-2.10.1-9.el7.x86_64 has missing requires of libmysqlclient.so.18()(64bit)
2:postfix-2.10.1-9.el7.x86_64 has missing requires of libmysqlclient.so.18(libmysqlclient_18)(64bit)
  Installing : mysql80-community-release-el7-7.noarch                       1/1
  Verifying  : mysql80-community-release-el7-7.noarch                       1/1

Installed:
  mysql80-community-release.noarch 0:el7-7

Complete!
```

11. Проверим, успешно ли добавлен репозиторий MySQL Yum.  

```bash
[root@sh-mysqlforcentos7cs ~]# yum repolist enabled | grep "mysql.*-community.*"
mysql-connectors-community/x86_64       MySQL Connectors Community           199
mysql-tools-community/x86_64            MySQL Tools Community                 92
mysql80-community/x86_64                MySQL 8.0 Community Server           346
```

12. Установим сервер MySQL.  

```bash
[root@sh-mysqlforcentos7cs ~]# yum install mysql-community-server
.................................................................
Installed:
  mysql-community-server.x86_64 0:8.0.30-1.el7

Dependency Installed:
  mysql-community-client.x86_64 0:8.0.30-1.el7
  mysql-community-client-plugins.x86_64 0:8.0.30-1.el7
  mysql-community-common.x86_64 0:8.0.30-1.el7
  mysql-community-icu-data-files.x86_64 0:8.0.30-1.el7
  mysql-community-libs.x86_64 0:8.0.30-1.el7

Complete!
```

13. Запустим сервер MySQL и проверим состояние.  

```bash
[root@sh-mysqlforcentos7cs ~]# service mysqld start
Redirecting to /bin/systemctl start mysqld.service
[root@sh-mysqlforcentos7cs ~]# service mysqld status
Redirecting to /bin/systemctl status mysqld.service
● mysqld.service - MySQL Server
   Loaded: loaded (/usr/lib/systemd/system/mysqld.service; enabled; vendor preset: disabled)
   Active: active (running) since Wed 2022-09-07 21:02:34 MSK; 19s ago
     Docs: man:mysqld(8)
           http://dev.mysql.com/doc/refman/en/using-systemd.html
  Process: 4136 ExecStartPre=/usr/bin/mysqld_pre_systemd (code=exited, status=0/SUCCESS)
 Main PID: 4215 (mysqld)
   Status: "Server is operational"
   CGroup: /system.slice/mysqld.service
           └─4215 /usr/sbin/mysqld

Sep 07 21:02:25 sh-mysqlforcentos7cs systemd[1]: Starting MySQL Server...
Sep 07 21:02:34 sh-mysqlforcentos7cs systemd[1]: Started MySQL Server.
```

14. Посмотрим пароль root на сервере MySQL.  

```bash
[root@sh-mysqlforcentos7cs ~]# grep 'temporary password' /var/log/mysqld.log
2022-09-07T18:02:29.847731Z 6 [Note] [MY-010454] [Server] A temporary password is generated for root@localhost: Fgt=Z2cqgaEd
```

15. Сменим пароль root на сервере MySQL.    

```bash
mysql> ALTER USER 'root'@'localhost' IDENTIFIED  BY 'ei7veeChu4bo!';
Query OK, 0 rows affected (0.01 sec)
```

16. Создаем базу r7-office.  

```bash
mysql> create database `r7-office`;
Query OK, 1 row affected (0.01 sec)
```

17. Пересылаем файл с дампом БД с основного сервера на побочный.  

```bash
[root@sh-centos7cs2 sid]# scp -P 2235 r7-office.sql root@45.94.123.5:/r7-office.sql
```

18. После этого загружаем дамп на побочном сервере.  

```bash
[root@sh-mysqlforcentos7cs /]# mysql -u root -p r7-office < r7-office.sql
```

19. Вносим правки в my.cnf на побочном сервере.  

```bash
[root@sh-mysqlforcentos7cs /]# cat /etc/my.cnf
[mysqld]

...........................................................

datadir=/var/lib/mysql
socket=/var/lib/mysql/mysql.sock

log-error=/var/log/mysqld.log
pid-file=/var/run/mysqld/mysqld.pid

max_allowed_packet = 1048576000

# ID Слейва
server-id = 2
# Путь к relay логу
relay-log = /var/log/mysql/mysql-relay-bin.log
# База данных для репликации
binlog_do_db = r7-office
# Путь к bin логу на Мастере
log_bin = /var/log/mysql/mysql-bin.log
```

20. Запускаем репликацию. Для этого идем на мастер и смотрим master log position в консоли mysql.  

```bash
[root@sh-centos7cs2 sid]# mysql -u root -p
Enter password:
..................................................................................
mysql> show master status;
+---------------+----------+--------------+------------------+-------------------+
| File          | Position | Binlog_Do_DB | Binlog_Ignore_DB | Executed_Gtid_Set |
+---------------+----------+--------------+------------------+-------------------+
| binlog.000002 |      157 | r7-office    |                  |                   |
+---------------+----------+--------------+------------------+-------------------+
1 row in set (0.00 sec)
```

21. Создаем папки с логами на слейве и правим права.  

```bash
[root@sh-mysqlforcentos7cs ~]# mkdir /var/log/mysql
[root@sh-mysqlforcentos7cs ~]# chown -R mysql:mysql /var/log/mysql
[root@sh-mysqlforcentos7cs ~]# chmod 777 /var/log/mysql
```

22. Включаем репликацию, для этого необходимо указать параметры подключения к мастеру с побочного сервера 

```bash
mysql> CHANGE MASTER TO MASTER_HOST = '158.160.11.51', MASTER_USER = 'slave_user', MASTER_PASSWORD = 'ei7veeChu4bo!', MASTER_LOG_FILE = 'binlog.000002', MASTER_LOG_POS = 157;
Query OK, 0 rows affected, 8 warnings (0.03 sec)

mysql> start slave;
Query OK, 0 rows affected, 1 warning (0.02 sec)
```


23. Были проблемы с репликацией, помогла команда на мастере

```bash
mysql> SET GLOBAL sync_binlog=1;
```

24. Проверяем работу репликации на побочном сервере 

```bash
mysql> show slave status \G;
*************************** 1. row ***************************
               Slave_IO_State: Waiting for source to send event
                  Master_Host: 158.160.11.51
                  Master_User: slave_user
                  Master_Port: 3306
                Connect_Retry: 60
              Master_Log_File: mysql-bin.000002
          Read_Master_Log_Pos: 157
               Relay_Log_File: mysql-relay-bin.000004
                Relay_Log_Pos: 326
        Relay_Master_Log_File: mysql-bin.000002
             Slave_IO_Running: Yes
            Slave_SQL_Running: Yes
              Replicate_Do_DB:
          Replicate_Ignore_DB:
           Replicate_Do_Table:
       Replicate_Ignore_Table:
      Replicate_Wild_Do_Table:
  Replicate_Wild_Ignore_Table:
                   Last_Errno: 0
                   Last_Error:
                 Skip_Counter: 0
          Exec_Master_Log_Pos: 157
              Relay_Log_Space: 536
              Until_Condition: None
               Until_Log_File:
                Until_Log_Pos: 0
           Master_SSL_Allowed: No
           Master_SSL_CA_File:
           Master_SSL_CA_Path:
              Master_SSL_Cert:
            Master_SSL_Cipher:
               Master_SSL_Key:
        Seconds_Behind_Master: 0
Master_SSL_Verify_Server_Cert: No
                Last_IO_Errno: 0
                Last_IO_Error:
               Last_SQL_Errno: 0
               Last_SQL_Error:
  Replicate_Ignore_Server_Ids:
             Master_Server_Id: 1
                  Master_UUID: cfb06db9-2e05-11ed-96f8-d00d8a3b575c
             Master_Info_File: mysql.slave_master_info
                    SQL_Delay: 0
          SQL_Remaining_Delay: NULL
      Slave_SQL_Running_State: Replica has read all relay log; waiting for more updates
           Master_Retry_Count: 86400
                  Master_Bind:
      Last_IO_Error_Timestamp:
     Last_SQL_Error_Timestamp:
               Master_SSL_Crl:
           Master_SSL_Crlpath:
           Retrieved_Gtid_Set:
            Executed_Gtid_Set:
                Auto_Position: 0
         Replicate_Rewrite_DB:
                 Channel_Name:
           Master_TLS_Version:
       Master_public_key_path:
        Get_master_public_key: 0
            Network_Namespace:
1 row in set, 1 warning (0.00 sec)

ERROR:
No query specified
```

---

### Ссылки

1. Ссылка на установку серверной версии Р7-Офис. Сервер. Профессиональный с помощью скрипта для CentOS: https://support.r7-office.ru/https@support.r7-office.ru/hc/ru/articles/4650839521948-_25D0_25A3_25D1_2581_25D1_2582_25D0_25B0_25D0_25BD_25D0_25BE_25D0_25B2_25D0_25BA_25D0_0C83026324.html              
2. Ссылка на переключение Р7-Офис. Сервер. Профессиональный на протокол HTTPS с помощью собственного сертификата: https://support.r7-office.ru/https@support.r7-office.ru/hc/ru/articles/4650866011804-_25D0_259A_25D0_25B0_25D0_25BA-_25D0_25BF_25D0_25B5_25D1_2580_25D0_25B5_25D0_25BA_25D001E0E1DD9D.html        
3. Ссылка на переход на HTTPS с помощью скрипта: https://support.r7-office.ru/https@support.r7-office.ru/hc/ru/articles/4650840176028/default.html
4. Пользователь для репликации в mysql https://dev.mysql.com/doc/refman/8.0/en/replication-howto-repuser.html


---