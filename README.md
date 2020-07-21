# Обучающие материалы по питону

## Курсы лекций

1. Специализация Программирование на Python от МФТИ и Mail.Ru Group (все курсы хорошие) https://www.coursera.org/specializations/programming-in-python
2. Академия Яндекса, Школа бэкенд-разработки 2019 на питоне https://www.youtube.com/playlist?list=PLQC2_0cDcSKBHamFYA6ncnc_fYuEQUy0s
3. Computer Science Center, Программирование на Python, осень 2018, Преподаватель курса: Алексей Александрович Кладов https://www.youtube.com/playlist?list=PLlb7e2G7aSpQhNphPSpcO4daaRPeVstku
4. Computer Science Center, Python, 2016, Преподаватель курса: Сергей Лебедев https://www.youtube.com/playlist?list=PLlb7e2G7aSpTTNp7HBYzCBByaE1h54ruW
5. Технострим Mail.Ru Group, Прикладной Python (осень 2018) https://www.youtube.com/playlist?list=PLrCZzMib1e9qM62lMXC90SiFy7-1-kAPJ

## По темам (+ краткий конспект)

### Внутренности питона

> Разбор кода на токены -> построение AST -> оптимизации -> генерация байткода -> выполнение байткода в виртуальной машине. Стандартный интерпретатор - cpython (написан на языке C https://github.com/python/cpython). Альтернативные - pypy (написан на питоне, с JIT), ironpython (C#) и jython(java) - под специфические задачи, не без проблем и особым спросом не пользуются. Для решения проблем и получения ответов на свои вопросы полезно 1) уметь разбирать байткод 2) знать структуру cpython и уметь читать сишный код

1. Что внутри у Питона: как работает интерпретатор https://www.youtube.com/watch?v=at30AmjPsy4
2. Внутреннее устройство интерпретатора CPython https://www.youtube.com/watch?v=O9LeNPiftgk
3. Внутри виртуальной машины Python. https://habr.com/ru/post/501338/ (ч1), https://habr.com/ru/post/501920/ (ч2)
4. Your Guide to the CPython Source Code (Real python) https://realpython.com/cpython-source-code-guide/
5. Внутреннее устройство интерпретатора CPython (урок от Otus) https://www.youtube.com/watch?v=O9LeNPiftgk
6. Устройство CPython. Лекция из Академии Яндекса https://www.youtube.com/watch?v=PxIqLgjtQ5Y&list=PLQC2_0cDcSKBHamFYA6ncnc_fYuEQUy0s
7. Understanding Python Bytecode. Learn about disassembling Python bytecode (Reza Bagheri) https://towardsdatascience.com/understanding-python-bytecode-e7edaae8734d

### Типы данных. Коллекции
> Все в питоне является объектом. Чтобы узнать тип объекта `x`, нужно вызвать `type(x)`, список методов и свойств - `dir(x)`, справку по методу - `help(x.some_method)`
1. Basic Data Types in Python (real python) https://realpython.com/python-data-types/
2. Dictionaries in Python (real python) https://realpython.com/python-dicts/
3. Sets in Python (real python) https://realpython.com/python-sets/
4. Lists and Tuples in Python (real python) https://realpython.com/python-lists-tuples/
5. Linked Lists in Python: An Introduction (real python) https://realpython.com/linked-lists-python/
6. Strings and Character Data in Python (real python) https://realpython.com/python-strings/ 

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
> Для питона есть консольный дебаггер - pdb, а также дебаггеры в популярных IDE
1. Python Debugging With Pdb (Real python) https://realpython.com/python-debugging-pdb/
2. Advanced Debugging in PyCharm (JetBrains) https://www.youtube.com/watch?v=k6j1NkVAsuU
3. Как устроены дебаггеры (доклад Елизаветы Шашковой на pycon) https://www.youtube.com/watch?v=jK3D77b-DXk

### Профайлинг 
> Как и для других ЯП, для питона существует ряд статистических (низкий оверхед и более низкая точность) и инструментальных (более высокая точность и высокий оверхед) профилировщиков
1. Flamegraph семплирующий профайлинг https://www.youtube.com/watch?v=kRA0RZoycMQ
2. PyConBY 2020: Christian Heimes - Introduction to low level profiling and tracing https://www.youtube.com/watch?v=PXEP97uU0NQ
3. Summary Of Python Profiling Tools http://pramodkumbhar.com/2019/05/summary-of-python-profiling-tools-part-i/ (на этом сайте есть еще хорошие статьи о производительности)

### GUI
> На питоне можно разрабатывать программы с графическим интерфейсом - для этого есть несколько популярных библиотек
1. Серия статей Python GUI Programming (RealPython). Обзор библиотек PySimpleGUI, Tkinter, PyQt, wxPython https://realpython.com/learning-paths/python-gui-programming/ 
2. Python GUI: создаём простое приложение с PyQt и Qt Designer (tproger) https://tproger.ru/translations/python-gui-pyqt/
3. 13 GUI-библиотек Python https://techrocks.ru/2018/04/26/13-python-gui-frameworks/
4. Серия статей о PyQT5 с примерами http://zetcode.com/gui/pyqt5/
5. Tkinter Course - Create Graphic User Interfaces in Python Tutorial (freecodecamp) https://www.youtube.com/watch?v=YXPyB4XeYLA

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
2. Как прокачать линтер. Максим Мазаев https://www.youtube.com/watch?v=HZPRoz8V6jk (этот же доклад https://www.youtube.com/watch?v=ZKoBZkdYLiM и статья https://habr.com/ru/company/oleg-bunin/blog/433474/)
3. Презентация "HOW TO WRITE PYLINT PLUGINS" Александра Тодорова https://piterpy.com/system/attachments/files/000/001/519/original/how_to_write_pylint_plugins_PiterPy_2018.pdf  

## Полезные книги

## Telegram-каналы

##  Митапы и конференции
1. Moscow python meetup (+ Moscow python conf) https://www.youtube.com/user/moscowdjangoru
2. Minsk python meetup https://www.youtube.com/user/pythonMinsk 
3. Python Meetup Chelyabinsk https://www.youtube.com/channel/UCpMh_XSn7yGPabFBYzY5hKg

