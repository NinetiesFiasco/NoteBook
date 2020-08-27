Установка
- 

# `sudo apt install -y mongodb` 

## Команды

# `sudo systemctl status mongodb` проверка состояния
# `sudo systemctl stop mongodb` Запуск
# `sudo systemctl start mongodb` Остановка
# `sudo systemctl reset mongodb` Перезапуск

https://www.youtube.com/watch?v=5lXVkB-yZWU&t=133s

отсюда вытащил команды

одна из команд (вроде собственно установка mongodb) попросила использовать флаг типо --use non auhtorized 

для автозапуска 

sudo systemctl enable mongodb 

именнование сервиса всегда разное(((

`show dbs` - показать все базы  
`use dbName` - использовать базу  
`show collections` - показать все коллекции  
`db.collectionName.find()` - показать содержимое коллекции
