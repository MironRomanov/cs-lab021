
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021
$ mkdir alice							
										\\создали папку алисы
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021
$ mkdir bob
										\\создали папку боба
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021
$ cd alice
										\\перешли в каталог алисы
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice
$ mkdir project
										\\создали папку проекта
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice
$ cd project
										\\перешли в каталог проекта
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project
$ cd ..
										\\вернулись обратно
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice
$ cd project
										\\перешли в каталог проекта
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project
$ git init
Initialized empty Git repository in C:/Users/Админ/Desktop/lab021/alice/project/.git/
										\\инициализация репозитария
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git config user.name 'Alice (IvanovII)'
										\\вводим информацию пользователя
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git config user.email 'alice@example.com'
										\\вводим информацию пользователя
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git config user.name 'Alice (RomanovMA)'
										\\вводим информацию пользователя
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git config user.email 'miron.romanov@yandex.ru'
										\\вводим информацию пользователя
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bin/
        main.cpp
        obj/
        project.cbp

nothing added to commit but untracked files present (use "git add" to track)
										\\просматриваем статус и содержимое каталога
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git add main.cpp
										\\добавляем в список коммита код проекта
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git commit -m 'code: заготовка программы'
[master (root-commit) 4e8555c] code: заготовка программы
 1 file changed, 9 insertions(+)
 create mode 100644 main.cpp
										\\коммитим
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git add project.cbp
warning: in the working copy of 'project.cbp', LF will be replaced by CRLF the next time Git touches it
										\\добавляем в список коммита проект
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git commit -m 'build: добавлен файл проекта'
[master 91fbacf] build: добавлен файл проекта
 1 file changed, 40 insertions(+)
 create mode 100644 project.cbp
										\\коммитим
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   main.cpp
										\\смотрим статус каталога
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bin/
        obj/
        project.layout

no changes added to commit (use "git add" and/or "git commit -a")

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git add main.cpp
										\\добавляем в список коммита код проекта
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git commit -m 'code: добавлен ввод чисел'
[master 4c79937] code: добавлен ввод чисел
 1 file changed, 4 insertions(+), 2 deletions(-)
										\\коммитим
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git add -u
										\\добавляем все измененные файлы
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git commit -m 'code: добавлен вывод суммы'
[master 355c185] code: добавлен вывод суммы
 1 file changed, 1 insertion(+)
										\\коммитим
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git commit -a -m 'code: добавлен вывод разности'
[master d34c353] code: добавлен вывод разности
 1 file changed, 2 insertions(+), 1 deletion(-)
										\\то же самое
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
        obj/
        project.layout
										\\смотрим статус при созданном гитигноре
nothing added to commit but untracked files present (use "git add" to track)

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
        project.layout
										\\обновили список игнорирования и смотрим статус
nothing added to commit but untracked files present (use "git add" to track)

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git add .gitignore
										\\коммитим гитигнор
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git commit -m 'git: создан файл игнорирования'
[master 301e19d] git: создан файл игнорирования
 1 file changed, 2 insertions(+)
 create mode 100644 .gitignore

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git log --stat
commit 301e19d716c7a40cff7ea252975d063c2a48dd21 (HEAD -> master)
Author: Alice (RomanovMA) <miron.romanov@yandex.ru>
Date:   Sun Mar 26 23:15:00 2023 +0300
										\\просматриваем все коммиты
    git: создан файл игнорирования

 .gitignore | 2 ++
 1 file changed, 2 insertions(+)

commit d34c3539dbf52c3b9911f6fba939b3e6c93f0dd1
Author: Alice (RomanovMA) <miron.romanov@yandex.ru>
Date:   Sun Mar 26 23:11:12 2023 +0300

    code: добавлен вывод разности

 main.cpp | 3 ++-
 1 file changed, 2 insertions(+), 1 deletion(-)

