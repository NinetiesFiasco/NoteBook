Команды Ubuntu
=

Ubuntu
-

* `lsb_release -a` Узнать версию
* `sudo reboot` перезагрузка


Файлы и папки
-

`ls` просмотр каталога
`mkdir dirName` создать папку
`touch fileName.extension` создать файл

Apache
-
* sudo apachectl stop - единожды остановить сервис 
* sudo update-rc.d apache2 disable - удалить из автозагрузки

Для изменения портов можно воспользоваться консольным приложением nano  
по путям /etc/apache2/ports.conf и /etc/apache2/sites-enabled/000-default.conf
изменить порты на нужные.
Как оказалось менять порт надо было в /etc/apache2/apache2.conf

Для подключения php в том же /etc/apache2/apache2.conf указать  
```
<FilesMatch \.php$>
  SetHandler application/x-httpd-php
</FilesMatch>
```

Порты
-
* sudo netstat -ntulp -поглядеть какие порты работают
* netstat -tulpn | grep :21 - проверка работоспособности порта

Убить процесс по ID
-
`sudo kill procID' 

ПРО FTP
-
* apt-get remove vsftpd - удалялъ FTP server
* sudo apt install vsftpd - установить FTP server

[Поглядеть про FTP](https://www.unixmen.com/install-configure-ftp-server-ubuntu/ "Страница про FTP")


proftpd
-
* sudo /etc/init.d/proftpd restart - перезапуск сервиса
* //Создать пользователя  
ftpasswd --passwd --file=/etc/proftpd/ftpd.passwd --name=user --uid=34 --gid=34 --home=/var/www/user --shell=/bin/false

[Настройка PROFTPD](https://habr.com/ru/sandbox/26850/ "полная настройка")


Пользователи, группы, права
-

`sudo useradd vasyapupkin` добавить пользователя  
`id -G` id групп  
`id -Gn` или groups названия групп  
`chown root/root /var/www/user` установка прав 0_о  
`chmod 775 /var/www/user`  установка разрешений 0_о (-R рекурсивно на все подпапки)  
`su - userName` войти как пользователь  
`cat /etc/group` посмотреть все группы  
`groups` посмотреть свои группы  

почему-то FTP работает только при allIn 777


GIT
-
`apt-get install git` установка
