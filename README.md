# Обучающие материалы по питону

## Курсы лекций

1. Специализация Программирование на Python от МФТИ и Mail.Ru Group (все курсы хорошие) https://www.coursera.org/specializations/programming-in-python
2. Академия Яндекса, Школа бэкенд-разработки 2019 на питоне https://www.youtube.com/playlist?list=PLQC2_0cDcSKBHamFYA6ncnc_fYuEQUy0s
3. Computer Science Center, Программирование на Python, осень 2018, Преподаватель курса: Алексей Александрович Кладов https://www.youtube.com/playlist?list=PLlb7e2G7aSpQhNphPSpcO4daaRPeVstku
4. Computer Science Center, Python, 2016, Преподаватель курса: Сергей Лебедев https://www.youtube.com/playlist?list=PLlb7e2G7aSpTTNp7HBYzCBByaE1h54ruW
5. Технострим Mail.Ru Group, Прикладной Python (осень 2018) https://www.youtube.com/playlist?list=PLrCZzMib1e9qM62lMXC90SiFy7-1-kAPJ

## По темам (+ краткий конспект)

### Внутренности питона

> Разбор кода на токены -> построение AST -> оптимизации -> генерация байткода -> выполнение байткода в виртуальной машине

1. Что внутри у Питона: как работает интерпретатор https://www.youtube.com/watch?v=at30AmjPsy4
2. Внутреннее устройство интерпретатора CPython https://www.youtube.com/watch?v=O9LeNPiftgk
3. Внутри виртуальной машины Python. Часть 1 https://habr.com/ru/post/501338/ (ч1), https://habr.com/ru/post/501920/ (ч2)
4. Your Guide to the CPython Source Code (Real python) https://realpython.com/cpython-source-code-guide/
5. Внутреннее устройство интерпретатора CPython (урок от Otus) https://www.youtube.com/watch?v=O9LeNPiftgk
6. Устройство CPython. Лекция из Академии Яндекса https://www.youtube.com/watch?v=PxIqLgjtQ5Y&list=PLQC2_0cDcSKBHamFYA6ncnc_fYuEQUy0s
7. Understanding Python Bytecode. Learn about disassembling Python bytecode (Reza Bagheri) https://towardsdatascience.com/understanding-python-bytecode-e7edaae8734d

### Типы данных. Коллекции

### Циклы, условия, операторы

### Возможности стандартной библиотеки

### Итераторы и генераторы. Сопрограммы

### Декораторы
> Часто используемый шаблон проектирования в питоне, для которого есть даже специальный синтаксический сахар `@deco\nmethod` - то же самое что `method=deco(method)` как мы написали бы на других ЯП. В декораторы можно передавать аргументы.
1. Лекция по ООП и декораторам от Акадении Яндекса https://youtu.be/Db19qjrMsYI?t=2596

### ООП и магические методы
> Все в питоне является объектом. Питон поддерживает множественное наследование, при этом порядок выбора метода определяется алгоритмом MRO. Соглашение об именовании методов (`_method` - приватный атрибут, `__method` - искажение имени для избежания конфликтов наследников). Магические методы `__method__` - задают поведение объекта с операторами, стандартными функциями, при доступе к атрибутам и т.д.
1. ООП. Лекция Академии Яндекса https://www.youtube.com/watch?v=Db19qjrMsYI
2. Руководство по магическим методам в Питоне (перевод статьи Rafe Kettler) https://habr.com/ru/post/186608/

### Дебаггинг

### Профайлинг 
1. Flamegraph семплирующий профайлинг https://www.youtube.com/watch?v=kRA0RZoycMQ
2. PyConBY 2020: Christian Heimes - Introduction to low level profiling and tracing https://www.youtube.com/watch?v=PXEP97uU0NQ

### GUI
1. Серия статей Python GUI Programming (RealPython). Обзор библиотек PySimpleGUI, Tkinter, PyQt, wxPython https://realpython.com/learning-paths/python-gui-programming/ 

### Пакеты

### Тестирование
1. Введение в автотесты. Вебинар от OTUS https://www.youtube.com/watch?v=EBMXOsCL9AA
2. Тестирование. Лекция из Академии Яндекса https://www.youtube.com/watch?v=2-EBSIRs0H4&list=PLQC2_0cDcSKBHamFYA6ncnc_fYuEQUy0s&index=4

### Event loop. Теория

### Асинхронные фреймворки
1. Дмитрий Ходаков, Авито «Tornado vs Aiohttp» https://www.youtube.com/watch?v=BbyVHtsIM1M (и статья https://habr.com/ru/company/avito/blog/435532/)

### Многопоточность. GIL. Многопроцессные приложения
1. Многопоточность и GIL. Лекция от Computer Science center https://www.youtube.com/watch?v=nR8WhdcRJwM
2. What is the Python Global Interpreter Lock (GIL)? https://realpython.com/python-gil/
3. 

### Модули на C

### WCGI

### Работа с СУБД. Драйверы. Популярные ORM

### Библиотеки NumPy и Pandas
1. Python NumPy Tutorial for Beginners (Freecodecamp.org) https://www.youtube.com/watch?v=QUT1VHiLmmI

### Автоматические утилиты для улучшения качества кода
1. Python Code Quality: Tools & Best Practices https://realpython.com/python-code-quality/
2. Как прокачать линтер. Максим Мазаев https://www.youtube.com/watch?v=HZPRoz8V6jk

## Полезные книги

## Telegram-каналы

##  Митапы и конференции
1. Moscow python meetup (+ Moscow python conf) https://www.youtube.com/user/moscowdjangoru
2. Minsk python meetup https://www.youtube.com/user/pythonMinsk 
3. Python Meetup Chelyabinsk https://www.youtube.com/channel/UCpMh_XSn7yGPabFBYzY5hKg

