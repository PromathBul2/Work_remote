# Инструкция для работы с Git и удаленными репозиториями

## Что такое Git?

Git - это одна из реализаций распределенных систем контроля версий, имеющая как и локальные, так и удаленные репозитории. Является самой популярной реализацией систем контроля версий в мире.

## Подготовка репозитория

Для создания репозитория необходимо выполнить команду _`git init`_ в папке с репозиторием и у вас создастся репозиторий (появится скрытая папка `.git`).

## Создание коммитов

### Git add

Для изменений в коммит используется команда _`git add`_. Чтобы использовать команду _`git add`_ напишите `git add <имя файла>`.

### Git commit

Для того, чтобы создать коммит (сохранение)необходимо выполнить команду _`git commit`_. Выполняется она так: `git commit -m "описание изменения"`, например `git commit -m "create new file"`.

### Git status

Для того, чтобы посмотреть состояние репозитория используется команда _`git status`_. Для этого необходимо в папке с репозиторием написать `git status` и вы увидите были ли изменения в файле.

### Git log

Чтобы посмотреть историю коммитов, используется команда _`git log`_, которая выводит список всех коммитов. У этой команды есть разные опции, самая используемая из них `--oneline`. Она показывает хеш в укороченном формате, ветку, в которой сделан коммит, а также текст коммита. Чтобы использовать эту опцию (как и любую другую), нужно добавить её после команды: `git log --oneline`.

## Работа с версиями

### Git checkout

В Git под термином _checkout_ подразумевают переключение между различными версиями целевого объекта. Команда _`git checkout`_ работает с тремя различными объектами: файлами, коммитами и ветками. Под переключением также обычно понимают действие, связанное с выполнением команды git checkout.Например, чтобы переключиться на любой другой предыдущий коммит надо выполнить команду так: `git checkout` и далее указать хотя-бы первые четыре символа хештега нужного коммита (то есть `git checkout 73ec`), затем чтобы вернуться обратно необходимо использовать команду `git checkout master` (или имя той ветки на которой вы находились перед переключением).

### Git diff

По умолчанию команда _`git diff`_ выводит все неподтвержденные изменения, внесенные после последнего коммита,сравнение файлов в двух коммитах. Команде _`git diff`_ можно передать ссылки на коммиты Git для сравнения. Возможные варианты ссылок — HEAD, теги и имена веток. Каждый коммит в Git имеет идентификатор, который можно получить с помощью команды git log.

## Создание веток

Чтобы создать новую ветку необходимо использовать команду `git branch`<name_branch>.

## Слияние веток

`git merge`<name_branch> слияние из ветки с именем указанным в команде, сливается в ветку с которым мы находимся

## Удаление веток

`git branch -d`<name_branch> - удаление слитой ветки из любой другой ветки
`git branch -D`<name_branch> - принудительное удаление ветки, даже если там есть не слитая информация.

## Отображение журнала фиксации в виде графика для текущей или всех веток

Просмотреть историю коммитов в виде графика для текущей ветки можно с помощью параметра log и флагов _--graph --oneline --decorate_. Опция _`--graph`_ выведет график в формате ASCII, отражающий структуру ветвления истории коммитов. В связке с флагами _`--oneline`_ и _`--decorate`_, этот флаг упрощает понимание того, к какой ветке относится каждый коммит.

Например:
`git log --graph --oneline --decorate`

Для просмотра истории коммитов по всем веткам используется флаг _--all_ так:

`git log --all --graph --oneline --decorate`

## Прекращение слияния при конфликте

Прервать слияние в случае конфликта можно параметром merge с флагом _`--abort`_. Он позволяет остановить процесс слияния и вернуть состояние, с которого этот процесс был начат.

`git merge --abort`

## Добавление удаленного репозитория

Добавить удалённый репозиторий можно параметром `remote add`, указав _shortname и url_ требуемого репозитория.

`git remote add` awesomeapp https://github.com/someurl..

###  