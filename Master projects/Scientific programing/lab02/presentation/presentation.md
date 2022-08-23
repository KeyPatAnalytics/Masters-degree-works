---
## Front matter
lang: ru-RU
title: Основы Markdown
author: Кейела Патачона
institute: Российский Университет Дружбы Народов
date: 20 ноября, 2021, Москва, Россия

## Formatting
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
toc: false
slide_level: 2
theme: metropolis
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
---

# Цели и задачи
## Цель лабораторной работы

Научиться оформлять презентации с помощью легковесного языка разметки Markdown

# Выполнение лабораторной работы

## Базовые сведения о Markdown

Чтобы создать заголовок, используйте знак (#), например:
```
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```
Чтобы задать для текста полужирное начертание, заключите его в двойные звездочки:
```
This text is **bold**.
```
Чтобы задать для текста курсивное начертание, заключите его в одинарные звездочки:
```
This text is *italic*.
```

## Базовые сведения о Markdown


Чтобы задать для текста полужирное и курсивное начертание, заключите его в тройные
звездочки:
```
This is text is both ***bold and italic***.
```
Блоки цитирования создаются с помощью символа >:
```
> The drought had lasted now for ten million years, 
  and  bla-bla-bla-bla-bla... 
```

## Базовые сведения о Markdown

Неупорядоченный (маркированный) список можно отформатировать с помощью звездочек или тире:
```
- List item 1
- List item 2
- List item 3
```
Чтобы вложить один список в другой, добавьте отступ :
```
- List item 1
	- List item A
	- List item B
- List item 2
- List item 2
```
Упорядоченный список можно отформатировать с помощью соответствующих цифр.


## Базовые сведения о Markdown

Синтаксис Markdown для встроенной ссылки состоит из части [link text], представляющей текст гиперссылки, и части (file-name.md) – URL-адреса или имени файла, на
который дается ссылка:
```
[link text](file-name.md)
```
## Базовые сведения о Markdown

Верхние и нижние индексы:

H~2~O записывается как
```
H~2~O
```
2^10^ записывается как
```
2^10^
```
$\sin^2 (x) + \cos^2 (x) = 1$  записывается как:
```
$\sin^2 (x) + \cos^2 (x) = 1$
```
## Конвертация из  Markdown в pdf и doc

Для обработки файлов в формате Markdown будем использовать Pandoc.

Преобразовать файл README.md можно следующим образом:
```
pandoc README.md -o README.pdf
```
или так
```
pandoc README.md -o README.docx
```

## Контрольный пример

![Markdown is useful](love_markdown.png){ #fig:001 width=70% height=70%}


# Выводы

Мы изучали основные комманды Markdown

## Результаты выполнения лабораторной работы

Научились оформлять презентацию с помощью легковесного языка разметки Markdown