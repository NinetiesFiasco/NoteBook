package.json
-

команда `npm init` генерирует файл package.json  
Все модули желательно устанавливать с флагом --save
тогда они сохранятся в файле package.json 
и будет проще перенести проект на другой сервер

## Nodemon - приложение которое перезапускает сервер при изменении исполняемых файлов

`npm install nodemon -g`
* nodemon app.js

# Some commands

## EXPRESS - движок, помогает обрабатывать URL запросы
`npm install express`

## Handlebars - движок представлений. 
`npm install hbs`

## forever - модуль который поддерживает код без запущенной консоли
* Глобальная установка  
`$ [sudo] npm install forever -g`  
* Установка модуля в папку с проектом  
`cd /path/to/your/project`  
`$ [sudo] npm install forever-monitor`
* Установка сервиса 
`npm install -g forever-service`  

## forever-service - модуль который запускает скрипт как демон

В связке с forever помогает запускать скрипт при перезапуске системы  
`sudo forever-service install serviceName --script app.js`  
Посмотреть работающие сервисы
`forever list`

```
Commands to interact with service nodeTest  
Start   - "sudo service nodeTest start"  
Stop    - "sudo service nodeTest stop"  
Status  - "sudo service nodeTest status"  
Restart - "sudo service nodeTest restart"  
```
  
## pm2 (аналог сервиса forever)
* Запуск из консоли
`pm2 start app.js`
* Стоп в консоле
`pm2 stop app.js`
