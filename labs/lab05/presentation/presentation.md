---
## Front matter
lang: ru-RU
title: Архитектура операционных систем
subtitle: "Лабораторная работа № 5. Анализ файловой системы Linux.
Команды для работы с файлами и каталогами"
author:
  - Леснухин Д. Д.
institute:
  - Российский университет дружбы народов, Москва, Россия


## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
---

# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Леснухин Даниил Дмитриевич
  * Студент НПИбд-02-22
  * Российский университет дружбы народов
  * [1132221553@pfur.ru](1132221553@pfur.ru)



:::
::::::::::::::

# Вводная часть

## Актуальность

Ознакомление с файловой системой Linux, её структурой, именами и содержанием
каталогов. Приобретение практических навыков по применению команд для работы
с файлами и каталогами, по управлению процессами (и работами), по проверке использования диска и обслуживанию файловой системы.

## Цели и задачи

1. Выполните все примеры, приведённые в первой части описания лабораторной работы.

2. Выполните следующие действия, зафиксировав в отчёте по лабораторной работе
используемые при этом команды и результаты их выполнения:
2.1. Скопируйте файл /usr/include/sys/io.h в домашний каталог и назовите его
equipment. Если файла io.h нет, то используйте любой другой файл в каталоге
/usr/include/sys/ вместо него.
2.2. В домашнем каталоге создайте директорию ~/ski.plases.
2.3. Переместите файл equipment в каталог ~/ski.plases.
2.4. Переименуйте файл ~/ski.plases/equipment в ~/ski.plases/equiplist.
2.5. Создайте в домашнем каталоге файл abc1 и скопируйте его в каталог
~/ski.plases, назовите его equiplist2.
2.6. Создайте каталог с именем equipment в каталоге ~/ski.plases.
2.7. Переместите файлы ~/ski.plases/equiplist и equiplist2 в каталог
~/ski.plases/equipment.
2.8. Создайте и переместите каталог ~/newdir в каталог ~/ski.plases и назовите
его plans.

3. Определите опции команды chmod, необходимые для того, чтобы присвоить перечисленным ниже файлам выделенные права доступа, считая, что в начале таких прав
нет:
3.1. drwxr--r-- ... australia
3.2. drwx--x--x ... play
3.3. -r-xr--r-- ... my_os
3.4. -rw-rw-r-- ... feathers
При необходимости создайте нужные файлы.

4. Проделайте приведённые ниже упражнения, записывая в отчёт по лабораторной
работе используемые при этом команды:
4.1. Просмотрите содержимое файла /etc/password.
4.2. Скопируйте файл ~/feathers в файл ~/file.old.
4.3. Переместите файл ~/file.old в каталог ~/play.
4.4. Скопируйте каталог ~/play в каталог ~/fun.
4.5. Переместите каталог ~/fun в каталог ~/play и назовите его games.
4.6. Лишите владельца файла ~/feathers права на чтение.
4.7. Что произойдёт, если вы попытаетесь просмотреть файл ~/feathers командой
cat?
4.8. Что произойдёт, если вы попытаетесь скопировать файл ~/feathers?
4.9. Дайте владельцу файла ~/feathers право на чтение.
4.10. Лишите владельца каталога ~/play права на выполнение.
4.11. Перейдите в каталог ~/play. Что произошло?
4.12. Дайте владельцу каталога ~/play право на выполнение.

5. Прочитайте man по командам mount, fsck, mkfs, kill и кратко их охарактеризуйте,
приведя примеры.

## Выполняем примеры, приведенные в методических материалах.

Используем следующие команды: 
1.1 touch - создание текстового файла.
1.2 cp - копирование файла с перемещением из одного каталога в другой.
1.3 mv - используется для того, чтобы переименовать файл или переместить его. (рис. @fig:001), (рис. @fig:002). 

![Выполнение примеров из методических материалов.](image/1.png){#fig:001 width=60%}

## Создание файла equipment.

Скопируем файл /usr/include/sys/io.h в домашний каталог и назовем его
equipment. (рис. @fig:003)

![Создание файла equipment.](image/3.png){#fig:003 width=60%)

## Выполняем действия с файлом equipment.

3. Далее мы должны создать директорию ~/ski.plases в домашней директории. Переместим файл equipment в созданную директорию. Следующим шагом мы переименовываем файл equipment в equiplist. Проверяем. (рис. @fig:004).

![Выполняем действия с файлом equipment.](image/4.png){#fig:004 width=60%)

## Работа с файлом abc1

4. Теперь мы должны создать файл abc1 в домашнем каталоге и скопировать его в каталог ~/ski/plases, переименовать его в equiplist2. Проверяем. (рис. @fig:005). Перемещаем файлы ~/ski.plases/equiplist и equiplist2 в каталог ~/ski.plases/equipment. Создаем каталог newdir и перемещаем его в ~/ski.plases, путем команд mkdir newdir, mv newdir plans, mv plans ~/ski.plases.

![Работа с файлом abc1](image/5.png){#fig:005 width=60%}

## Определяем опции команды chmod.

Далее мы определяем опции, путем анализа, команды chmod, необходимые для того, чтобы присвоить перечисленным ниже файлам выделенные права доступа, считая, что в начале таких прав
нет:
3.1. drwxr--r-- ... australia
3.2. drwx--x--x ... play
3.3. -r-xr--r-- ... my_os
3.4. -rw-rw-r-- ... feathers

(рис. @fig:006).

![Определяем опции команды chmod](image.6png){#fig:006 width=60%)

## Выполнение 4 действия из методических материалов.

На этом шаге мы должны выполнить следующие действия: (рис. @fig:007).
     Просмотреть содержимое файла /etc/password.
6.1. Скопировать файл ~/feathers в файл ~/file.old.
6.2. Переместить файл ~/file.old в каталог ~/play.
6.3. Скопировать каталог ~/play в каталог ~/fun.
6.4. Переместить каталог ~/fun в каталог ~/play и назовите его games.
6.5. Лишите владельца файла ~/feathers права на чтение.
6.6. Просмотреть файл ~/feathers командой cat?
6.7. Скопировать файл ~/feathers?
6.8. Дать владельцу файла ~/feathers право на чтение.
6.9. Лишить владельца каталога ~/play права на выполнение.
6.10. Перейти в каталог ~/play. Что произошло?
4.12. Дать владельцу каталога ~/play право на выполнение. 

![Выполнение ряда действий](image.7.png){#fig:007 width=60%)

## Читаем man по командам.

Прочитаем man по командам fsck, mount и др. (рис. @fig:008).

![Читаем man по командам](image/8.png){#fig:008 width=90%}

## Результаты

Ознакомились с файловой системой Linux, её структурой, именами и содержанием
каталогов. Приобрели практические навыки по применению команд для работы
с файлами и каталогами, по управлению процессами (и работами), по проверке использования диска и обслуживанию файловой системы.



