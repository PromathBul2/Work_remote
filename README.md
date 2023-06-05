# Work_remote
Скоро я стану, как Илон Маск...

# Временное сохранение изменений без коммита
git stash     ## временно сохранить незакоммиченные изменения и убрать их из рабочей директории  
git stash pop ## вернуть сохраненные командой git stash изменения в рабочую директорию  
# Удалённые репозитории
Есть два распространённых способа привязать удалённый репозиторий к локальному: по HTTPS и по SSH. Если SSH у вас не настроен (или вы не знаете что это), привязывайте удалённый репозиторий по HTTPS (адрес привязываемого репозитория должен начинаться с https://).

git remote -v  # показать список удалённых репозиториев, связанных с локальным  
git branch -r  # показать удаленные ветки  
git branch -a  # показать все ветки(локальные и удаленные)         
git remote remove origin   # убрать привязку удалённого репозитория с сокр. именем origin  
git remote add origin https://github.com:nicothin/test.git # добавить удалённый репозиторий (с сокр. именем origin) с указанным URL  
git remote rm origin       # удалить привязку удалённого репозитория  
git remote show origin     # получить данные об удалённом репозитории с сокращенным именем origin  
git fetch origin           # скачать все ветки с удаленного репозитория (с сокр. именем origin), но не сливать со своими ветками  
git fetch origin master    # то же, но скачивается только указанная ветка  
git checkout --track origin/github_branch # создать локальную ветку github_branch (данные взять из удалённого репозитория с сокр. именем origin, ветка github_branch) и переключиться на неё  
git push origin master     # отправить в удалённый репозиторий (с сокр. именем origin) данные своей ветки master  
git pull origin            # влить изменения с удалённого репозитория (все ветки)  
git pull origin master     # влить изменения с удалённого репозитория (только указанная ветка)  

Синхронизация репозитория-форка с мастер-репозиторием
Есть некий репозиторий на github.com, он него нами был сделан форк, добавлены какие-то изменения. Оригинальный (мастер-)репозиторий был как-то обновлён. Задача: стянуть с мастер-репозитория изменения (которые там внесены уже после того, как мы его форкнули).

# указана последовательность действий:
git remote -add upstream https://github.com:address.git # добавляем удаленный репозиторий: сокр. имя — upstream, URL мастер-репозитория  
git fetch upstream - #стягиваем все ветки мастер-репозитория, но пока не сливаем со своими  
git checkout master - #переключаемся на ветку master своего репозитория  
git merge upstream/master - #вливаем стянутую ветку master удалённого репозитория upstream в свою ветку master  