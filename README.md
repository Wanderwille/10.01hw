# Домашнее задание к занятию " ELK " - "Подус Сергей"

## Задание 1

Установите и запустите Elasticsearch, после чего поменяйте параметр cluster_name на случайный.

Приведите скриншот команды 'curl -X GET 'localhost:9200/_cluster/health?pretty', сделанной на сервере с установленным Elasticsearch. Где будет виден нестандартный cluster_name.

### Ответ: 

![Скриншот 1](https://github.com/Wanderwille/scrinshot/blob/main/Elastic.png)

## Задание 2

Установите и запустите Kibana.

Приведите скриншот интерфейса Kibana на странице http://<ip вашего сервера>:5601/app/dev_tools#/console, где будет выполнен запрос GET /_cluster/health?pretty.


### Ответ:

![Скриншот 2](https://github.com/Wanderwille/scrinshot/blob/main/Kibana.png)

## Задание 3

Установите и запустите Logstash и Nginx. С помощью Logstash отправьте access-лог Nginx в Elasticsearch.

Приведите скриншот интерфейса Kibana, на котором видны логи Nginx.

### Ответ:

![Скриншот 3](https://github.com/Wanderwille/scrinshot/blob/main/image%20(17).png)

## Задание 4

Установите и запустите Filebeat. Переключите поставку логов Nginx с Logstash на Filebeat.

Приведите скриншот интерфейса Kibana, на котором видны логи Nginx, которые были отправлены через Filebeat.

### Ответ:

![Скриншот 4](https://github.com/Wanderwille/scrinshot/blob/main/image%20(18).png)