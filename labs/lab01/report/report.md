---
## Front matter
title: "Отчет по лабораторной работе №1"
subtitle: "Архитектура операционных систем"
author: "Леснухин Даниил Дмитриевич НПИбд-02-22"

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

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Выполнение лабораторной работы

1. Настройка VirtualBox.
Сперва нужно установить VirtualBox , скачав программу с официального сайта
[VirtualBox](https://www.virtualbox.org/wiki/Downloads) (рис. @fig:001)

![Завершение установки VirtualBox](image/1.png){ #fig:001 width=90%}

Открываем VirtualBox, создаем новую виртуальную машину (рис. @fig:002), (рис. @fig:003). Даем имя
в соответствии с именованием, обозначенным на портале ТУИС. Указываем папку, где
будут храниться файлы виртуальной машины (можно указывать удобную ВАМ папку).
Я выбрал следующий путь: D\:VirtualBox. После данных действий выбираем тип ОС
Linux, версия Fedora(64-bit).

![Создание новой виртуальной машины](image/2.png){ #fig:002 width 90%}

![Создание новой виртуальной машины](image/3.png){ #fig:003 width 90%}

После выполнения вышеперечисленных действий необходимо указать объём 
оперативной памяти для виртуальной машины (рис. @fig:004). Затем создадим новый
виртуальный жесткий диск (рис. @fig:005) и выберем тип файла VDI, он определяет формат,
который будет использоваться при создании жесткого диска (рис. @fig:006). После данных
действий необходимо выбрать динамический формат хранения данных. (рис. @fig:007). 

![Выбор объема памяти](image/4.png){ #fig:004 width 90%}
![Создание нового жесткого диска](image/5.png){ #fig:005 width 90%}
![Определение типа жесткого диска](image/6.png){ #fig:006 width 90%}
![Определение формата хранения](image/7.png){ #fig:007 width 90%}

Завершив первичную настройку, переходим к следующему шагу. Необходимо указать
имя виртуального динамического жесткого диски и его размер (рис. @fig:008). Я установил 60
ГБ

![Определение имени и размера файла](image/8.png){ #fig:008 width 90%}

Мы создали виртуальную машину (рис. @fig:009). Осталось несколько шагов: в настройках во
вкладке «Дисплей» увеличиваем доступный объем видеопамяти до 128 Мб (рис. @fig:010), а
также во вкладке «Носители» добавляем новый привод оптических дисков и применяем
образ (рис. @fig:011) который был скачан с [сайта](https://getfedora.org/ru/workstation/download/).
Подробное описание применения образа (рис. @fig:012).

![Виртуальная машина](image/9.png){# fig:009 width 90%}
![Увеличение памяти](image/10.png){# fig:010 width 90%}
![“Носители” виртуальной машины: выбор образа оптического диска.](image/11.png){ #fig:011 width 90%}
![Продолжение](image/12.png){ #fig:012 width 90%}

Виртуальная машина готова к эксплуатации (рис. @fig:013).

![Виртуальная машина готова к эксплуатации](image/13.png){ #fig:013 width 90%}

2. Запуск виртуальной машины и установка системы.
Запуск liveinst через приложение терминал (рис. @fig:014)

![Запуск liveinst через приложение терминал](image/14.png){ #fig:014 width 90%}

Выбираем язык интерфейса, устанавливаем имя и пароль для нашего пользователя (рис. @fig:015)

![Выбираем язык интерфейса, устанавливаем имя и пароль для нашего пользователя](image/15.png){ #fig:015 width 90%}

После этого приступаем к выполнению домашнего задания, т.к. все предыдущие шаги уже выполнены.

(рис. @fig:016)

![Домашнее задание](image/16.png){ #fig:016 width 100%}




# Выводы

Приобрели практические навыки установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

