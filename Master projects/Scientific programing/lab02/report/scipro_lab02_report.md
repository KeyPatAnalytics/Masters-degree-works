---
# Front matter
lang: ru-RU
title: "Научное програмирование"
subtitle: "Отче по лабораторной работе № 2: Markdown"
author: "Кейела Патачона- НПМмд-02-21"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Научиться оформлять отчёты с помощью легковесного языка разметки Markdown.

# Теоретические сведения

Вся теоритическая часть по использованию языка разметки Markdown была взята из инструкции по лабораторной работе №2 на сайте:
https://esystem.rudn.ru/pluginfile.php/1284122/mod_resource/content/3/002-markdown.pdf 


# Выполнение лабораторной работы

**1.** Создадим учётную запись на https://github.com. 

![рисунок 1](../screenshots/01.png){ #fig:001 width=70% }

**2.**  Установим git на наш компьтер. 

![рисунок 2](../screenshots/02.png){ #fig:002 width=70% }

![рисунок 3](../screenshots/03.png){ #fig:003 width=70% }

**3.** Настроим систему контроля версий git, как это указано в инструкции к 1-ой лаборатной работе  c использованием сервера репозиториев https://github.com/.

Для этого необходимо сгенерировать пару ключей (приватный и открытый), а затем вставить их в SSH-ключи на github.

![рисунок 4](../screenshots/04.png){ #fig:004 width=70% }

![рисунок 5](../screenshots/05.png){ #fig:005 width=70% }

![рисунок 6](../screenshots/06.png){ #fig:006 width=70% }

**4.** Создадим структуру каталога лабораторных работ согласно пункту М.2.

**5.** Подключение репозитория к github 

Создадим репозиторий на GitHub.

Рабочий каталог будем обозначать как laboratory. Вначале нужно перейти в этот
каталог:

–cd laboratory

Инициализируем системы git:

–git init

Создаём заготовку для файла README.md:

–echo "# Лабораторные работы" >> README.md

–git add README.md

Делаем первый коммит и выкладываем на github:

–git commit -m "first commit"

–git remote add origin git@github.com:<username>/sciproc-intro.git

–git push -u origin master

Результат проделанных операций представлен ниже.

![рисунок 7](../screenshots/07.png){ #fig:007 width=70% }

![рисунок 8](../screenshots/08.png){ #fig:008 width=70% }

![рисунок 9](../screenshots/09.png){ #fig:009 width=70% }

**6.** Первичная конфигурация 

Добавим файл лицензии:

–wget https://creativecommons.org/licenses/by/4.0/legalcode.txt -O

Добавим шаблон игнорируемых файлов. Просмотрим список имеющихся шаблонов:
–curl -L -s https://www.gitignore.io/api/list

Затем скачаем шаблон, например, для C:

–curl -L -s https://www.gitignore.io/api/c >> .gitignore

Можно это же сделать через web-интерфейс на сайте https://www.gitignore.io/.

Добавим новые файлы:

–git add .
Выполним коммит:

–git commit -a
Отправим на github:

–git push

Результат проделанных операций представлен ниже.

![рисунок 10](../screenshots/10.png){ #fig:010 width=70% }

![рисунок 11](../screenshots/11.png){ #fig:011 width=70% }

![рисунок 12](../screenshots/12.png){ #fig:012 width=70% }


**7.** Конфигурация git-flow 

– Инициализируем git-flow

git flow init

Префикс для ярлыков установим в v.

– Проверьте, что Вы на ветке develop:

git branch

– Создадим релиз с версией 1.0.0

git flow release start 1.0.0

– Запишем версию:

echo "1.0.0" >> VERSION
– Добавим в индекс:

git add .

git commit -am 'chore(main): add version'

– Зальём релизную ветку в основную ветку

git flow release finish 1.0.0

– Отправим данные на github

git push --all

git push --tags

– Создадим релиз на github.


# Выводы

Были изучены идеология и применение средств контроля версий. Также был освоен язык разметки Markdown.

# Контрольные вопросы

1. Что такое системы контроля версий (VCS) и для решения каких задач они предназначаются?

• Системы контроля версий (Version Control System, VCS) применяются при работе
нескольких человек над одним проектом.

2. Объясните следующие понятия VCS и их отношения: хранилище, commit, история,
рабочая копия.

• Хранилище (repository), или репозитарий, —место хранения всех версий и служебной информации. Commit («[трудовой] вклад», не переводится) — синоним версии; процесс создания новой версии. Рабочая копия (working copy) — текущее состояние файлов проекта, основанное на версии, загруженной из хранилища (обычно на последней).

3. Что представляют собой и чем отличаются централизованные и децентрализованные
VCS? Приведите примеры VCS каждого вида.

• Централизованные системы контроля версий представляют собой приложения типа клиент-сервер, когда репозиторий проекта существует в единственном экземпляре и хранится на сервере. Доступ к нему осуществлялся через специальное клиентское приложение. В качестве примеров таких программных продуктов можно привести CVS, Subversion.аспределенные системы контроля версий (Distributed Version Control System, DVCS) позволяют хранить репозиторий (его копию) у каждого разработчика, работающего с данной системой. При этом можно выделить центральный репозиторий (условно), в который будут отправляться изменения из локальных и, с ним же эти локальные репозитории будут синхронизироваться. При работе с такой системой, пользователи периодически синхронизируют свои локальные репозитории с центральным и работают непосредственно со своей локальной копией. После внесения достаточного количества изменений в локальную копию они (изменения) отправляются на сервер. При этом сервер, чаще всего, выбирается условно, т.к. в большинстве DVCS нет такого понятия как “выделенный сервер с центральным репозиторием”.

4. Опишите действия с VCS при единоличной работе с хранилищем.

5. Опишите порядок работы с общим хранилищем VCS.

6. Каковы основные задачи, решаемые инструментальным средством git?

•Возврат к любой версии кода из прошлого. Просмотр истории изменений. Совместная работа без боязни потерять данные или затереть чужую работу.

7. Назовите и дайте краткую характеристику командам git.

• Наиболее часто используемые команды git:

– создание основного дерева репозитория:

git init

– получение обновлений (изменений) текущего дерева из центрального репозитория:
git pull

– отправка всех произведённых изменений локального дерева в центральный репозиторий:

git push
– просмотр списка изменённых файлов в текущей директории:
git status

– просмотр текущих изменения:

git diff

– добавить все изменённые и/или созданные файлы и/или каталоги:
git add .

– добавить конкретные изменённые и/или созданные файлы и/или каталоги:

git add имена_файлов
– удалить файл и/или каталог из индекса репозитория (при этом файл и/или каталог
остаётся в локальной директории):

git rm имена_файлов

– сохранение добавленных изменений:

– сохранить все добавленные изменения и все изменённые файлы:
git commit -am 'Описание коммита'

– сохранить добавленные изменения с внесением комментария через встроенный
редактор:

git commit

– создание новой ветки, базирующейся на текущей:
git checkout -b имя_ветки

– переключение на некоторую ветку:

git checkout имя_ветки

– отправка изменений конкретной ветки в центральный репозиторий:

git push origin имя_ветки

– слияние ветки с текущим деревом:

git merge --no-ff имя_ветки

8. Приведите примеры использования при работе с локальным и удалённым репозиториями.

• См пункты 1.3.3 -1.3.4

9. Что такое и зачем могут быть нужны ветви (branches)?

• Ветки нужны для того, чтобы программисты могли вести совместную работу над проектом и не мешать друг другу при этом.

10. Как и зачем можно игнорировать некоторые файлы при commit?

• Игнорируемые файлы — это, как правило, артефакты сборки и файлы, генерируемые машиной из исходных файлов в вашем репозитории, либо файлы, которые по какой-либо иной причине не должны попадать в коммиты. Для этого нужно указать название все игноиремых файлов в файде с названием .gitignore



