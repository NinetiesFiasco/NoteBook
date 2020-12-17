### gh-pages пакет для nodejs для маршрутизации на gitHub pages
### Техническое описание
Пакет gh-pages, после сборки проекта `build`, публикует файлы из папки build (или указанной) в репозиторий.  
Опубликованная сборка сохраняет возможность маршрутизации.
### Подготовка
* Создать репозиторий на github
* Установить пакет локально в проект
```sh
yarn add gh-pages --save-dev
```
* Создать скрипты в package.json
```sh
"scripts": {
    "deploy": "gh-pages -d build",
    "build": "react-scripts build"
}
```

### Использование

Собрать проект
```sh
yarn build
```
Опубликовать проект
```sh
yarn deploy
```