commit 355c185f8b4750d669555bc42a25aaf36a16b118
Author: Alice (RomanovMA) <miron.romanov@yandex.ru>
Date:   Sun Mar 26 23:09:55 2023 +0300

    code: добавлен вывод суммы


Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git log --oneline --decorate
301e19d (HEAD -> master) git: создан файл игнорирования
d34c353 code: добавлен вывод разности
355c185 code: добавлен вывод суммы
4c79937 code: добавлен ввод чисел
91fbacf build: добавлен файл проекта
4e8555c code: заготовка программы
										\\просматриваем коммиты кратко и красиво
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git log --oneline --decorate --all --graph
* 301e19d (HEAD -> master) git: создан файл игнорирования
* d34c353 code: добавлен вывод разности
* 355c185 code: добавлен вывод суммы
* 4c79937 code: добавлен ввод чисел
* 91fbacf build: добавлен файл проекта
* 4e8555c code: заготовка программы
										\\то же самое
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git log -- main.cpp
commit d34c3539dbf52c3b9911f6fba939b3e6c93f0dd1
Author: Alice (RomanovMA) <miron.romanov@yandex.ru>
Date:   Sun Mar 26 23:11:12 2023 +0300
										\\смотрим коммиты связанные с кодом проекта
    code: добавлен вывод разности

commit 355c185f8b4750d669555bc42a25aaf36a16b118
Author: Alice (RomanovMA) <miron.romanov@yandex.ru>
Date:   Sun Mar 26 23:09:55 2023 +0300

    code: добавлен вывод суммы

commit 4c7993795756ac83d66437c2e0276a60ac4b4702
Author: Alice (RomanovMA) <miron.romanov@yandex.ru>
Date:   Sun Mar 26 23:08:23 2023 +0300

    code: добавлен ввод чисел

commit 4e8555cb014708e3ba60c28c4661aea8a1157e7c
Author: Alice (RomanovMA) <miron.romanov@yandex.ru>
Date:   Sun Mar 26 23:04:54 2023 +0300

    code: заготовка программы

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git log --grep 'build:'
commit 91fbacfa86c80465020b3e22102c1c35c5cb6517
Author: Alice (RomanovMA) <miron.romanov@yandex.ru>
Date:   Sun Mar 26 23:06:07 2023 +0300
										\\смотрим коммиты со совом build внутри
    build: добавлен файл проекта

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git log -- project.cbp
commit 91fbacfa86c80465020b3e22102c1c35c5cb6517
Author: Alice (RomanovMA) <miron.romanov@yandex.ru>
Date:   Sun Mar 26 23:06:07 2023 +0300

    build: добавлен файл проекта

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git show HEAD
commit 301e19d716c7a40cff7ea252975d063c2a48dd21 (HEAD -> master)
Author: Alice (RomanovMA) <miron.romanov@yandex.ru>
Date:   Sun Mar 26 23:15:00 2023 +0300

    git: создан файл игнорирования

diff --git a/.gitignore b/.gitignore
new file mode 100644
index 0000000..4c7473d
--- /dev/null
+++ b/.gitignore
@@ -0,0 +1,2 @@
+/bin
+/obj

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git show master
commit 301e19d716c7a40cff7ea252975d063c2a48dd21 (HEAD -> master)
Author: Alice (RomanovMA) <miron.romanov@yandex.ru>
Date:   Sun Mar 26 23:15:00 2023 +0300
										\\смотрим коммиты связанные с нашей веткой
    git: создан файл игнорирования

diff --git a/.gitignore b/.gitignore
new file mode 100644
index 0000000..4c7473d
--- /dev/null
+++ b/.gitignore
@@ -0,0 +1,2 @@
+/bin
+/obj

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git show HEAD~1
commit d34c3539dbf52c3b9911f6fba939b3e6c93f0dd1
Author: Alice (RomanovMA) <miron.romanov@yandex.ru>
Date:   Sun Mar 26 23:11:12 2023 +0300
										\\смотрим предпоследний коммит
    code: добавлен вывод разности

