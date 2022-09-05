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

3. Запустим firewalld и добавим в авто загрузку при старте ОС.

```bash
[root@sh-centos7cs ~]# systemctl enable firewalld.service
[root@sh-centos7cs ~]# systemctl start firewalld.service
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

4. 

```bash 

```

---

## Задание 1.2

Добавить и настроить nginx в качестве реверс прокси.

## Решение задания 1.2

---

## Задание 1.3

Перевести портал на https, добавив самоподписной сертификат.

## Решение задания 1.3

---

## Задание 1.4

Настроить репликацию бд mysql master - slave.

## Решение задания 1.4

---

### Ссылки

1. Ссылка на установку серверной версии Р7-Офис. Сервер. Профессиональный с помощью скрипта для CentOS: https://support.r7-office.ru/https@support.r7-office.ru/hc/ru/articles/4650839521948-_25D0_25A3_25D1_2581_25D1_2582_25D0_25B0_25D0_25BD_25D0_25BE_25D0_25B2_25D0_25BA_25D0_0C83026324.html              
2. Ссылка на переключение Р7-Офис. Сервер. Профессиональный на протокол HTTPS с помощью собственного сертификата?: https://support.r7-office.ru/https@support.r7-office.ru/hc/ru/articles/4650866011804-_25D0_259A_25D0_25B0_25D0_25BA-_25D0_25BF_25D0_25B5_25D1_2580_25D0_25B5_25D0_25BA_25D001E0E1DD9D.html        

---