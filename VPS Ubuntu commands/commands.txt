Здесь будут храниться команды для Ubuntu

/*
* Apache
*/
sudo apachectl stop - единожды остановить сервис 
sudo update-rc.d apache2 disable - удалить из автозагрузки


/*
* Порты
*/
sudo netstat -ntulp -поглядеть какие порты работают
netstat -tulpn | grep :21 - проверка работоспособности порта


/*
* ПРО FTP
*/
apt-get remove vsftpd - удалялъ FTP server
sudo apt install vsftpd - установить FTP server
поглядеть про FTP https://www.unixmen.com/install-configure-ftp-server-ubuntu/

/*
* proftpd
*/
sudo /etc/init.d/proftpd restart - перезапуск сервиса
//Создать пользователя 
ftpasswd --passwd --file=/etc/proftpd/ftpd.passwd --name=user --uid=34 --gid=34 --home=/var/www/user --shell=/bin/false

https://habr.com/ru/sandbox/26850/ - полная настройка

/*
* Пользователи
*/
sudo useradd vasyapupkin - добавить пользователя
id -G   id групп
id -Gn или groups названия групп
chown root/root /var/www/user   -установка прав 0_о
chmod 775 /var/www/user   -установка разрешений 0_о (-R рекурсивно на все подпапки)

/*
* Ubuntu
*/
sudo reboot - перезагрузка

/*
* GIT
*/
apt-get install git - установка
