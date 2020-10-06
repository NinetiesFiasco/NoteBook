Команды Ubuntu
=

Ubuntu
-

* `lsb_release -a` Узнать версию
* `sudo reboot` перезагрузка
* `reset` очистить консоль

Обновление Advanced Package Tool
-

* 1. `sudo apt update` Загрузка обновлений
* 2. `sudo apt upgrade` Обновление

Файлы и папки
-

* `ls` просмотр каталога  
* `cd` сменить каталог  
* `mkdir dirName` создать папку  
* `rm -rf dirName` удалить папку
* `touch fileName.extension` создать файл  
* `mv curFileName newFileName` переименновать файл  
* `cp -R folder1 folder2` скопировать папку 1 в папку 2

ZIP
-

* `sudo apt install zip unzip` установка
* `zip -r proj.zip server src package.json` запакует в proj.zip папки server, src и файл package.json
* `unzip fld.zip -d destFld` распакует fld.zip в папку destFld
* `sudo chmod -R 777 destFld` даст всем права на использование этой папки и всех вложенных папок  

IP
-
* ip address

Apache
-
* `sudo apachectl stop` - единожды остановить сервис 
* `sudo update-rc.d apache2 disable` - удалить из автозагрузки

Для изменения портов можно воспользоваться консольным приложением nano  
по путям `/etc/apache2/ports.conf` и `/etc/apache2/sites-enabled/000-default.conf`
изменить порты на нужные.
Как оказалось менять порт надо было в `/etc/apache2/apache2.conf`

Для подключения php в том же /etc/apache2/apache2.conf указать  
```
<FilesMatch \.php$>
  SetHandler application/x-httpd-php
</FilesMatch>
```

Порты
-
* `sudo netstat -ntulp` - поглядеть какие порты работают
* `netstat -tulpn | grep :21` - проверка работоспособности порта

Убить процесс по ID
-
`sudo kill procID`

Пользователи, группы, права
-

* `sudo useradd vasyapupkin` добавить пользователя  
* `id -G` id групп  
* `id -Gn` или groups названия групп  
* `chown root/root /var/www/user` установка прав 0_о  
* `chmod 775 /var/www/user`  установка разрешений 0_о (-R рекурсивно на все подпапки)  
* `su - userName` войти как пользователь  
* `cat /etc/group` посмотреть все группы  
* `groups` посмотреть свои группы  

почему-то FTP работает только при allIn 777


GIT
-
* `apt-get install git` установка
