Установка
-

## Установка Node JS

* `sudo apt update` - Обновление пакетов
* `sudo apt upgrade` - Установка обновлений
* `sudo apt install curl` - Позволит соединиться с сайтом node и подтянуть нужную версию
* `curl -sL https://deb.nodesource.com/setup_current.x | sudo -E bash -` - подтянуть текущую версию (current) пакета nodejs
* `sudo apt install nodejs` - Установить nodejs


### `https://github.com/nodesource/distributions` - Описание установки нужной версии

## Установка Yarn
* `https://classic.yarnpkg.com/en/docs/install/#debian-stable` - Официальный сайт

### Установка pm2

* `npm install pm2@latest -g` - глобальная установка
* `pm2 start script.js` - запуск скрипта script.js
* `pm2 [list|ls|status]` - посмотреть все рабочие скрипты
* `pm2 startup` - запускать pm2 при загрузке системы
* `pm2 save` - сохранить текущий лист для перезагрузки
