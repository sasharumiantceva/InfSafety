---
# Front matter
lang: ru-RU
title: 'Отчёт по лабораторной работе 1'
subtitle: 'Установка и конфигурация операционной системы на виртуальную машину'
author: 'Румянцева Александра Сергеевна'

# Formatting
toc-title: 'Содержание'
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
mainfont: Ubuntu
romanfont: Ubuntu
sansfont: Ubuntu
monofont: Ubuntu
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

Приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Задание

Лабораторная работа подразумевает установку на виртуальную машину VirtualBox (https://www.virtualbox.org/) операционной системы Linux, дистрибутив Centos.

# Выполнение лабораторной работы

1. Запускаю _Virtual Box_, задаю располодение для виртуальных машин в папке с _rumiantceva_ (рис.1), и выбираю удобную для меня клавишу управления: _Right_ _Ctrl_ (рис. 2).

   ![рис.1. Выбор папки для виртуальных машин.](images/1.jpg){ #fig:001 width=60% }

   ![рис.2. Настройка клавиши управления.](images/2.jpg){ #fig:002 width=60% }

2. Создаю новую виртуальную машину с именем **_Base_**: выбираю тип операционной системы _Linux_, а также версию _Red Hat_ (рис.3).

   ![рис.3. Окно "Имя машины и тип ОС".](images/3.jpg){ #fig:003 width=60% }

3. Указываю объем памяти 1024 МБ (рис.4).

   ![рис.4. Окно "Объем памяти".](images/4.jpg){ #fig:004 width=60% }

4. Задаю конфигурацию жесткого диска: создаю новый динамический виртуальный жёсткий диск типа VDI, а также размер диска - 40 ГБ и его расположение (рис.5-8).

   ![рис.5. Создание жёсткого диска.](images/5.jpg){ #fig:005 width=60% }

   ![рис.6. Тип жёсткого диска.](images/6.jpg){ #fig:006 width=60% }

   ![рис.7. Жёсткий диск. Формат хранения.](images/7.jpg){ #fig:007 width=60% }

   ![рис.8. Размер жёсткого диска.](images/8.jpg){ #fig:008 width=60% }

5. Добавляю во вкладке _"Носители"_ свойств виртулальной машины новый привод оптических дисков, выбираю нужный образ для установки операционной системы (рис.9).

   ![рис.9. Окно "Выбор оптического диска"](images/9.jpg){ #fig:009 width=60% }

6. Запускаю созданную виртуальную машину и начинаю установку (рис.10). Выбираю язык, который буду использовать в процессе установки: русский язык (рис. 11). 

   ![рис.10. Запуск машины, выбор установки.](images/10.jpg){ #fig:010 width=60% }

   ![рис.11. Выбор языка.](images/11.jpg){ #fig:011 width=60% }

7. Провожу конфигурацию параметров будущей ОС в соответствии с требованиями (рис. 12):
	- дата и время: выбираю москвский часовой пояс (рис. 13)
	- язык для клавиатуры и языковой поддержки: оставляю русский язык (рис. 14)
	- источник установки: локальный носитель (рис. 15)
	- выбор программы: выбираю сервер с GUI (средства разработки) (рис. 16)
	- расположение установки: автоматическое разбиение диска (рис. 17)
	- KDUMP: kdump отключен (рис. 18)
	- сеть и имя узла: включила сеть и задала имя узла со своим именем (рис. 19)
	- security policy: no content found (рис. 20)

   ![рис.12. ](images/12.jpg){ #fig:012 width=60% }

   ![рис.13. Выбор часового пояса.](images/13.jpg){ #fig:013 width=60% }

   ![рис.14. Выбор языка для клавиатуры и языковой поддержки.](images/14.jpg){ #fig:014 width=60% }

   ![рис.15. Настройка источника установки.](images/15.jpg){ #fig:015 width=60% }

   ![рис.16. Выбор программ.](images/16.jpg){ #fig:016 width=60% }

   ![рис.17. Место установки.](images/17.jpg){ #fig:017 width=60% }

   ![рис.18. KDUMP](images/18.jpg){ #fig:018 width=60% }

   ![рис.19. Сеть и имя узла. Задание сетевого имени виртуальной машины.](images/19.jpg){ #fig:019 width=60% }

   ![рис.20. Security policy](images/20.jpg){ #fig:020 width=60% }

8. Создаю нового пользователя с правами администратора, задаю пароль (рис.21-23).

   ![рис.21. Установка пароля для root.](images/21.jpg){ #fig:021 width=60% }

   ![рис.22. Создание пользователя с правами администратора.](images/22.jpg){ #fig:022 width=60% }

   ![рис.23. Заданные пароль и пользователь.](images/23.jpg){ #fig:023 width=60% }

9. Продолжаю установку операционной системы, перезагружаю виртуальную машину по требованию установщика. Принимаю лицензионное соглашение (рис.24).

   ![рис.24. Лицензионное соглашение.](images/24.jpg){ #fig:024 width=60% }

10. Вхожу в созданный ранее профиль, открывается привычный графический интерфейс (рис.25).

   ![рис.25. Вход в профиль. Ввод пароля.](images/25.jpg){ #fig:025 width=60% }

11. Произвожу установку драйверов. Для этого заходим в устройства -> подключить образ диска Дополнительной гостевой ОС (рис. 26), нажимаем запустить (рис. 27) и вводим пароль (рис. 28). происходит установка (рис. 29).

   ![рис.26. Виртуальная машина Base. Подключить образ диска Дополнительной гостевой ОС.](images/26.jpg){ #fig:026 width=60% }

   ![рис.27. Согласие на запуск приложения.](images/27.jpg){ #fig:027 width=60% }

   ![рис.28. Ввод пароля. Подтверждение административных прав.](images/28.jpg){ #fig:028 width=60% }

   ![рис.29. Установка дрйверов.](images/29.jpg){ #fig:029 width=60% }

12. После установки выполняю перезагрузку (рис. 30).

   ![рис.30. Перезагрузка.](images/30.jpg){ #fig:030 width=60% }

13. Открываю терминал, перехожу на **_root_** пользователя командой _su_, обновляю системные файлы _yum update_, устанавливаю mc командой _yum install mc_ (рис.31-33).

   ![рис.31. Терминал. Переход на root пользователя. Начало выполнения команды yum update.](images/31.jpg){ #fig:031 width=60% }

   ![рис.32. Терминал. Успешное обновление системных файлов. Начало выполнения команды yum install mc.](images/32.jpg){ #fig:032 width=60% }

   ![рис.33. Терминал. Успешная установка mc.](images/33.jpg){ #fig:033 width=60% }

14. Завершаю работу виртуальной машины (рис. 34).

   ![рис.34. Завершение работы виртуальной машины.](images/34.jpg){ #fig:034 width=60% }

15. Освобождаю «Base.dvi»,чтобы другие виртуальные машины могли использовать машину Base и её конфигурацию как базовую (рис. 35).

   ![рис.35. Освобождение Base.dvi.](images/35.jpg){ #fig:035 width=60% }

16. На основе виртуальной машины Base создаем машину Host2, выбрав в качестве диска существующий жёсткий диск (рис. 36-37).

   ![рис.36. Создание виртуальной маришины Host2.](images/36.jpg){ #fig:036 width=60% }

   ![рис.37. Выбор жёсткого диска для Host2.](images/37.jpg){ #fig:037 width=60% }

# Выводы

Приобрела практические навыки установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.
