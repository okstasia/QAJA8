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

The default interactive shell is now zsh.
To update your account to use zsh, please run `chsh -s /bin/zsh`.
For more details, please visit https://support.apple.com/kb/HT208050.
MacBook-Pro:qaja8 k$ ды
-bash: ды: command not found
MacBook-Pro:qaja8 k$ ls
INFO.md			file-feature-1.txt	file-feature.txt
QAJA8			file-feature-2.txt
MacBook-Pro:qaja8 k$ vim test-file
MacBook-Pro:qaja8 k$ git add .
MacBook-Pro:qaja8 k$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   test-file

MacBook-Pro:qaja8 k$ git commit -am "new file created"
[main 684ea34] new file created
 1 file changed, 6 insertions(+)
 create mode 100644 test-file
MacBook-Pro:qaja8 k$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
MacBook-Pro:qaja8 k$ git checkout -b
error: switch `b' requires a value
MacBook-Pro:qaja8 k$ git checkout -b 15-4-feature-1
Switched to a new branch '15-4-feature-1'
MacBook-Pro:qaja8 k$ git status
On branch 15-4-feature-1
nothing to commit, working tree clean
MacBook-Pro:qaja8 k$ vi test-file
MacBook-Pro:qaja8 k$ git add .
MacBook-Pro:qaja8 k$ git commit -am "text changed"
[15-4-feature-1 4069521] text changed
 1 file changed, 2 insertions(+), 1 deletion(-)
MacBook-Pro:qaja8 k$ git status
On branch 15-4-feature-1
nothing to commit, working tree clean
MacBook-Pro:qaja8 k$ git checkout -b 15-4-feature-2
Switched to a new branch '15-4-feature-2'
MacBook-Pro:qaja8 k$ vi test-file
MacBook-Pro:qaja8 k$ git add.
git: 'add.' is not a git command. See 'git --help'.

The most similar command is
	add
MacBook-Pro:qaja8 k$ git commit -am "changed text"
[15-4-feature-2 343b08d] changed text
 1 file changed, 1 insertion(+)
MacBook-Pro:qaja8 k$ git status
On branch 15-4-feature-2
nothing to commit, working tree clean
MacBook-Pro:qaja8 k$ git checkout -b 15-4-feature-3
Switched to a new branch '15-4-feature-3'
MacBook-Pro:qaja8 k$ vi test-file
MacBook-Pro:qaja8 k$ git add.
git: 'add.' is not a git command. See 'git --help'.

The most similar command is
	add
MacBook-Pro:qaja8 k$ git commit -am "mistakes corrected" 
[15-4-feature-3 a177ca9] mistakes corrected
 1 file changed, 1 insertion(+), 1 deletion(-)
MacBook-Pro:qaja8 k$ git status
On branch 15-4-feature-3
nothing to commit, working tree clean
MacBook-Pro:qaja8 k$ git push origin 15-4-feature-3
Enumerating objects: 22, done.
Counting objects: 100% (21/21), done.
Delta compression using up to 4 threads
Compressing objects: 100% (18/18), done.
Writing objects: 100% (18/18), 3.08 KiB | 1.54 MiB/s, done.
Total 18 (delta 10), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (10/10), completed with 2 local objects.
remote: 
remote: Create a pull request for '15-4-feature-3' on GitHub by visiting:
remote:      https://github.com/okstasia/QAJA8/pull/new/15-4-feature-3
remote: 
To https://github.com/okstasia/QAJA8.git
 * [new branch]      15-4-feature-3 -> 15-4-feature-3
MacBook-Pro:qaja8 k$ git push origin 15-4-feature-2
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for '15-4-feature-2' on GitHub by visiting:
remote:      https://github.com/okstasia/QAJA8/pull/new/15-4-feature-2
remote: 
To https://github.com/okstasia/QAJA8.git
 * [new branch]      15-4-feature-2 -> 15-4-feature-2
MacBook-Pro:qaja8 k$ git push origin 15-4-feature-1
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for '15-4-feature-1' on GitHub by visiting:
remote:      https://github.com/okstasia/QAJA8/pull/new/15-4-feature-1
remote: 
To https://github.com/okstasia/QAJA8.git
 * [new branch]      15-4-feature-1 -> 15-4-feature-1
MacBook-Pro:qaja8 k$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)
MacBook-Pro:qaja8 k$ git merge 15-4-feature-1
Updating 684ea34..4069521
Fast-forward
 test-file | 3 ++-
 1 file changed, 2 insertions(+), 1 deletion(-)
MacBook-Pro:qaja8 k$ git diff 15-4-feature-2
diff --git a/test-file b/test-file
index 3a2f6cc..b7d6602 100644
--- a/test-file
+++ b/test-file
@@ -1,7 +1,6 @@
 В ветке два поменяйте первый абзац текста, а в ветке три отредактируйте второй абзац. Если вы работаете с кодом, то меняйте одинаковые блоки кода.
 Снова переключитесь на мастер и добавьте новый текст перед первым абзацем (или комментарий к коду), а второй абзац удалите.
 Создайте три ветки в вашем репозитории (например, 15-4-feature-1, 15-4-feature-2, 15-4-feature-3). Сделайте в них конфликтующие изменения, например: в ветке один и ветке два поменяйте первый абзац текста, а в ветке три отредактируйте второй абзац. Если вы работаете с кодом, то меняйте одинаковые блоки кода.
-В ветке два поменяйте первый абзац текста, а в ветке три отредактируйте второй абзац. 
 Отправьте все ветки в ваш репозиторий на Github. 
 Поочерёдно объедините изменения с веткой master (помните, что это — ваша главная ветка и, если не уверены в результате мёрджа, откатите его и сделайте снова). Отправьте master со всеми объединёнными изменениями на Github (команда git push origin master).
 Постарайтесь записать все выполненные вами команды в отдельный файл INFO.md и отдельным коммитом сохраните его в ветке master. Ещё раз отправьте master на Github.
MacBook-Pro:qaja8 k$ 
MacBook-Pro:qaja8 k$ 
MacBook-Pro:qaja8 k$ git merge 15-4-feature-2
Updating 4069521..343b08d
Fast-forward
 test-file | 1 +
 1 file changed, 1 insertion(+)
MacBook-Pro:qaja8 k$ git merge 15-4-feature-3
Updating 343b08d..a177ca9
Fast-forward
 test-file | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)
MacBook-Pro:qaja8 k$ git status
On branch main
Your branch is ahead of 'origin/main' by 4 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
MacBook-Pro:qaja8 k$ git push origin main
To https://github.com/okstasia/QAJA8.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/okstasia/QAJA8.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
MacBook-Pro:qaja8 k$ git pull
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 725 bytes | 181.00 KiB/s, done.
From https://github.com/okstasia/QAJA8
   03c47ae..0bcb803  main       -> origin/main
hint: Waiting for your editor to close the file... fatal: cannot run /Applications/TextEdit.app/Contents/MacOS/TextEdit: No such file or directory
error: unable to start editor '/Applications/TextEdit.app/Contents/MacOS/TextEdit'
Not committing merge; use 'git commit' to complete the merge.
MacBook-Pro:qaja8 k$ git status
On branch main
Your branch and 'origin/main' have diverged,
and have 4 and 1 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)

All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
	modified:   INFO.md

MacBook-Pro:qaja8 k$ git commit
hint: Waiting for your editor to close the file... fatal: cannot run /Applications/TextEdit.app/Contents/MacOS/TextEdit: No such file or directory
error: unable to start editor '/Applications/TextEdit.app/Contents/MacOS/TextEdit'
Please supply the message usingit commit -am "filed edited" 
