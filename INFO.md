# QAJA8

<p><strong>git clone:</strong> Клонировать репозиторий в новую директорию</p>
<p><strong>git init:</strong> Создать новый репозиторий или перезаписать существующий</p> 
<p><strong>git add:</strong> Добавить данные</p>
<p><strong>git mv:</strong> Переместить файлы внутри репозитория</p>
<p><strong>git restore:</strong> Восстановить изменения</p>
<p><strong>git diff:</strong> Отобразить изменения коммитов</p>
<p><strong>git log:</strong> Показать историю коммитов</p>
<p><strong>git status:</strong> Показать статус файлов</p>
<p><strong>git commit:</strong> Записать изменения в репозитории</p>
<p><strong>git commit -am <em>имя файла</em></strong>:</strong> Записать изменения в репозитории с названием коммита</p>
<p><strong>git stash:</strong> Скрыть сделанные изменения</p>
<p><strong>vim <em>имя файла</em>:</strong> Создать файл</p>
<p><strong>vi <em>имя файла</em>:</strong> Редактировать файл</p>
<p><strong>git branch:</strong> Показать существующие ветки, создать новую ветку</p>
<p><strong>git checkout/-b:</strong> Переключиться на другую ветку/Создать новую ветку и переключиться на нее</p>
Last login: Thu Aug 26 22:12:00 on ttys001

ls
vim test-file
git add .
git status
git commit -am "new file created"
git status
git checkout -b
git checkout -b 15-4-feature-1
git status
vi test-file
git add .
git commit -am "text changed"
git status
git checkout -b 15-4-feature-2
vi test-file
git commit -am "changed text"
git status
git checkout -b 15-4-feature-3
vi test-file
git commit -am "mistakes corrected" 
git status
git push origin 15-4-feature-3
git push origin 15-4-feature-2
git push origin 15-4-feature-1
k$ git checkout main
k$ git merge 15-4-feature-1
git diff 15-4-feature-2
git merge 15-4-feature-2
git merge 15-4-feature-3
git status
git push origin main
git status
git commit
git status
git push origin main
