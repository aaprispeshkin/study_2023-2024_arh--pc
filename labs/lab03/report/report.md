---
## Front matter
title: "Лабораторная работа №3"
subtitle: "Язык разметки Markdown"
author: "Приспешкин Андрей Андреевич"

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

Целью данной лабораторной работы является освоение языка разметки Markdown и оформления отчётов на этом языке.

# Задание

1. Установка необходимого ПО
2. Выполнение отчёта с помощью языка разметки Markdown
3. Загрузка отчёта на GitHub

# Выполнение лабораторной работы

Зайдём в рабочий каталог созданный в лаюораторной работе №2 и воспользуемся командой git pull для обновления каталога(рис.1).

![Рис.1 Переход в рабочий каталог и использование git pull ](image/lab01.png)

Перейдём в подкаталог третьей лабораторной работы(рис.2)

![Рис. 2 Переход в подкаталог третьей лабораторной работы](image/lab02.png)

В этом подкаталоге используем команду make чтобы скомпилировать pdf и docx файлы отчёта из файла с расширением md(markdown)(рис.3)

![Рис. 3 Пример работы команды make и проверка с помощью утилиты ls](image/lab03.png)

Удалим скомпилированные файлы командой make clean и проверим её работу утилитой ls(рис.4)

![Рис. 4 Пример работы команды make clean и проверка утилитой ls](image/lab04.png)

Далее, начнём делать отчёт в текстовом редакторе neovim(рис.5)

![Рис. 5 Открытие отчёта в текстовом редакторе neovim](image/lab05.png)

Загрузим отчёт на github с помощью команд git add, git commit и git push(рис.6)

![Рис.6 Загрузка отчёта на github](image/lab06.png)

# Выводы

В результате данной лабораторной работы я освоил базовые навыки работы с языком разметки markdown

# Список литературы{.unnumbered}

[Лабораторная работа №3. Язык разметки Markdown](https://esystem.rudn.ru/pluginfile.php/2089083/mod_resource/content/0/%D0%9B%D0%B0%D0%B1%D0%BE%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%20%E2%84%963.%20%D0%AF%D0%B7%D1%8B%D0%BA%20%D1%80%D0%B0%D0%B7%D0%BC%D0%B5%D1%82%D0%BA%D0%B8%20.pdf)
