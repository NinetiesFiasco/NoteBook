# Пользователи Ubuntu

## Посмотреть всех

* `cat /etc/passwd`  Все данные в файле
* `sed 's/:.*//' /etc/passwd` Только имена

## Добавить пользователя

* `adduser username` Добавление

## Сменить пользователя

* `sudo su - username` Смена

## Удалить пользователя

* `deluser username` Удаление

## Добавить группу

* `sudo groupadd myGroup`

## Добавить пользователя в группу

* `sudo usermod -aG myGroup user`

## Посмотреть группы пользователя 

* `groups user`

## Изменить группу папки
* `sudo chgrp myGroup myFolder`

## Раздать всё и сразу 
* `chmod -R 777 myFolder`