diff --git a/main.cpp b/main.cpp
index ba43a3a..1890198 100644
--- a/main.cpp
+++ b/main.cpp
@@ -7,6 +7,7 @@ int main()
        cout << "Enter A and B: ";
        int a, b;
        cin >> a >> b;
-       cout << "A + B = " << a + b << '\n';
+       cout << "A + B = " << a + b << '\n'
+            << "A - B = " << a - b << '\n';
        return 0;
 }

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git show master~1
commit d34c3539dbf52c3b9911f6fba939b3e6c93f0dd1
Author: Alice (RomanovMA) <miron.romanov@yandex.ru>
Date:   Sun Mar 26 23:11:12 2023 +0300
										\\смотрим предпоследний коммит связанный с нашей веткой
    code: добавлен вывод разности

diff --git a/main.cpp b/main.cpp
index ba43a3a..1890198 100644
--- a/main.cpp
+++ b/main.cpp
@@ -7,6 +7,7 @@ int main()
        cout << "Enter A and B: ";
        int a, b;
        cin >> a >> b;
-       cout << "A + B = " << a + b << '\n';
+       cout << "A + B = " << a + b << '\n'
+            << "A - B = " << a - b << '\n';
        return 0;
 }

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git show d34c3539dbf52c3b9911f6fba939b3e6c93f0dd1
commit d34c3539dbf52c3b9911f6fba939b3e6c93f0dd1
Author: Alice (RomanovMA) <miron.romanov@yandex.ru>
Date:   Sun Mar 26 23:11:12 2023 +0300
										\\смотрим коммит по хэшу
    code: добавлен вывод разности

diff --git a/main.cpp b/main.cpp
index ba43a3a..1890198 100644
--- a/main.cpp
+++ b/main.cpp
@@ -7,6 +7,7 @@ int main()
        cout << "Enter A and B: ";
        int a, b;
        cin >> a >> b;
-       cout << "A + B = " << a + b << '\n';
+       cout << "A + B = " << a + b << '\n'
+            << "A - B = " << a - b << '\n';
        return 0;
 }

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git diff
diff --git a/main.cpp b/main.cpp
index 1890198..4203289 100644
--- a/main.cpp
+++ b/main.cpp
@@ -8,6 +8,7 @@ int main()
        int a, b;
        cin >> a >> b;
        cout << "A + B = " << a + b << '\n'
-            << "A - B = " << a - b << '\n';
+            << "A - B = " << a - b << '\n'
+            << "A * B = " << a * b << '\n';
        return 0;
 }
											\\смотрим список изменений
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git diff HEAD~2
diff --git a/.gitignore b/.gitignore
new file mode 100644
index 0000000..4c7473d
--- /dev/null
+++ b/.gitignore
@@ -0,0 +1,2 @@
+/bin
+/obj
diff --git a/main.cpp b/main.cpp
index ba43a3a..4203289 100644
--- a/main.cpp
+++ b/main.cpp
@@ -7,6 +7,8 @@ int main()
        cout << "Enter A and B: ";
        int a, b;
        cin >> a >> b;
-       cout << "A + B = " << a + b << '\n';
+       cout << "A + B = " << a + b << '\n'
+            << "A - B = " << a - b << '\n'
+            << "A * B = " << a * b << '\n';
        return 0;
 }
										\\смотрим кол-во изменений до предпредпоследнего коммита
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git diff HEAD~1 HEAD
diff --git a/.gitignore b/.gitignore
new file mode 100644
index 0000000..4c7473d
--- /dev/null
+++ b/.gitignore
@@ -0,0 +1,2 @@
+/bin
+/obj
										\\кол-во изменений между последним и прдпоследнима коммитом
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git diff 4e8555c HEAD~1
diff --git a/main.cpp b/main.cpp
index b4392ec..1890198 100644
--- a/main.cpp
+++ b/main.cpp
@@ -4,6 +4,10 @@ using namespace std;
										\\изменения между первым и предпоследним коммитом
 int main()
 {
-    cout << "Hello world!" << endl;
-    return 0;
+       cout << "Enter A and B: ";
+       int a, b;
+       cin >> a >> b;
+       cout << "A + B = " << a + b << '\n'
+            << "A - B = " << a - b << '\n';
+       return 0;
 }
