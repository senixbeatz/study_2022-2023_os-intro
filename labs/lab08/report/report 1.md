---
## Front matter
title: "Лабораторная работа No 8"
subtitle: "Текстовой редактор vi"
author: "Павлов Арсений Валерьевич"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Познакомиться с операционной системой Linux. Получить практические навыки рабо-
ты с редактором vi, установленным по умолчанию практически во всех дистрибутивах.

# Задание 1. Создание нового файла с использованием vi
1. Создайте каталог с именем ~/work/os/lab08.
2. Перейдите во вновь созданный каталог.
3. Вызовите vi и создайте файл hello.sh
vi hello.sh
4. Нажмите клавишу i и вводите следующий текст.
#!/bin/bash
HELL=Hello
function hello {
	LOCAL HELLO=World
	echo $HELLO
}
echo $HELLO
hello
5. Нажмите клавишу Esc для перехода в командный режим после завершения ввода
текста.
6. Нажмите : для перехода в режим последней строки и внизу вашего экрана появится
приглашение в виде двоеточия.
7. Нажмите w (записать) и q (выйти), а затем нажмите клавишу Enter для сохранения
вашего текста и завершения работы.
8. Сделайте файл исполняемым
	chmod +x hello.sh

# Задание 2

1. Вызовите vi на редактирование файла
1 vi ~/work/os/lab08/hello.sh
2. Установите курсор в конец слова HELL второй строки.
3. Перейдите в режим вставки и замените на HELLO. Нажмите Esc для возврата в команд-
ный режим.
4. Установите курсор на четвертую строку и сотрите слово LOCAL.
5. Перейдите в режим вставки и наберите следующий текст: local, нажмите Esc для
возврата в командный режим.
6. Установите курсор на последней строке файла. Вставьте после неё строку, содержащую
следующий текст: echo $HELLO.
7. Нажмите Esc для перехода в командный режим.
8. Удалите последнюю строку.
9. Введите команду отмены изменений u для отмены последней команды.
10. Введите символ : для перехода в режим последней строки. Запишите произведённые
изменения и выйдите из vi.
Здесь приводится описание задания в соответствии с рекомендациями
методического пособия и выданным вариантом.

# Выполнение лабораторной работы

Выполнение задания номер 1.

1. Создаю каталог с именем ~/work/os/lab06 и перехожу во вновь созданный каталог.

![Название рисунка](image/1.png){#fig:001 width=70%}

2. Вызываю vi и создаю файл hello.sh

![Название рисунка](image/2.png){#fig:001 width=70%}

3. Нажимаю клавишу i и ввожу следующий текст.
#!/bin/bash
HELL=Hello
function hello {
	LOCAL HELLO=World
	echo $HELLO
}
echo $HELLO
hello

![Название рисунка](image/3.png){#fig:001 width=70%}
4. Нажимаю клавишу Esc для перехода в командный режим после завершения ввода
текста, а также нажимаю : для перехода в режим последней строки и внизу вашего экрана появится
приглашение в виде двоеточия.

![Название рисунка](image/4.png){#fig:001 width=70%}

5. Нажимаю w (записать) и q (выйти), а затем нажмите клавишу Enter для сохранения
вашего текста и завершения работы.

![Название рисунка](image/5.png){#fig:001 width=70%}

![Название рисунка](image/6.png){#fig:001 width=70%}

6. Делаю файл исполняемым, путем ввода команды
	chmod +x hello.sh
	
Выполнение задания номер 2.
1. Вызываю vi на редактирование файла
	vi ~/work/os/lab08/hello.sh

![Название рисунка](image/3.png){#fig:001 width=70%}


2. Устанавливаю курсор в конец слова HELL второй строки и перехожу в режим вставки и заменяю на HELLO.

![Название рисунка](image/8.png){#fig:001 width=70%}

4. Установливаю курсор на четвертую строку и стираю слово LOCAL.

![Название рисунка](image/9.png){#fig:001 width=70%}

5. Перехожу в режим вставки и набираю следующий текст: local, нажимаю Esc для
возврата в командный режим.

![Название рисунка](image/10.png){#fig:001 width=70%}

6. Устанавливаю курсор на последней строке файла. Вставляю после неё строку, содержащую
следующий текст: echo $HELLO.

![Название рисунка](image/13.png){#fig:001 width=70%}

7. Нажимаю Esc для перехода в командный режим и удаляю последнюю строку.

![Название рисунка](image/15.png){#fig:001 width=70%}

9. Ввожу команду отмены изменений u для отмены последней команды.

![Название рисунка](image/16.png){#fig:001 width=70%}

10. Ввожу символ : для перехода в режим последней строки. Записываю произведённые
изменения и выхожу из vi.

![Название рисунка](image/17.png){#fig:001 width=70%}


# Выводы

Я познакомился с операционной системой Linux, получил практические навыки рабо-
ты с редактором vi, установленным по умолчанию практически во всех дистрибутивах.

# Список литературы

https://esystem.rudn.ru/pluginfile.php/1975909/mod_resource/content/4/008-lab_vi.pdf

::: {#refs}
:::
