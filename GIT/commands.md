GIT
=


## Установка в Ubuntu
`apt-get install git`

## Создать репозиторий
`git init`

## Глобальные данные которые попадут в комиты
`git config --global user.name "Anton Seredin"`  
`git config --global user.email "example@email.com"`

## Локальные данные которые попадут в комиты
`git config user.name "testUser"`  
`git config user.meail "test@emails@com"`

## Добавить файл в контроллер GIT
`git add file.txt`

## Проверка состояния
`git status`

## Поглядеть комиты
`git log --pretty=oneline`
#### (можно добавить автора или другие свойства для поиска)

## Скачать репозиторий
`git clone https://github.com/NinetiesFiasco/any.git`

## Создать ветку
`git checkout -b "newBranch"`


## Выбрать ветку
`git checkout newBranch`

## Загрузить репозиторий
`git push -u origin master`

## Подтянуть обновлённые файлы с удалённого репозитория
1. `git init`
1. `git remote add <URL to GIT>`
1. `git pull origin master`
