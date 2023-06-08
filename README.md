# Инструкция по работе с удаленным репозиторием
## 1. Подключение удаленного репозитория
Команда `git remote add` добавляет удаленный репозиторий к вашему локальному. 

`git remote add` <название удаленного репозитория> <ссылка на удаленный репозиторий>
 
 Имя удаленного репозитория в команде `git remote add` вы можете придумать сами. 

 Ссылку можно взять, нажав на большую зеленую кнопку Code на странице репозитория на GitHub.
 ## 2. Отключение удаленного репозитория от локального
Команда `git remote remove` - удаляет подключение вашего репозитория к удаленному. 

`git remote add` <название удаленного репозитория> 
 ## 3. Клонирование удаленного репозитория
 Команда `git clone` позволяет клонировать существующий удаленный репозиторий. Операция клонирования создаёт на вашем компьютере точную копию удаленного репозитория.
 
 `git clone` <ссылка на удаленный репозиторий>
## 4. Получение изменений из удаленного репозитория
Команда `git pull` позволяет получить изменения из удаленного репозитория и обновить свою рабочую копию. По умолчанию слияние удаленной ветки с локальной происходит в fast-forward режиме.
По сути это `git pull` - это то же самое, что `git fetch` + `git merge`. 

Команда `git fetch` используется для синхронизации локальных ссылочных объектов с этими же объектами в удаленном репозитории. Рабочую копию она не меняет.
Чтобы синхронизировать локальную рабочую копию с удаленным репозиторием, нужно слить удаленные ветки в локальные. Сделать это можно командой `git merge`.
## 5. Отправка изменений в удаленный репозиторий. 
Команда `git push` загружает изменения в удаленный репозиторий. 
## 6. Создание форка репозитория на GitHub
Форк  – точная копия репозитория, но в вашем аккаунте. Форки нужны, чтобы вносить свои изменения в проект, к репозиторию которого у вас нет прямого доступа.