
---
# Front matter
title: "Отчет по лабораторной работе"  
subtitle: "Работа с git"  
author: "Воробьев Александр Олегович"  
group: "NFIbd-01-19"

# Generic otions
lang: ru-RU
toc-title: "Содержание"

# Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

# Pdf output format
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
### Fonts
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
## Misc options
indent: true
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

Изучить принципы работы с git.

# Задание

Включает в себя выполнение следующих пунктов:  
- Подготовка рабочей среды 
- Создание проекта
- Внесение изменений в файл
- Индексация изменений
- Отмена локальных изменений (до индексации)
- Отмена проиндексированных изменений (перед коммитом)
- Отмена коммитов
- Удаление коммиттов из ветки
- Удаление тега oops
- Внесение изменений в коммиты
- Перемещение файлов
- Второй способ перемещения файлов
- Подробное рассмотрение структуры
- Git внутри: Каталог .git
- Работа непосредственно с объектами git
- Создание ветки
- Навигация по веткам
- Изменения в ветке master
- Коммит изменений файла в другую ветку
- Слияние веток
- Создание конфликта
- Разрешение конфликтов
- Сброс ветки
- Сброс ветки master
- Перебазирование
- Слияние в ветку master
- Клонирование репозиториев
- Просмотр клонированного репозитория
- Что такое origin?
- Удаленные ветки
- Изменение оригинального репозитория
- Слияние извлеченных изменений
- Добавление ветки наблюдения
- Чистые репозитории
- Создание чистого репозитория
- Добавление удаленного репозитория
- Отправка изменений
- Извлечение общих изменений

# Теоретическое введение

Git - распределённая система управления версиями. 

| Имя каталога | Описание каталога                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `/`          | Корневая директория, содержащая всю файловую                                                                               |
| `/bin `      | Основные системные утилиты, необходимые как в однопользовательском режиме, так и при обычной работе всем пользователям     |
| `/etc`       | Общесистемные конфигурационные файлы и файлы конфигурации установленных программ                                           |
| `/home`      | Содержит домашние директории пользователей, которые, в свою очередь, содержат персональные настройки и данные пользователя |
| `/media`     | Точки монтирования для сменных носителей                                                                                   |
| `/root`      | Домашняя директория пользователя  `root`                                                                                   |
| `/tmp`       | Временные файлы                                                                                                            |
| `/usr`       | Вторичная иерархия для данных пользователя                                                                                 |


# Выполнение лабораторной работы

1.1.1 Установка имени и электронной почты  
![рис. 1](screen/ph1.png)

1.1.2 Параметры установки окончаний строк  
![рис. 2](screen/ph2.png)

1.1.3 Установка отображения unicode  
![рис. 3](screen/ph3.png)

1.2.1 Создайте страницу «Hello, World»  
![рис. 4](screen/ph4.png)

1.2.2 Создание репозитория  
![рис. 5](screen/ph5.png)

1.2.3 Добавление файла в репозиторий    
![рис. 6](screen/ph6.png)

1.2.4 Проверка состояния репозитория  
Команда git status  

1.3.1 Измените страницу «Hello, World»  
![рис. 7](screen/ph7.png)  
![рис. 8](screen/ph8.png)  
Проверили статус рабочего каталога  
![рис. 9](screen/ph9.png)

1.4 Индексация изменений  
![рис. 10](screen/ph10.png)  

1.4.1 Коммит изменений  
![рис. 11](screen/ph11.png)

1.4.2 Добавьте стандартные теги страницы  
![рис. 12](screen/ph12.png)  
![рис. 13](screen/ph13.png)  
![рис. 14](screen/ph14.png)  
![рис. 15](screen/ph15.png)  
![рис. 16](screen/ph16.png)  

1.4.3 История  
![рис. 17](screen/ph17.png)

1.4.4 Получение старых версий  
![рис. 18](screen/ph18.png)

1.4.5 Создание тегов версий  
![рис. 19](screen/ph19.png)

1.4.6 Переключение по имени тега  
![рис. 20](screen/ph20.png)

1.4.7 Просмотр тегов с помощью команды tag  
![рис. 21](screen/ph21.png)

1.5.1 Переключитесь на ветку master  
![рис. 22](screen/ph22.png)

1.5.2 Измените hello.html  
![рис. 23](screen/ph23.png)

1.5.3 Проверьте состояние  
![рис. 24](screen/ph24.png)

1.5.4 Отмена изменений в рабочем каталоге  
![рис. 25](screen/ph25.png)

1.6.1 Измените файл и проиндексируйте изменения  
![рис. 26](screen/ph26.png)  
![рис. 27](screen/ph27.png)

1.6.2 Проверьте состояние  
![рис. 28](screen/ph28.png)

1.6.3 Выполните сброс буферной зоны  
![рис. 29](screen/ph29.png)

1.6.4 Переключитесь на версию коммита  
![рис. 30](screen/ph30.png)

1.7.2 Измените файл и сделайте коммит  
![рис. 31](screen/ph31.png)  
![рис. 32](screen/ph32.png)

1.7.3 Сделайте коммит с новыми изменениями, отменяющими предыдущие  
![рис. 33](screen/ph33.png)  
![рис. 34](screen/ph34.png)

1.7.4 Проверьте лог  
![рис. 35](screen/ph35.png)

1.8.3 Для начала отметьте эту ветку  
![рис. 36](screen/ph36.png)

1.8.4 Сброс коммитов к предшествующим коммиту Oops  
![рис. 37](screen/ph37.png)

1.8.5 Ничего никогда не теряется  
![рис. 38](screen/ph38.png)

1.9.1 Удаление тега oops  
![рис. 39](screen/ph39.png)