diff --git a/project.cbp b/project.cbp
new file mode 100644
index 0000000..99bb702
--- /dev/null
+++ b/project.cbp
@@ -0,0 +1,40 @@

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   main.cpp
										\\смотрим статус
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        project.layout

no changes added to commit (use "git add" and/or "git commit -a")

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git add main.cpp

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git commit -m 'code: добавлен вывод произведения'
[master 1346289] code: добавлен вывод произведения
 1 file changed, 2 insertions(+), 1 deletion(-)
										\\коммитим код проекта
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git reset --hard HEAD~1
HEAD is now at 301e19d git: создан файл игнорирования
									\\удаляем коммит проекта и восстанавливаем до предыдущей версии
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git checkout HEAD -- main.cpp
									\\возвращаем до код до версии последнего коммита
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ ssh-keygen								\\создаем ключ
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/Админ/.ssh/id_rsa):
/c/Users/Админ/.ssh/id_rsa already exists.
Overwrite (y/n)? y
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/Users/Админ/.ssh/id_rsa
Your public key has been saved in /c/Users/Админ/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:2av3syj5BbVkM3stWylkU1/kUKZYGOnz8XbQV+aUHp0 Админ@DESKTOP-2C28JPJ
The key's randomart image is:
+---[RSA 3072]----+
|            .+o+O|
|            oo.EB|
|           .B+o==|
|         o +==+o=|
|        S o o+o=+|
|           o .o++|
|         .. . ...|
|        o..o.    |
|        .+o.oo   |
+----[SHA256]-----+

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ eval `ssh-agent -s`
Agent pid 1302
									\\создаем агента чтобы не вводить пароль кучу раз
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ ssh-add
Enter passphrase for /c/Users/Админ/.ssh/id_rsa:
Identity added: /c/Users/Админ/.ssh/id_rsa (Админ@DESKTOP-2C28JPJ)
									\\добавляем публичный ключ 
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ cat ~/.ssh/id_rsa.pub
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDOaCVBc2MmMwhtcHhT/qLYx0RgxYCK4bErcCLA39Y/tRfp6VkyvQ7bBkQ/tJvrSdiUfMA45r8p6bZsHPPcqqfp1nGftRxMQ4zfH0ZGB0Pj14Qu9wLKYvIyVew2k1PQW7Ktkk2vcZbJvsGVQ47d6Zv+DCHeyV30yu/ji/BU2SHidrx5Hr2Gddug5Ai3MK3w2ltuL7XaQN0ci+0N1eM9AglPBHy/R3bcRNkN2Cf/iyE1iSA9fjrR+RLf4M9KZZvCN0KdZUmmixrfwH3tg+7dcl3bWdNIIMcXIF77lew8rMijxOTYufzX/NirC+OZP990VPSTt61yCabAGIzweA48gqb1AHbq361CHy7hfHIzwl76akhdXJQdfSBFB/TQDnkKg67SrWXcJJthp0/Esu+TOqEMvkk1k/DGbj16WUgjNogWtVn4tFzMw8oKilhUqg8USQG7KlZBj7liUn4FO4Gx2i3OTFvzHvgwyT3KdP8mtvPMg0J9nFUTbn6Lkb1CROigrz0= Админ@DESKTOP-2C28JPJ
									\\выводим его
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (master)
$ git remote add origin git@github.com:MironRomanov/cs-lab021.git
git branch -M main
git push -u origin main							\\привязываем к нашему гиту
Enumerating objects: 18, done.
Counting objects: 100% (18/18), done.
Delta compression using up to 16 threads
Compressing objects: 100% (16/16), done.
Writing objects: 100% (18/18), 2.38 KiB | 2.38 MiB/s, done.
Total 18 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), done.
To github.com:MironRomanov/cs-lab021.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob
$ git clone  git@github.com:MironRomanov/cs-lab021.git project
Cloning into 'project'...						\\клонируем проект для боба
Enter passphrase for key '/c/Users/Админ/.ssh/id_rsa':
remote: Enumerating objects: 18, done.
remote: Counting objects: 100% (18/18), done.
remote: Compressing objects: 100% (14/14), done.
remote: Total 18 (delta 2), reused 18 (delta 2), pack-reused 0
Receiving objects: 100% (18/18), done.
Resolving deltas: 100% (2/2), done.

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob
$ cd project
									\\переходим в каталог проекта
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main)
$ git config user.name 'Bob (The Builder)'

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main)
$ git config user.email 'bobthebuilder@example.com'
									\\добавляем информацию о пользователе
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.
									\\смотрим статус проекта
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   main.cpp

