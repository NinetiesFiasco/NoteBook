#MySQL

Если установка через wizzard, то при первом запуске стоит назначить пароль на root  
гайд есть на главном сайте mysql  
Создать файл `C:\\sql\init.txt` с sql запросом:  
`ALTER USER 'root'@'localhost' IDENTIFIED BY 'MyNewPass';`

В PowerShell  
```
cd "C:\Program Files\MySQL\MySQL Server 8.0\bin"
.\mysqld --defualts-file="C:\\ProgramData\\MySQL\\MySQL Server 8.0\\my.ini" --init-file=C:\\sql\init.txt
```

mysql запросы: 
* Добавить нового пользователя и подарить ему все права
```
CREATE USER 'user'@'localhost' IDENTIFIED BY 'pass';

GRANT ALL PRIVILEGES ON * . * TO 'user'@'localhost';

FLUSH PRIVILEGES;
```