1.10.1 Измените страницу, а затем сделайте коммит  
![рис. 40](screen/ph40.png)  
![рис. 41](screen/ph41.png)

1.10.2 Необходим email  
![рис. 42](screen/ph42.png)

1.10.3 Измените предыдущий коммит  
![рис. 43](screen/ph43.png)

1.10.4 Просмотр истории  
![рис. 44](screen/ph44.png)

1.11.1 Переместите файл hello.html в каталог lib  
1.12.1 Коммит в новый каталог  
![рис. 45](screen/ph45.png)

1.13.1 Добавление index.html  
![рис. 46](screen/ph46.png)  
![рис. 47](screen/ph47.png)

1.14.1 Каталог.git  
![рис. 48](screen/ph48.png)

1.14.2 База данных объектов  
![рис. 49](screen/ph49.png)

1.14.3 Углубляемся в базу данных объектов  
![рис. 50](screen/ph50.png)

1.14.4 Config File  
![рис. 51](screen/ph51.png)  
![рис. 52](screen/ph52.png)

1.14.6 Файл HEAD  
![рис. 53](screen/ph53.png)

1.15.1 Поиск последнего коммита  
![рис. 54](screen/ph54.png)

1.15.2 Вывод последнего коммита с помощью SHA1 хэша  
![рис. 55](screen/ph55.png)

1.15.3 Поиск дерева, 1.15.4 Вывод каталога lib, 1.15.5 Вывод файла hello.html  
![рис. 56](screen/ph56.png)

1.16.1 Создайте ветку  
![рис. 57](screen/ph57.png)

1.16.2 Добавьте файл стилей style.css  
![рис. 58](screen/ph58.png)  
![рис. 59](screen/ph59.png)

1.16.3 Измените основную страницу  
![рис. 60](screen/ph60.png)  
![рис. 61](screen/ph61.png)

1.16.4 Измените index.html  
![рис. 62](screen/ph62.png)  
![рис. 63](screen/ph63.png)

1.17 Навигация по веткам  
![рис. 64](screen/ph64.png)

1.17.1 Переключение на ветку master  
![рис. 65](screen/ph65.png)

1.17.2 Вернемся к ветке style  
![рис. 66](screen/ph66.png)

1.18.1 Создайте файл README в ветке master  
![рис. 67](screen/ph67.png)

1.19 Сделайте коммит изменений README.md в ветку master  
![рис. 68](screen/ph68.png)

1.19.2 Просмотрите текущие ветки  
![рис. 69](screen/ph69.png)

1.20.1 Слияние веток  
![рис. 70](screen/ph70.png)  
![рис. 71](screen/ph71.png)  
![рис. 72](screen/ph72.png)

1.21.1 Вернитесь в master и создайте конфликт  
![рис. 73](screen/ph73.png)  
![рис. 74](screen/ph74.png)

1.21.2 Просмотр веток  
![рис. 75](screen/ph75.png)

1.22.1 Слияние master с веткой style  
![рис. 76](screen/ph76.png)  
![рис. 77](screen/ph77.png)  

1.22.2 Решение конфликта  
![рис. 78](screen/ph78.png)

1.22.3 Сделайте коммит решения конфликта  
![рис. 79](screen/ph79.png)

1.23.1 Сброс ветки style  
![рис. 80](screen/ph80.png)  
![рис. 81](screen/ph81.png)

1.23.2 Проверьте ветку  
![рис. 82](screen/ph82.png)

1.24.1 Сброс ветки master  
![рис. 83](screen/ph83.png)  
![рис. 84](screen/ph84.png)

1.25 Перебазирование  
![рис. 85](screen/ph85.png)

1.26.1 Слияние style в master  
![рис. 86](screen/ph86.png)

1.26.2 Просмотрите логи  
![рис. 87](screen/ph87.png)

1.27.1 Перейдите в рабочий каталог  
![рис. 88](screen/ph88.png)

1.27.2 Создайте клон репозитория hello  
![рис. 89](screen/ph89.png)

1.28.1 Давайте взглянем на клонированный репозиторий  
![рис. 90](screen/ph90.png)

1.28.2 Просмотрите историю репозитория  
![рис. 91](screen/ph91.png)

1.29 Что такое origin?  
![рис. 92](screen/ph92.png)

1.30 Удаленные ветки  
![рис. 93](screen/ph93.png)

1.30.1 Список удаленных веток  
![рис. 94](screen/ph94.png)

1.31.1 Внесите изменения в оригинальный репозиторий hello  
![рис. 95](screen/ph95.png)  
![рис. 96](screen/ph96.png)

1.31.2 Извлечение изменений  
![рис. 97](screen/ph97.png)  
![рис. 98](screen/ph98.png)

1.31.3 Проверьте README.md  
![рис. 99](screen/ph99.png)

1.32.1 Слейте извлеченные изменения в локальную ветку master  
![рис. 100](screen/ph100.png)

1.32.2 Еще раз проверьте файл README.md  
![рис. 101](screen/ph101.png)

1.33.1 Добавьте локальную ветку, которая отслеживает удаленную ветку  
![рис. 102](screen/ph102.png)

1.35 Создайте чистый репозиторий  
![рис. 103](screen/ph103.png)

1.36 Добавление удаленного репозитория  
![рис. 104](screen/ph104.png)

1.37 Отправка изменений  
![рис. 105](screen/ph105.png)  
![рис. 106](screen/ph106.png)

1.38 Извлечение общих изменений  
![рис. 107](screen/ph107.png)

# Выводы

В результате выполнения работы я научился работать с консольной утилитой git. Понял как вести и отслеживать историю изменения файлов в проекте. 

# Список литературы{.unnumbered}

Кулябов Д.С. Работа с git. - 31 c.  