no changes added to commit (use "git add" and/or "git commit -a")

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main)
$ git add main.cpp

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main)
$ git commit -m 'code: добавлен вывод произведения'
[main f731c82] code: добавлен вывод произведения
 1 file changed, 2 insertions(+), 1 deletion(-)
									\\коммитим
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main)
$ git push
Enter passphrase for key '/c/Users/Админ/.ssh/id_rsa':
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 422 bytes | 422.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0			\\переносим коммит и изменения на гит
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:MironRomanov/cs-lab021.git
   301e19d..f731c82  main -> main

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git fetch								\\синхронизируем проект с новыми изменениями
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 1), reused 3 (delta 1), pack-reused 0
Unpacking objects: 100% (3/3), 402 bytes | 134.00 KiB/s, done.
From github.com:MironRomanov/cs-lab021
   301e19d..f731c82  main       -> origin/main

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git log --oneline --decorate --all --graph				\\смотрим коммиты
* f731c82 (origin/main) code: добавлен вывод произведения
* 301e19d (HEAD -> main) git: создан файл игнорирования
* d34c353 code: добавлен вывод разности
* 355c185 code: добавлен вывод суммы
* 4c79937 code: добавлен ввод чисел
* 91fbacf build: добавлен файл проекта
* 4e8555c code: заготовка программы

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git pull --ff-only
Updating 301e19d..f731c82
Fast-forward								\\переносим отстающую ветку к новым коммитам
 main.cpp | 3 ++-
 1 file changed, 2 insertions(+), 1 deletion(-)

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git log --oneline --decorate --all --graph
* f731c82 (HEAD -> main, origin/main) code: добавлен вывод произведения
* 301e19d git: создан файл игнорирования				\\смотрим коммиты
* d34c353 code: добавлен вывод разности
* 355c185 code: добавлен вывод суммы
* 4c79937 code: добавлен ввод чисел
* 91fbacf build: добавлен файл проекта
* 4e8555c code: заготовка программы

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git add main.cpp

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git commit -m 'code: добавлен вывод деления'
[main e61d869] code: добавлен вывод деления
 1 file changed, 2 insertions(+), 1 deletion(-)
									\\коммитим
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.					\\переносим изменения на гит
Writing objects: 100% (3/3), 434 bytes | 434.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:MironRomanov/cs-lab021.git
   f731c82..e61d869  main -> main

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main)
$ git fetch								\\синхронизируем проект
Enter passphrase for key '/c/Users/Админ/.ssh/id_rsa':
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 1), reused 3 (delta 1), pack-reused 0
Unpacking objects: 100% (3/3), 414 bytes | 103.00 KiB/s, done.
From github.com:MironRomanov/cs-lab021
   f731c82..e61d869  main       -> origin/main

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main)
$ git log --oneline --decorate --all --graph				\\смотрим коммиты и графы
* e61d869 (origin/main, origin/HEAD) code: добавлен вывод деления
* f731c82 (HEAD -> main) code: добавлен вывод произведения
* 301e19d git: создан файл игнорирования
* d34c353 code: добавлен вывод разности
* 355c185 code: добавлен вывод суммы
* 4c79937 code: добавлен ввод чисел
* 91fbacf build: добавлен файл проекта
* 4e8555c code: заготовка программы

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main)
$ git pull --ff-only							\\переносим отстающую ветку наверх к новым коммитам
Enter passphrase for key '/c/Users/Админ/.ssh/id_rsa':
Updating f731c82..e61d869
Fast-forward
 main.cpp | 3 ++-
 1 file changed, 2 insertions(+), 1 deletion(-)

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main)
$ git log --oneline --decorate --all --graph
* e61d869 (HEAD -> main, origin/main, origin/HEAD) code: добавлен вывод деления
* f731c82 code: добавлен вывод произведения
* 301e19d git: создан файл игнорирования
* d34c353 code: добавлен вывод разности
* 355c185 code: добавлен вывод суммы
* 4c79937 code: добавлен ввод чисел
* 91fbacf build: добавлен файл проекта
* 4e8555c code: заготовка программы

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git add main.cpp

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git commit -m 'code: добавлен вывод максимума'
[main 5732294] code: добавлен вывод максимума
 1 file changed, 3 insertions(+), 2 deletions(-)
											\\коммитим
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 468 bytes | 468.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:MironRomanov/cs-lab021.git
   e61d869..5732294  main -> main
											\\переносим на гит
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main)
$ git add main.cpp

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main)
$ git commit -m 'code: добавлен вывод минимума'
[main 084d925] code: добавлен вывод минимума
 1 file changed, 3 insertions(+), 2 deletions(-)
											\\коммитим
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main)
$ git push
Enter passphrase for key '/c/Users/Админ/.ssh/id_rsa':
To github.com:MironRomanov/cs-lab021.git						\\пытаемся перенести на гит, но выходит ошибка
 ! [rejected]        main -> main (fetch first)						\\из-за разных версий проекта
