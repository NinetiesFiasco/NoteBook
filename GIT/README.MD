GIT
=

## Создать репозиторий
`git init`

## Загрузить репозиторий в облако
`git push -u origin master`

## Скачать репозиторий
`git clone https://github.com/NinetiesFiasco/any.git`

## Добавить файл в контроллер GIT
`git add file.txt`

## Проверка состояния
`git status`

## Создание коммита
1. `git status` - проверка изменённых файлов
1. `git add file.txt` - добавление нужных файлов в коммит по одному
1. `git commit -m "Commit Comment"` - добавление комментария к коммиту
1. `git push` - отправка в облако

## Поглядеть комиты
`git log --pretty=oneline`

#### (можно добавить автора или другие свойства для поиска)


## Создать ветку
`git checkout -b "newBranch"`

## Выбрать ветку
`git checkout newBranch`

## Подтянуть обновлённые файлы с удалённого репозитория
1. `git init`
1. `git remote add <URL to GIT>`
1. `git pull origin master`

## Глобальные данные которые попадут в комиты
`git config --global user.name "Anton Seredin"`  
`git config --global user.email "example@email.com"`

## Локальные данные которые попадут в комиты
`git config user.name "testUser"`  
`git config user.meail "test@emails@com"`

## Установка в Ubuntu
`apt-get install git`

