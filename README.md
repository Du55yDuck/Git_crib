# Шпаргалка по работе с *GiT* + База для работы с терминалом. 
---
## Базовые команды для терминала:


$ pwd - инфо о текущей директории<br>     
$ ls -  инфо содержимого директории<br>    
$ ls -a - инфо расширенного списка файлов и папок + скрытые . .. .git<br> 
$ ls ~ - инфо домашней директории<br> 
$ ls .. - инфо директории выше<br>
$ cd . - переход и обращение к текущей директории<br> 
$ cd ~ - переход к домашней директории<br>
$ cd .. - переход выше<br>
$ cd имя директории - переход в указанную директорию<br> 
$ touch имя файла.расширение(txt, md и прочее) - создать файл в текущ директории<br>  
$ mkdir имя папки - создать папку в текущ директории<br>  
$ mkdir ~/имя папки - создать папку в домашней директории<br> 
$ mkdir -p папка_3/папка_2/папка_1 - создать папку в папках в текущ директории<br>  
$ cp что_копируем куда - копия<br>  
$ mv что_перемещаем куда - перемещение<br> 
$ cat имя_файла.txt - распечатать содержимое файла(работает только с текстовыми файлами)<br>  
$ rm имя_файла - удаление файла<br>  
$ rmdir имя_папки - удаление пустой директории<br>  
$ rm -r имя_папки - удаление полной директории<br> 
---


## Установка *Git*. 
Windows - Скачать с офф-сайта + пакет bash. 
Linux - Скачать с офф-сайта. 
Mac OS - 1. В терминале $ usr/bin/git -> install. 
       - 2. Через менеджер пакетов Homebrew. 
В терминале /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)" --> $ brew install git. 
### $ git version - проверка установки. 
---


## Настройка *Git*. 
1. $ git config --global user.name "Имя или ник". 
2. $ git config --global user.email Ваша_почта. 
3. $ cat ~/.gitconfig или $ git config --list - проверка настроек. 
---

## Регистрация на *GitHub* и создание репозитория. 
1. Регимся на Гитхабе. 
2. Создаем новый репозиторий. 
3. Генерация SSh-ключа:<br>  
- $ cd ~ --> $ ls -la .ssh/ - проверка на наличие созданных ключей(id_dsa.pub, id_rsa.pub). 
- Если ключей нет, генерируем новые --> $ ssh-keygen -t ed25519 -C "Ваша_почта". 
Или так $ ssh-keygen -t rsa -b 4096 -C "Ваша_почта". 
- Сохраняем ключи по запросу. 
- Вводим кодовое слово или 2 enter. 
- $ ls -a ~/. Ssh - проверка ключей(.pub - публичный, без pub - приватный). 
4. Привязка ключей к Github:<br>
- копируем содержимое файла .pub в буфер обмена $ pbcopy < ~/.ssh/id_ed25519.pub. 
- или $ clip < ~/.ssh/id_ed25519.pub или .../id_rsa.pub. 
- Github --> settings --> ssh and CPG keys --> new ssh key:<br>
Title: название. 
Key type: authentication key. 
Key: вставить содержимое из буфера обмена. 
- add ssh key(появится на экране). 
5. Проверка - $ ssh -T git@github.com(The authentication...github). 
- Набираем yes --> Hi, имя You've ...<br>
---

## Создание локального репозитория. 
- Создали папку, которая будет репозиторием. 
- В терминале $ git init. 
- проверка - $ git status. 
---

## Связка удаленного и локального репозиториея. 
1. Скопировать URL из созданного репозитория на Гитхабе(ssh --> copy). 
2. $ cd Наш_репозиторий. 
3. $ git remote add origin вставить URL. 
4. $ git remote -v - проверка(должны совпасть). 
----

## Работа с *Git*. 
1. $ cd наш_репозиторий. 
2. $ git add . - подготовить все содержимое к сохранению. 
3. $ git commit -m "текст сообщения: что изменено" - сохранение. 
4. $ git push -u origin main(1-й раз указать -u и имя удал репо и название текущей ветки). 
- Далее по схеме: git add . --> git commit -m "" --> git push. 
---

## Базовые команды для *Git*:<br>
$ git add . - подготовить все содержимое к сохранению<br> 
$ git commit -m "" - сохранить<br>  
$ git push - синхронизация с GitHub<br> 
$ git status - статус процесса<br> 
$ git log - инфо о всех коммитах<br>  
$ git config global user.name "" - привязка имени<br> 
$ git config global user.email ваша_почта - привязка почты<br> 
$ git remote add origin + URL - связка лок и удал репозитория<br> 
$ git remote -v - инфо о репозиториях<br> 
---

### Если нужно "разгитить" директорию:<br>

$ cd директория. 
$ rm -rf .git - удаление без подтверждения (вся история коммитов удаляется). 
---


Не забудьте создать файл README.md. 
Также язык для разметки - [markdown](https://www.markdownguide.org/cheat-sheet/)
---

# Успехов в дальнейшем!

