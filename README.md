# Домашнее задание к занятию "Disaster recovery и Keepalived" - "Подус Сергей"       
    
### Задание 1
Запустите два simple python сервера на своей виртуальной машине на разных портах
Установите и настройте HAProxy, воспользуйтесь материалами к лекции по ссылке
Настройте балансировку Round-robin на 4 уровне.
На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy.
Ответ:
Файл конфига: https://github.com/Wanderwille/file/blob/main/haproxy.cfg.txt
![Скриншот 1](https://github.com/Wanderwille/scrinshot/blob/main/server%201.png)
![Скриншот 2](https://github.com/Wanderwille/scrinshot/blob/main/server%202.png)
![Скриншот 3](https://github.com/Wanderwille/scrinshot/blob/main/curl.png)
![Скриншот 3](https://github.com/Wanderwille/scrinshot/blob/main/haproxy%20web.png)
### Задание 2
Запустите три simple python сервера на своей виртуальной машине на разных портах
Настройте балансировку Weighted Round Robin на 7 уровне, чтобы первый сервер имел вес 2, второй - 3, а третий - 4
HAproxy должен балансировать только тот http-трафик, который адресован домену example.local
На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy c использованием домена example.local и без него.

Ответ:
Файл конфига: https://github.com/Wanderwille/file/blob/main/haproxy2.cfg.txt
![Скриншот 4](https://github.com/Wanderwille/scrinshot/blob/main/мь4.png)
![Скриншот 5](https://github.com/Wanderwille/scrinshot/blob/main/мь45.png)






