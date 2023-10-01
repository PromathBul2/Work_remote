# Проект "Мой удивительный проект"
## Работа с Git
git init - добавляет окружение git в папку
git status - статус репозитория
git remote add origin https://github.com/recpi2008/Git.git - соединяем папку с репозиторием
git remote -v  - показывает список remote соединений

git add Git.TXT - добавляем файл
git add .  - добавить рекурсия файлов
git rm --cached Git.TXT - если ошиблись(удалить)
git commit - добавляем коммит (в редакторе i текст esc :wq)
git commit -m'text'  - чтобы не открывать редактор
git commit -am 'updated Git.RTF' - сразу все делаем

touch images/.gitkeep - добавление пустых папок
touch .gitignore - добавление игнора файлов

git log - просмотр истории репозитория
git log --oneline  - сокращенная выписка
git reset a155ea6 - откатиться к commit
git reflog - инфо обо всех изменениях
git revert a155ea6 - отменяет действие commit

git branch   - смотрим доступные ветки
git branch name  - создаем новую ветку
git checkout dev - переключаемся на ветку
git branch dev_2 master - создаем ветку из ветки
git checkout -b dev_3 - создание ветки с переключением на нее



ssh-keygen - создать ключ
git clone ссылка_ssh name_directory - клонируем репозиторий в указаннаю папку
git push - кладем в GitHub изменения
git push -u origin dev - если push в несозданную ветку
git pull - изменения из Github в папку

git fetch - обновляет ветки из репозотория в папке
git merge name_dev - вливает изменения в ветку мастер, после этого git push
git branch -d name_dev - удаляем ветку, после этого git push
git push --delete origin name_dev - удаляем ветки из Github



REBASE
git rebase main - 
git push --force - подтверждаем



Версии:
git tag 1.0.0 - записываем версию
git tag - смотрим версии
git tag --list - смотрим все версии
git push --tag - загружаем push версии
git tag -d 1.0.1 - удаляем тэг
git push --delete origin 1.0.1 - удаляем тэг из удаленного репозитория


## Описание проекта
Этот проект создан для того, чтобы продемонстрировать разные возможности форматирования в Markdown.


