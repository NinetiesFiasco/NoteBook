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
  
  ### Настройки указаны в файле settings.md

  ### Устанавливаем домашний каталог  
  `DefaultRoot /home/ftp`  

  ### Запираем всех в домашнем каталоге, чтобы не могли просмотреть каталоги выше, важно для безопасности  
  `DefaultRoot ~`  
  
  
  ## Полезные команды  
  `sudo systemctl start proftpd`  
  `sudo systemctl stop proftpd`  
  `sudo systemctl restart proftpd`  

  `sudo systemctl status proftpd.service`  
  

  
