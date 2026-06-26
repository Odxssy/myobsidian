Для пуша коммитов директорий по типу баз из Obsidian требуется установить директорию этой папки и "положить" туда файл гита.

Вот поэтапный гайд по установке:

1. Установить git через PowerShell на PC командой :
   ==winget install --id Git.Git -e --source winget==
2. Директория не должна лежать в облаке или OneDrive, папка обязательно должна быть локальной.
3. Далее создаем репозиторий на GItHub и ==копируем ссылку== на него, после чего "проваливаемся" в папку с директорией где лежит наша база :
   cd имя_нужной_папки
   git add .
   git commit "название комита"
   git remote add origin "==ссылка на репозиторий git=="
   git push -u origin master
4. Дальше все пуши будут делаться так :
   git add .
   git commit -m "."
   git push 
5. В случае ошибки "Another git process seems to be running in this repository, or the lock file may be stale" - был создан скрипт .lock, его видно если включить отображение системных файлов или можно удалить командой del .git\index.lock
   