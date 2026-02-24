---
## Front matter
title: "Отчёт по лабораторной работе №1"
subtitle: "Архитектура компьютера"
author: "Агапова Анна Антоновна"

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
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы
Приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Выполнение лабораторной работы
1.Virtualbox у меня уже был установлен, открываю окно приложения и создаю новую виртуальную машину. Указываю её имя, путь к папке машины, выбираю тип ОС и версию. (рис. [-@fig-001])

![Создание виртуальной машины](1.png){#fig-001 width=60%}

2.Указываю объем основной памяти виртуальной машины размером 4096 Мб (рис. [-@fig-002])

![Указание объема памяти](2.png){#fig-002 width=60%}

3.Создаю новый виртуальный диск.Задаю размер диска 80 Гб. Задаю тип и формат жёсткого диска: VDI. (рис. [-@fig-003])

![Создание виртуального диска](3.png){#fig-003 width=60%}

4.Выполняю команду liveinst, чтобы установить базовые настройки Fedora.(рис. [-@fig-004])

![Команда liveinst](4.png){#fig-004 width=60%}

5.Устанавливаю язык (рис. [-@fig-005])

![Установка языков](5.png){#fig-005 width=60%}

6.Устанавливаю часовой пояс и дату. (рис. [-@fig-006])

![Установка часового пояса](6.png){#fig-006 width=60%}

7.Создаю учетную запись. (рис. [-@fig-007])

![Создание учетной записи](7.png){#fig-007 width=60%}

8.Создаю учетной записи root. (рис. [-@fig-008])

![Создание учетной записи root](8.png){#fig-008 width=60%}

9.Создалась учетная запись. (рис. [-@fig-009])

![Учетная запись](9.png){#fig-009 width=60%}

10.Перехожу на спецпользователя. (рис. [-@fig-0010])

![Переход на root](10.png){#fig-0010 width=60%}

11.Устанавливаю срества разработки. (рис. [-@fig-0011])

![Установка средств разработки](11.png){#fig-0011 width=60%}

12.Меняю hostname. (рис. [-@fig-0012])

![Изменение hostname](12.png){#fig-0012 width=60%}

13.Запускаю таймер. (рис. [-@fig-0013])

![Запуск таймера](13.png){#fig-0013 width=60%}

14.Открываю md, перехожу в /etc/selinux/config. (рис. [-@fig-0014])

![Работа с md](14.png){#fig-0014 width=60%}

15.Меняю значение SELINUX=enforcing на SELINUX=permissive и перезагружаю виртуальную машину.(рис. [-@fig-0015])

![Отключение SELinux](15.png){#fig-0015 width=60%}

16.Устанавливаю pandoc для работы с языком разметки Markdown. (рис. [-@fig-0016])

![Работа с языком разметки Markdown](16.png){#fig-0016 width=60%}

# Контрольные вопросы
1. Учетная запись пользователя содержит необходимые для идентификации пользователя
при подключении к системе данные, а так же информацию для авторизации и учета: системного имени (user name), идентификатор пользователя (UID), идентификатор груп-
пы (CID), полное имя (full name), домашний каталог (home directory), начальная оболочка (login shell).
2. Для получения
справки по команде: –help; для перемещения по файловой
системе - cd; для просмотра содержимого каталога - ls; для определения
объёма каталога - du ; для создания / удаления каталогов - mkdir/rmdir; для
создания / удаления файлов - touch/rm; для задания определённых прав на
файл / каталог - chmod; для просмотра истории команд - history
3. Файловая система - это порядок, определяющий способ организации и
хранения и именования данных на различных носителях информации.
Примеры: FAT32 представляет собой пространство, разделенное на три части: одна область для служебных структур, форма указателей в виде таблиц и зона для хранения самих файлов. ext3/ext4 - журналируемая файловая система, используемая в основном в ОС с ядром Linux.
4. С помощью команды df, введя ее в терминале. Это утилита, которая пока-
зывает список всех файловых систем по именам устройств, сообщает их
размер и данные о памяти. Также посмотреть подмонтированные файловые
системы можно с помощью утилиты mount.
5. Чтобы удалить зависший процесс, вначале мы должны узнать, какой у него id: используем команду ps. Далее в терминале вводим команду kill < PID >. Или можно использовать утилиту killall, что “убьет” все процессы, которые есть в данный момент, для этого не нужно знать id процесса.

# Выводы
При выполнении данной лабораторной работы я приобрела практические
навыки установки операционной системы на виртуальную машину, а так же
сделала настройки минимально необходимых для дальнейшей работы сервисов.

# Список литературы
1. Dash, P. Getting Started with Oracle VM VirtualBox / P. Dash. – Packt Publishing Ltd, 2013. – 86 сс.
2. Colvin, H. VirtualBox: An Ultimate Guide Book on Virtualization with VirtualBox. VirtualBox / H. Colvin. – CreateSpace Independent Publishing Platform, 2015. – 70 сс.
3. Vugt, S. van. Red Hat RHCSA/RHCE 7 cert guide : Red Hat Enterprise Linux 7 (EX200 and EX300) : Certification Guide. Red Hat RHCSA/RHCE 7 cert guide / S. van Vugt. – Pearson IT Certification, 2016. – 1008 сс.
4. Робачевский, А. Операционная система UNIX / А. Робачевский, С. Немнюгин, О. Стесик. – 2-е изд. – Санкт-Петербург : БХВ-Петербург, 2010. – 656 сс.
5. Немет, Э. Unix и Linux: руководство системного администратора. Unix и Linux / Э. Немет, Г. Снайдер, Т.Р. Хейн, Б. Уэйли. – 4-е изд. – Вильямс, 2014. – 1312 сс.
6. Колисниченко, Д.Н. Самоучитель системного администратора Linux : Системный администратор / Д.Н. Колисниченко. – Санкт-Петербург : БХВ-Петербург, 2011. – 544 сс.
7. Robbins, A. Bash Pocket Reference / A. Robbins. – O’Reilly Media, 2016. – 156 сс.
