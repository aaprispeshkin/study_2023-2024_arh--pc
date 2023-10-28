---
## Front matter
title: "Лабораторная работа №4"
subtitle: "Создание и процесс обработки программ на языке ассемблера NASM"
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

Цель данной лабораторной работы -- базовая ознакомление с языком NASM, а также освоить процедуры компиляции и сборки программ написаных на этом языке.

# Задание

1. Создание программы Hello world на языке NASM
2. Работа с транслятором NASM
3. Работа с компоновщиком LD
4. Запуск исполняемого файла
5. Задания для самостоятельной работы

# Выполнение лабораторной работы

Создадим в рабочем каталоге work подкаталог в котором будет выполняться лабораторная работа(Рис.1).

![Рис. 1 Создание нового подкаталога](image/lab01.png)

Перейдём в созданный нами подкаталог(Рис.2).

![Рис. 2 Переход в созданный подкаталог](image/lab02.png)

Создадим файл hello.asm утилитой touch(Рис.3).

![Рис. 3 Создание файла hello.asm](image/lab03.png)

Редактировать файл будем в текстовом редакторе neovim(Рис.4).

![Рис. 4 Откроем файл hello.asm в текстовом редакторе neovim](image/lab04.png)

Вставим пример кода из лабораторной работы в текстовый редактор(Рис.5).

![Рис. 5 Пример кода в текстовом редакторе](image/lab05.png)

Переведём текст программы hello.asm в объектный код с помощью транслятора(Рис.6).

![Рис. 6 Работа транслятора](image/lab06.png)

Введём команду которая скомпилирует файл hello.asm в файл obj.o, так же воспользуемся ключом -g и с помощью ключа -l создадим файл листинга list.lst(Рис.7).

![Рис.7 Компиляция программы с расширенным синтаксисом](image/lab07.png)

Проверим правильность выполнения работы утилитой ls(Рис.8).

![Рис.8 Проверка работы транслятора](image/lab07.5.png)

Передадим файл hello.o компоновщику ld, зададим имя создаваемого файла с помощью ключа -o(Рис.9).

![Рис. 9 Работа компоновщика ld](image/lab08.png)

Проверим правильность работы компоновщика утилитой ls(Рис. 10).

![Рис.10 Проверка работы компоновщика](image/lab08.5.png)

Передадим файл obj.o компоновщику. Файл будем иметь имя main, так как оно было указано после ключа -o(Рис.11).

![Рис.11 Передача файла obj.o компоновщику и проверка его работы](image/lab09.png)

Запустим сделанную нами программу hello(Рис.12).

![Рис. 12 Запуск программы hello](image/lab10.png)

Утилитой cp создадим копию hello.asm и назовём её lab4.asm. Проверим правильность копирования утилитой ls(Рис.13).

![Рис.13 Копирование файла hello.asm](image/lab11.png)

Откроем файл lab4.asm в текстовом редакторе neovim(Рис.14).

![Рис.14 Использование команды nvim для открытие файла lab4.asm](image/lab12.png)

Внеёсем изменения в код так, чтобы программа lab4.asm выводила мои имя и фамилию(Рис.15).

![Рис.15 Код с внесёнными изменениями](image/lab13.png)

Скомпилируем получившийся код в объектный файл lab4.o(Рис.16).

![Рис.16 Компиляция программы lab4.asm](image/lab14.png)

Отправим объектный код компоновщику для создания файла lab(Рис.17).

![Рис.17 Создание файла lab](image/lab15.png)

Запустим для проверки программу lab(Рис.18).

![Рис.18 Результат работы программы lab](image/lab16.png)

Скопируем программы созданные в ходе этой лабораторной работы в рабочий каталог(Рис.19).

![Использование утилиты cp для копирования программ в рабочий каталог](image/lab17.png)

# Выводы

В ходе данной лабораторной работы я познакомился с языком NASM, а так же научился работать с компилятором и компоновщиком для превращения программ в объектный код и запускаемые файлы соответственно.

# Список литературы{.unnumbered}

[Лабораторная работа №4. Создание и процесс обработки программ на языке ассемблера NASM](https://esystem.rudn.ru/mod/resource/view.php?id=1030552)
