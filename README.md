# Working with the remote repository, description of the instructions
1. Создал новую папку, командой `git init` инициализировал новый репозиторий.  
2. Командой `git branch -M main` переименовали ветку master в ветку main.  
3. Связали локальный репозитори с форком командой `git remote add origin`
4. Командой `git remote -v` проверили связку.  
5. Командой `git pull origin main` вытягиваем информацию с удаленного репозитория на свой локальный. (не клонируем)
6. Командой `git branch Home_work` создали дополнительную ветку. Для выполнения Домашнего задания.
7. Командой `git checkout Home_work` перешли на ветку
Home_work.  
8. Команда `git push` Позволяет отправить свою версию репозитория во внешний репозиторий.  
9. Команда  `pull request` - команда для предложения изменений, запрос на вливание изменений в репозиторий. На сайте Github нажимаем кнопку pull request.   
P.S. `git push --set-upstream origin`