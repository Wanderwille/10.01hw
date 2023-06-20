# Домашнее задание к занятию "Zabbix - часть 1" - "Подус Сергей"       

### Задание 1
Установите Zabbix Server с веб-интерфейсом.

Процесс выполнения
Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
Установите PostgreSQL. Для установки достаточна та версия что есть в системном репозитороии Debian 11
Пользуясь конфигуратором комманд с официального сайта, составьте набор команд для установки последней версии Zabbix с поддержкой PostgreSQL и Apache
Выполните все необходимые команды для установки Zabbix Server и Zabbix Web Server
Ответ: 
![Скриншот 1](https://github.com/Wanderwille/scrinshot/blob/main/VirtualBox_Deba_20_06_2023_09_32_10.png)

Команды для установки и настройки:
##### wget https://repo.zabbix.com/zabbix/6.4/debian/pool/main/z/zabbix-release/zabbix-release_6.4-1+debian12_all.deb
##### dpkg -i zabbix-release_6.4-1+debian12_all.deb
##### apt update
##### apt install zabbix-server-pgsql zabbix-frontend-php php8.2-pgsql zabbix-apache-conf zabbix-sql-scripts zabbix-agent
##### sudo -u postgres createuser --pwprompt zabbix
##### sudo -u postgres createdb -O zabbix zabbix##
##### zcat /usr/share/zabbix-sql-scripts/postgresql/server.sql.gz | sudo -u zabbix psql zabbix
##### systemctl restart zabbix-server zabbix-agent apache2
##### systemctl enable zabbix-server zabbix-agent apache2
Так же была отредактирована строчка DBpassword=#####* в файле /etc/zabbix/zabbix_server.conf

### Задание 2
Установите Zabbix Agent на два хоста.

Процесс выполнения
Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
Установите Zabbix Agent на 2 виртмашины, одной из них может быть ваш Zabbix Server
Добавьте Zabbix Server в список разрешенных серверов ваших Zabbix Agentов
Добавьте Zabbix Agentов в раздел Configuration > Hosts вашего Zabbix Servera
Проверьте что в разделе Latest Data начали появляться данные с добавленных агентов

Ответ:
![Скриншот 2](https://github.com/Wanderwille/scrinshot/blob/main/zabbix%201.png)
![Скриншот 3](https://github.com/Wanderwille/scrinshot/blob/main/zabbix2.png)
![Скриншот 4](https://github.com/Wanderwille/scrinshot/blob/main/zabbix%203.png)

Команды используемые в задании:
Так как все ВМ это Debian то:
##### wget https://repo.zabbix.com/zabbix/6.4/debian/pool/main/z/zabbix-release/zabbix-release_6.4-1+debian12_all.deb
##### dpkg -i zabbix-release_6.4-1+debian12_all.deb
##### apt update 
##### apt install zabbix-agent2 zabbix-agent2-plugin-*
##### systemctl restart zabbix-agent
##### systemctl enable zabbix-agent