error: failed to push some refs to 'github.com:MironRomanov/cs-lab021.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main)
$ git fetch										\\синхронизируем проект
Enter passphrase for key '/c/Users/Админ/.ssh/id_rsa':
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 1), reused 3 (delta 1), pack-reused 0
Unpacking objects: 100% (3/3), 448 bytes | 89.00 KiB/s, done.
From github.com:MironRomanov/cs-lab021
   e61d869..5732294  main       -> origin/main

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main)
$ git log --oneline --decorate --all --graph						\\видим разветвление
* 084d925 (HEAD -> main) code: добавлен вывод минимума
| * 5732294 (origin/main, origin/HEAD) code: добавлен вывод максимума
|/
* e61d869 code: добавлен вывод деления
* f731c82 code: добавлен вывод произведения
* 301e19d git: создан файл игнорирования
* d34c353 code: добавлен вывод разности
* 355c185 code: добавлен вывод суммы
* 4c79937 code: добавлен ввод чисел
* 91fbacf build: добавлен файл проекта
* 4e8555c code: заготовка программы

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main)
$ git rebase origin/main
Auto-merging main.cpp									\\переносим наш коммит выше прошлого
CONFLICT (content): Merge conflict in main.cpp
error: could not apply 084d925... code: добавлен вывод минимума
hint: Resolve all conflicts manually, mark them as resolved with
hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".	\\не получается, ошибка в коде
Could not apply 084d925... code: добавлен вывод минимума

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main|REBASE 1/1)
$ git status
interactive rebase in progress; onto 5732294
Last command done (1 command done):
   pick 084d925 code: добавлен вывод минимума
No commands remaining.
You are currently rebasing branch 'main' on '5732294'.
  (fix conflicts and then run "git rebase --continue")
  (use "git rebase --skip" to skip this patch)
  (use "git rebase --abort" to check out the original branch)

Unmerged paths:
  (use "git restore --staged <file>..." to unstage)
  (use "git add <file>..." to mark resolution)
        both modified:   main.cpp

