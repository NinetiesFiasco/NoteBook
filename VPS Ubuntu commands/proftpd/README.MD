Установка
-

## Обновление системы  
  `sudo apt-get update`  
  `sudo apt-get upgrade`  
  
## Текстовый редактор  
  `sudo apt-get install nano`  
## Собственно пакет  
  `sudo apt-get install proftpd-basic`  
  
# Создаём каталог /home/ftp  
  `cd /home`  
  `sudo mkdir ftp`  
  `sudo chmod 777 ftp`  
  
## Создаём пользователей (тут user пароль запросит)  
### Создаём группу (ftpeshniki) и присваиваем ей пользователя (dimant)  
  `sudo ftpasswd --group --name=ftpeshniki --gid=50 --member=dimant --file /etc/proftpd/ftpd.group`  
### Создаём пользователя (dimant) и присваиваем ему домашнюю директорию (/home/ftp), в процессе будет запрошен пароль  
  `sudo ftpasswd --passwd --name=dimant --home=/home/ftp --shell=/bin/false --uid=1003 --file /etc/proftpd/ftpd.passwd`  


  

## Настройка proftpd  
  ### открыть файл  
  `sudo nano /etc/proftpd/proftpd.conf`  
  ### настройки  


  `AllowOverwrite            on`  
  
  `RequireValidShell         off`  
  `AuthUserFile              /etc/proftpd/ftpd.passwd`  
  `AuthGroupFile             /etc/proftpd/ftpd.group`  
   
  `UseIPv6                   off`  
  `ServerName                "ftp-server"`  
  `ServerType                standalone`  
  `DeferWelcome              on`  


  ###Эти две команды убыстряют работу сервака, гуглите для подробностей.  
  `UseReverseDNS             off`  
  `IdentLookups              off`  

  `MultilineRFC2228          on`  
  `DefaultServer             on`  
  `ShowSymlinks              off`  

  `TimeoutNoTransfer         600`  
  `TimeoutStalled            100`  
  `TimeoutIdle               2200`  
 
  `DisplayChdir              .message`  
  `ListOptions               "-l"`  
 
  `TimeoutLogin              20`  
  
  `RootLogin                 off`  

  ### Журналы  
  `ExtendedLog               /var/log/ftp.log`  
  `TransferLog               /var/log/xferlog`  
  `SystemLog                 /var/log/syslog.log`  
  
  // **** ЭТУ ШТУКУ УДАЛИТЬ ****   
  // Запрещаем заливать файлы начинающиеся с точки  
  `DenyFilter                \*.*/`  
  //****************************   
  
  
  ### Сообщение после успешного захода на сервер  
  `AccessGrantMsg            "Welcome to Server"`  
  ### Идентификатор сервера, показывается всем при заходе на сервер  
  `ServerIdent                  on       "privet :))"`  
  

  ### Устанавливаем домашний каталог  
  `DefaultRoot /home/ftp`  

  ### Запираем всех в домашнем каталоге, чтобы не могли просмотреть каталоги выше, важно для безопасности  
  `DefaultRoot ~`  
  
  
  ## Полезные команды  
  `sudo systemctl start proftpd`  
  `sudo systemctl stop proftpd`  
  `sudo systemctl restart proftpd`  

  `sudo systemctl status proftpd.service`  
  

  
