# Домашнее задание к занятию "`Git`" - `Шелухин Юрий`


## Задание 1

**Что нужно сделать:**

1. Зарегистрируйте аккаунт на [GitHub](https://github.com/).
2. Создайте  **новый отдельный публичный репозиторий**. Обязательно поставьте галочку в поле «Initialize this repository with a README».
3. Склонируйте репозиторий, используя https протокол `git clone ...`.
4. Перейдите в каталог с клоном репозитория.
5. Произведите первоначальную настройку Git, указав своё настоящее имя и email: `git config --global user.name` и `git config --global user.email johndoe@example.com`.
6. Выполните команду `git status` и запомните результат.
7. Отредактируйте файл README.md любым удобным способом, переведя файл в состояние Modified.
8. Ещё раз выполните `git status` и продолжайте проверять вывод этой команды после каждого следующего шага.
9. Посмотрите изменения в файле README.md, выполнив команды `git diff` и `git diff --staged`.
10. Переведите файл в состояние staged или, как говорят, добавьте файл в коммит, командой `git add README.md`.
11. Ещё раз выполните команды `git diff` и `git diff --staged`.
12. Теперь можно сделать коммит `git commit -m 'First commit'`.
13. Сделайте `git push origin master`.

В качестве ответа добавьте ссылку на этот коммит в ваш md-файл с решением.

## Решение 1

1-6
cd ~/HW/8-01  
git init  
git config --global user.name YuryShelukhin  
git config --global user.email yysg@yandex.ru

![статус до коммита](https://github.com/YuryShelukhin/8-01HW/blob/master/img/1-1-6.png?raw=true)


7-11  
добавим отслеживание

<img src = "img/1-1-6.png" width = 60%>


Коммит после решения  
[ссылка](https://github.com/YuryShelukhin/8-01HW/commit/5f92d30deaf7c21fae70984601fac4e9f5987925)

---

### Задание 2

1. Создайте файл .gitignore (обратите внимание на точку в начале файла) и проверьте его статус сразу после создания.
2. Добавьте файл .gitignore в следующий коммит git add....
3. Напишите правила в этом файле, чтобы игнорировать любые файлы .pyc, а также все файлы в директории cache.
4. Сделайте коммит и пуш.

## Решение 2

1-2.
<img src = "img/2-1-2.png" width = 60%>

3.
<img src = "img/2-3.png" width = 60%>

4.
<img src = "img/2-4.png" width = 60%>

Коммит после решения  
[ссылка](https://github.com/YuryShelukhin/8-01HW/commit/9907d3be05a9698f4ef948dd64de2597b55d6bab)

---

### Задание 3


1. Создайте новую ветку dev и переключитесь на неё.
2. Создайте в ветке dev файл test.sh с произвольным содержимым.
3. Сделайте несколько коммитов и пушей в ветку dev, имитируя активную работу над  
    файлом в процессе разработки.
4. Переключитесь на основную ветку.
5. Добавьте файл main.sh в основной ветке с произвольным содержимым, сделайте комит и пуш . Так имитируется продолжение общекомандной разработки в основной ветке во время разработки отдельного функционала в dev ветке.
6. Сделайте мердж dev ветки в основную с помощью git merge dev. Напишите осмысленное сообщение в появившееся окно комита.
7. Сделайте пуш в основной ветке.
8. Не удаляйте ветку dev.

В качестве ответа прикрепите ссылку на граф коммитов https://github.com/ваш-логин/ваш-репозиторий/network в ваш md-файл с решением.

Ваш граф комитов должен выглядеть аналогично скриншоту:

<img src = "img/3-0.png" width =60%>

## Решение 3.

1-3.  
<img src = "img/3-1-3.png" width =60%>
git add .  
git status 
git checkout -b dev  
git commit -am 'dev commit 1'  
git push origin dev  
Изменяем файл, несколько раз комиттим и пушим  
4.   
git branch -v   
git checkout master  
5.  
vim main.sh  
git add .  
git commit -am 'commit 25 master'  
git push origin master  
6.  
git merge dev  
7.  
git commit -am 'commit 26 master'  
git push origin master  

Ссылка на граф коммитов после решения  
[ссылка](https://github.com/YuryShelukhin/8-01HW/network)

<img src = "img/3-8.png" width =60%>

---


### Задание 4

1. Создайте ветку conflict и переключитесь на неё.
2. Внесите изменения в файл test.sh.
3. Сделайте коммит и пуш.
4. Переключитесь на основную ветку.
5. Измените ту же самую строчку в файле test.sh.
6. Сделайте коммит и пуш.
7. Сделайте мердж ветки conflict в основную ветку и решите конфликт так, чтобы в результате в файле оказался код из ветки conflict.

В качестве ответа на задание прикрепите ссылку на граф коммитов https://github.com/ваш-логин/ваш-репозиторий/network в ваш md-файл с решением.

## Решение 4

1.  
git checkout -b conflict  
2.  
<img src = "img/4-2.png" width =60%>
3-4.  
git push origin master  
5.   
<img src = "img/4-5.png" width =60%>
6-7.  
<img src = "img/4-7.png" width =60%>

Ссылка на граф коммитов после решения  
[ссылка](https://github.com/YuryShelukhin/8-01HW/network)

<img src = "img/4-graf.png" width =60%>