no changes added to commit (use "git add" and/or "git commit -a")

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main|REBASE 1/1)
$ git add main.cpp
										\\изменяем код и добавляем его в список
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main|REBASE 1/1)
$ git rebase --continue
[detached HEAD f671e3d] code: добавлен вывод минимума				\\продолжаем перенос коммита выше
 1 file changed, 2 insertions(+), 1 deletion(-)
Successfully rebased and updated refs/heads/main.

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main)
$ git log --oneline --decorate --all --graph
* f671e3d (HEAD -> main) code: добавлен вывод минимума				\\смотрим лог
* 5732294 (origin/main, origin/HEAD) code: добавлен вывод максимума
* e61d869 code: добавлен вывод деления
* f731c82 code: добавлен вывод произведения
* 301e19d git: создан файл игнорирования
* d34c353 code: добавлен вывод разности
* 355c185 code: добавлен вывод суммы
* 4c79937 code: добавлен ввод чисел
* 91fbacf build: добавлен файл проекта
* 4e8555c code: заготовка программы

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/bob/project (main)
$ git push									\\переносим наш коммит на гит
Enter passphrase for key '/c/Users/Админ/.ssh/id_rsa':
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 422 bytes | 422.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:MironRomanov/cs-lab021.git
   5732294..f671e3d  main -> main

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git branch double
										\\создаем новую ветку
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git checkout double
Switched to branch 'double'
M       project.cbp
										\\переходим на нее
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (double)
$ git add main.cpp

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (double)
$ git commit -m 'code: тип данных заменен на double'
[double 7babcf3] code: тип данных заменен на double
 1 file changed, 1 insertion(+), 1 deletion(-)
										\\коммитим изменения
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (double)
$ git checkout main
Switched to branch 'main'
M       project.cbp
Your branch is up to date with 'origin/main'.
										\\переходим на ветку мейн
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git merge double
Updating 5732294..7babcf3
Fast-forward
 main.cpp | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)
										\\соединяем ветки
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git log --oneline --decorate --all --graph
* 7babcf3 (HEAD -> main, double) code: тип данных заменен на double
| * f671e3d (origin/main) code: добавлен вывод минимума
|/										\\видим разветвление
* 5732294 code: добавлен вывод максимума
* e61d869 code: добавлен вывод деления
* f731c82 code: добавлен вывод произведения
* 301e19d git: создан файл игнорирования
* d34c353 code: добавлен вывод разности
* 355c185 code: добавлен вывод суммы
* 4c79937 code: добавлен ввод чисел
* 91fbacf build: добавлен файл проекта
* 4e8555c code: заготовка программы

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git fetch									\\синхронизируем проекты
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 1), reused 3 (delta 1), pack-reused 0
Unpacking objects: 100% (3/3), 402 bytes | 80.00 KiB/s, done.
From github.com:MironRomanov/cs-lab021
   5732294..f671e3d  main       -> origin/main

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git log --oneline --decorate --all --graph
* 7babcf3 (double) code: тип данных заменен на double
| * f671e3d (origin/main) code: добавлен вывод минимума
|/
* 5732294 (HEAD -> main) code: добавлен вывод максимума
* e61d869 code: добавлен вывод деления
* f731c82 code: добавлен вывод произведения
* 301e19d git: создан файл игнорирования
* d34c353 code: добавлен вывод разности
* 355c185 code: добавлен вывод суммы
* 4c79937 code: добавлен ввод чисел
* 91fbacf build: добавлен файл проекта
* 4e8555c code: заготовка программы

Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git fetch
										\\синхронизируем проекты
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git push
To github.com:MironRomanov/cs-lab021.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'github.com:MironRomanov/cs-lab021.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
										\\пытаемся перенести изменения на гит
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git rebase origin/main
Successfully rebased and updated refs/heads/main.
										\\перемещаем наш коммит выше предыдущего
Админ@DESKTOP-2C28JPJ MINGW64 ~/Desktop/lab021/alice/project (main)
$ git push									\\переносим изменения на гит и все
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 468 bytes | 468.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:MironRomanov/cs-lab021.git
   e61d869..5732294  main -> main




