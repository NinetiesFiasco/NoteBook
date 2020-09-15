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

* `curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -` - Добавить репозиторий через curl
* `echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list` - что-то где-то прописать
* `sudo apt update && sudo apt install yarn` - Установить

### Установка pm2

* `npm install pm2@latest -g` - глобальная установка
* `pm2 start script.js` - запуск скрипта script.js
* `pm2 [list|ls|status]` - посмотреть все рабочие скрипты
* `pm2 startup` - запускать pm2 при загрузке системы
* `pm2 save` - сохранить текущий лист для перезагрузки
#### Внимание файл .env будет читаться из папки запуска pm2 (лучше использовать абсолютный путь для env)
