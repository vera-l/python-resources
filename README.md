# Обучающие материалы по питону (roadmap)

## Курсы лекций

1. Специализация Программирование на Python от МФТИ и Mail.Ru Group (все курсы хорошие) https://www.coursera.org/specializations/programming-in-python
2. Академия Яндекса, Школа бэкенд-разработки 2019 на питоне https://www.youtube.com/playlist?list=PLQC2_0cDcSKBHamFYA6ncnc_fYuEQUy0s
3. Computer Science Center, Программирование на Python, осень 2018, Преподаватель курса: Алексей Александрович Кладов https://www.youtube.com/playlist?list=PLlb7e2G7aSpQhNphPSpcO4daaRPeVstku
4. Computer Science Center, Python, 2016, Преподаватель курса: Сергей Лебедев https://www.youtube.com/playlist?list=PLlb7e2G7aSpTTNp7HBYzCBByaE1h54ruW
5. Технострим Mail.Ru Group, Прикладной Python (осень 2018) https://www.youtube.com/playlist?list=PLrCZzMib1e9qM62lMXC90SiFy7-1-kAPJ
6. 

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
8. Жизненный цикл кода на Python – модель выполнения CPython (Otus) https://habr.com/ru/company/otus/blog/442252/
9. Официальная документация по модулю `dis` и список байткод-инструкций https://docs.python.org/3/library/dis.html#python-bytecode-instructions
10. HOW to use AST (Kamnee Maran) https://medium.com/@kamneemaran45/python-ast-5789a1b60300
11. Online python ast explorer https://python-ast-explorer.com/
12. Знай и люби свой CPython во имя луны и великой справедливости, Александр Кошкин https://www.youtube.com/watch?v=0_5_zEOo8kg

### Типы данных. Коллекции
> Все в питоне является объектом. Чтобы узнать тип объекта `x`, нужно вызвать `type(x)`, список методов и свойств - `dir(x)`, справку по методу - `help(x.some_method)`
1. Basic Data Types in Python (real python) https://realpython.com/python-data-types/
2. Dictionaries in Python (real python) https://realpython.com/python-dicts/
3. Sets in Python (real python) https://realpython.com/python-sets/
4. Lists and Tuples in Python (real python) https://realpython.com/python-lists-tuples/
5. Linked Lists in Python: An Introduction (real python) https://realpython.com/linked-lists-python/
6. Strings and Character Data in Python (real python) https://realpython.com/python-strings/ 
7. Модуль collections из стандартной библиотеки https://habr.com/ru/post/478934/
8. The Python heapq Module: Using Heaps and Priority Queues (real python) https://realpython.com/python-heapq-module/

### Циклы, условия, операторы
> Поведение объектов с тем или иным оператором определяется реализацией у него соответствующего магического метода.
1. Operators and Expressions in Python (real python) https://realpython.com/python-operators-expressions/
2. Operator and Function Overloading in Custom Python Classes (real python) https://realpython.com/operator-function-overloading/
3. Conditional Statements in Python (real python) https://realpython.com/python-conditional-statements/
4. Python "while" Loops (Indefinite Iteration) (real python) https://realpython.com/python-while-loop/
5. Python "for" Loops (Definite Iteration) (real python)  https://realpython.com/python-for-loop/
6. Список операторов (официальная документация) https://docs.python.org/3/library/operator.html

### Итераторы и генераторы. Сопрограммы

### Функции. Замыкания. Декораторы
> Часто используемый шаблон проектирования в питоне, для которого есть даже специальный синтаксический сахар `@deco\nmethod` - то же самое что `method=deco(method)` как мы написали бы на других ЯП. В декораторы можно передавать аргументы.
1. Лекция по ООП и декораторам от Акадении Яндекса https://youtu.be/Db19qjrMsYI?t=2596
2. Функциональное программирование и работа с данными (+ декораторы) (урок OTUS) https://www.youtube.com/watch?v=iHT2OlrCBgs
3. Скринкаст Олега Молчанова по декораторам https://www.youtube.com/watch?v=Ss1M32pp5Ew
4. 

### ООП. Магические методы. Протокол дескрипторов. Метаклассы
> Все в питоне является объектом. Питон поддерживает множественное наследование, при этом порядок выбора метода определяется алгоритмом MRO. Соглашение об именовании методов (`_method` - приватный атрибут, `__method` - искажение имени для избежания конфликтов наследников). Магические методы `__method__` - задают поведение объекта с операторами, стандартными функциями, при доступе к атрибутам и т.д.
1. ООП. Лекция Академии Яндекса https://www.youtube.com/watch?v=Db19qjrMsYI
2. Руководство по магическим методам в Питоне (перевод статьи Rafe Kettler) https://habr.com/ru/post/186608/
3. Магические методы и дескрипторы (урок Otus) https://www.youtube.com/watch?v=6Zd35hSvGio
4. Руководство к дескрипторам (хабр) https://habr.com/ru/post/122082/
5. Дескрипторы (В. Донец) https://www.youtube.com/watch?v=akyVo4BzYZo
6. Алексей Кузьмин. Жизненный цикл Python-объекта https://www.youtube.com/watch?v=UndKVhoMNg8

### Возможности стандартной библиотеки
> У питона богатейшая стандартная библиотека. Там есть все, что нужно и даже больше
1. Официальная документация https://docs.python.org/3/library/
2. Python 3 Module of the Week (по частям с примерами) https://pymotw.com/3/

### Дебаггинг
> Для питона есть консольный дебаггер - pdb, а также дебаггеры в популярных IDE
1. Python Debugging With Pdb (Real python) https://realpython.com/python-debugging-pdb/
2. Advanced Debugging in PyCharm (JetBrains) https://www.youtube.com/watch?v=k6j1NkVAsuU
3. Как устроены дебаггеры (доклад Елизаветы Шашковой на pycon) https://www.youtube.com/watch?v=jK3D77b-DXk
4. Отладка Python (статья от mail.ru с обзором дебаггеров) https://habr.com/ru/company/mailru/blog/205426/

### Обработка исключений
1. Python Exceptions: An Introduction https://realpython.com/python-exceptions/
2. Understanding the Python Traceback https://realpython.com/python-traceback/
3. Python KeyError Exceptions and How to Handle Them https://realpython.com/python-keyerror/
3. Devpractice Работа с исключениями https://devpractice.ru/python-lesson-11-work-with-exceptions/
4. Григорий Петров: "Работа с ошибками. Как ловить исключения и что потом с ними делать." https://www.youtube.com/watch?v=hzVECcMI8ys

### Пакеты и модули. Pypi. pip и easy_install. virtualenv
1. Ликбез по пакетам и шпаргалка по модулям в Python (Хекслет) https://ru.hexlet.io/blog/posts/likbez-po-paketam-i-shpargalka-po-modulyam-v-python
2. Python Modules and Packages – An Introduction (real python) https://realpython.com/python-modules-packages/
3. How to Publish an Open-Source Python Package to PyPI (real python) https://realpython.com/pypi-publish-python-package/
4. Dependencies Handling in Python (Julien Danjou) https://julien.danjou.info/dependencies-handling-in-python-automatic-update/

### Многопоточность. GIL. Многопроцессные приложения
1. Многопоточность и GIL. Лекция от Computer Science center https://www.youtube.com/watch?v=nR8WhdcRJwM
2. What is the Python Global Interpreter Lock (GIL)? https://realpython.com/python-gil/
3. An Intro to Threading in Python (real python) https://realpython.com/intro-to-python-threading/
4. GIL (урок Otus) https://www.youtube.com/watch?v=hCOmbMRsJ8c
5. GIL в Python: зачем он нужен и как с этим жить - Доклад Г. Петрова https://www.youtube.com/watch?v=AWX4JnAnjBE
6. Злата Обуховская, Nvidia «Structured Concurrency. Что не так с асинхронностью в питоне?» https://www.youtube.com/watch?v=NmWzt7VdTgA

### Асинхронное программирование. Event loop. Теория
1. Асинхронное программирование в Python (урок OTUS) https://www.youtube.com/watch?v=LROBh6pgEp8
2. async / await - лекция от Computer Science Center https://www.youtube.com/watch?v=x6JZmBK2I8Y
3. Асинхронное программирование - Лекция Академии Яндекса https://www.youtube.com/watch?v=AXkOli6BsBY (ч.1), https://www.youtube.com/watch?v=IB4bJqmfjI0 (ч.2), https://www.youtube.com/watch?v=FFUYf8FHDlY (ч.3)
4. Demystifying Python's Async and Await Keywords от JetBrainsTV https://www.youtube.com/watch?v=F19R_M4Nay4
5. Алексей Кузьмин, ДомКлик «Асинхронность изнутри» https://www.youtube.com/watch?v=pZkerqks43Y
6. Доклад Д. Бизли Конкурентность в Питоне с нуля. Вживую. https://www.youtube.com/watch?v=ys8lW8eQaJQ
7. Аsync и await в production / Сергей Борисов (ДомКлик) https://www.youtube.com/watch?v=pN9A5kD_rK8
8. Основы асинхронности в Python - Курс лекций Олега Молчанова https://www.youtube.com/watch?v=ZGfv_yRLBiY
9. Что внутри у питона: откуда быть пошел async (доклад З. Обуховской, также рассказано про генераторы) https://www.youtube.com/watch?v=GX7AUAwpQ4I
10. Школа программистов HH: Python Async (Р. Чекалов) https://www.youtube.com/watch?v=VWEISe8TXUE
11. Дмитрий Ходаков, Avito «CPU bound задачи в веб-сервисах на Python» https://www.youtube.com/watch?v=OmBuXb7P9Ak

### Асинхронные фреймворки и библиотеки
1. Дмитрий Ходаков, Авито «Tornado vs Aiohttp» https://www.youtube.com/watch?v=BbyVHtsIM1M (и статья https://habr.com/ru/company/avito/blog/435532/)
2. Различные асинхронные библиотеки от создателей `asyncio` https://github.com/aio-libs
3. Андрей Светлов, Python Core Developer «Aiohttp от автора» https://www.youtube.com/watch?v=5NrnBu1vcKo
4. Yury Selivanov - Asyncio in Python 3.7 and 3.8 https://www.youtube.com/watch?v=ReXxO_azV-w
5. Самые быстрые Python веб-фреймворки в 2019 (перевод статьи Maksim Larkin) https://habr.com/ru/post/440282/
6. Андрей Светлов: "Подводные камни asyncio" https://www.youtube.com/watch?v=GLN_xo4Awcc

### Работа с памятью
> Питон - очень неэкономный по памяти язык. Иногда возникают задачи, которые требуют знаний про то как питон работает с памятью (счетчик ссылок, арены и GC для циклических ссылок) и как можно эту память сэкономить.
1. «Память и Python. Что надо знать для счастья?» Алексей Кузьмин, ЦНС https://www.youtube.com/watch?v=D0vbuIDOV4c
2. Python потребляет много памяти, или как уменьшить размер объектов. (доклад З.Шибзухова) https://www.youtube.com/watch?v=qUnzGUz_YxE
3. Что внутри у питона: как устроена память (доклад З. Обуховской) https://www.youtube.com/watch?v=lSgoYx06L_s
4. В. Синицын - Python: управление памятью https://www.youtube.com/watch?v=ZxvwZ4fX_qE
5. Nina Zakharenko - Memory Management in Python - The Basics https://www.youtube.com/watch?v=URNdRl97q_0

### Вопросы производительности
> Несмотря на то, что питон - не самый быстрый язык, интерптетатор постоянно оптимизируют
1. Python — это медленно. Почему? https://habr.com/ru/company/ruvds/blog/418823/
2. Что я узнал про оптимизацию в Python (перевод статьи Gregory Szorc's) https://habr.com/ru/company/otus/blog/457942/
3. Which is the fastest version of Python? (статья Anthony Shaw, сравнение 2.7-3.7+pypy) https://hackernoon.com/which-is-the-fastest-version-of-python-2ae7c61a6b2b
4. Оптимизации, сделавшие Python 3.6 быстрее Python 3.5 https://www.youtube.com/watch?v=zMECweCmuA4

### Профайлинг 
> Как и для других ЯП, для питона существует ряд статистических (низкий оверхед и более низкая точность) и инструментальных (более высокая точность и высокий оверхед) профилировщиков
1. Flamegraph семплирующий профайлинг https://www.youtube.com/watch?v=kRA0RZoycMQ
2. PyConBY 2020: Christian Heimes - Introduction to low level profiling and tracing https://www.youtube.com/watch?v=PXEP97uU0NQ
3. Summary Of Python Profiling Tools http://pramodkumbhar.com/2019/05/summary-of-python-profiling-tools-part-i/ (на этом сайте есть еще хорошие статьи о производительности)
4. Профилирование и отладка Python (цикл статей от mail.ru): https://habr.com/ru/company/mailru/blog/201594/ (теория), https://habr.com/ru/company/mailru/blog/201778/ (ручное и статистическое), https://habr.com/ru/company/mailru/blog/202832/ (событийное)
5. Крутой sampling-профайлер (строит флеймграфы также) https://github.com/benfred/py-spy (must-have, так как pyflame больше по поддерживается)
6. Алексей Кузьмин, ДомКлик «Поиск и оптимизация узких мест в Python» https://www.youtube.com/watch?v=tDZHhIiACDA
7. Flamegraph that! Self-service profiling tool for Node and Python services (Ruth Grace Wong) https://www.youtube.com/watch?v=w97I5q0hbkw

### Модули на C и ctypes
1. Building a Python C Extension Module (real python) https://realpython.com/build-python-c-extension-module/
2. Производительность в Python. Легкий путь (o ctypes) https://habr.com/ru/post/157537/ (дока https://docs.python.org/3/library/ctypes.html)
3. Python — Программирование расширений на C https://coderlessons.com/tutorials/python-technologies/vyuchit-piton/python-programmirovanie-rasshirenii-na-c
4. C/C++ из Python (ctypes) (хабр) https://habr.com/ru/post/466499/
5. Как писать модули для питона на C и  go (первый доклад pytup'a) https://youtu.be/tpKs4UVe3Bk?t=487
6. Андрей Светлов - Оптимизация производительности при помощи Cython https://www.youtube.com/watch?v=5-WoT4X17sk

### Тестирование
1. Введение в автотесты. Вебинар от OTUS https://www.youtube.com/watch?v=EBMXOsCL9AA
2. Тестирование. Лекция из Академии Яндекса https://www.youtube.com/watch?v=2-EBSIRs0H4&list=PLQC2_0cDcSKBHamFYA6ncnc_fYuEQUy0s&index=4

### Утилиты для улучшения качества кода
1. Python Code Quality: Tools & Best Practices https://realpython.com/python-code-quality/
2. Как прокачать линтер. Максим Мазаев https://www.youtube.com/watch?v=HZPRoz8V6jk (этот же доклад https://www.youtube.com/watch?v=ZKoBZkdYLiM и статья https://habr.com/ru/company/oleg-bunin/blog/433474/)
3. Презентация "HOW TO WRITE PYLINT PLUGINS" Александра Тодорова https://piterpy.com/system/attachments/files/000/001/519/original/how_to_write_pylint_plugins_PiterPy_2018.pdf  
4. Аннотации типов в Python 3 (урок OTUS) https://youtu.be/I09iX8aoCsw?t=313
5. «Модифицируй это!» или «Больше магии Python с помощью изменения AST» (А. Маршалов) https://www.youtube.com/watch?v=Zv6yT-ytIvg
6. Инструменты для анализа кода Python https://proglib.io/p/python-code-analysis (ч.1), https://proglib.io/p/python-code-analysis-tools (ч.2)
7. Г. Петров PyRe: еще один type checker https://www.youtube.com/watch?v=-Lz81ex3jP8

### WCGI

### Работа с СУБД. Драйверы. Популярные ORM
> Самые популярные ORM для питона - SQLAlchemy и Django ORM. 
1. Introduction to Python SQL Libraries (real python) https://realpython.com/python-sql-libraries/
2. "Let's Build an ORM" - Greg Back (Pyohio 2019) https://www.youtube.com/watch?v=6rw0p9AOYb8
3. Object-relational Mappers (ORMs) (обзор, fullstackpython) https://www.fullstackpython.com/object-relational-mappers-orms.html
4. Python: Работа с базой данных (хабр) https://habr.com/ru/post/321510/ (db-api), https://habr.com/ru/post/322086/ (orm)
5. Асинхронные драйверы для работы с различными БД от создателей `asyncio` https://github.com/aio-libs
6. Список асинхронных драйверов для БД https://github.com/timofurrer/awesome-asyncio#database-drivers
7. SQLAlchemy ORM: удобная работа с базами данных на Python (ITVDN) https://www.youtube.com/watch?v=PAKJpfxeXjc
8. Сравнение технологий aiopg & asyncpg, Алексей Фирсов / PyDaCon meetup https://www.youtube.com/watch?v=bY6ZU0-26TA

### Библиотеки NumPy и Pandas
1. Python NumPy Tutorial for Beginners (Freecodecamp.org) https://www.youtube.com/watch?v=QUT1VHiLmmI

### GUI
> На питоне можно разрабатывать программы с графическим интерфейсом - для этого есть несколько популярных библиотек
1. Серия статей Python GUI Programming (RealPython). Обзор библиотек PySimpleGUI, Tkinter, PyQt, wxPython https://realpython.com/learning-paths/python-gui-programming/ 
2. Python GUI: создаём простое приложение с PyQt и Qt Designer (tproger) https://tproger.ru/translations/python-gui-pyqt/
3. 13 GUI-библиотек Python https://techrocks.ru/2018/04/26/13-python-gui-frameworks/
4. Серия статей о PyQT5 с примерами http://zetcode.com/gui/pyqt5/
5. Tkinter Course - Create Graphic User Interfaces in Python Tutorial (freecodecamp) https://www.youtube.com/watch?v=YXPyB4XeYLA

## Must-read книги 
1. Лучано Рамальо: Python. К вершинам мастерства (Fluent Python) https://www.ozon.ru/context/detail/id/135305378/
2. Данжу Джульен: Путь Python. Черный пояс по разработке, масштабированию, тестированию и развертыванию https://www.ozon.ru/context/detail/id/158868396/
3. Бейдер Дэн: Чистый Python. Тонкости программирования для профи https://www.ozon.ru/context/detail/id/146393762/

## Telegram-каналы
1. pythonist.ru (статьи и задачки для собеседований) https://t.me/pythonist_ru
2. Книги https://t.me/python_textbooks
3. Задачки, в основном несложные https://t.me/pythonquestions
4. Англоязычный канал со статьями https://t.me/pythonl
5. Тесты https://t.me/pythontesti
6. Proglib (статьи, не только питон) https://t.me/proglibrary

## Тесты и задачки для проверки знаний
1. Real Python Quizzes https://realpython.com/quizzes/
2. PYnative Python Quizes https://pynative.com/python-quizzes/

##  Митапы и конференции
1. Moscow python meetup (+ Moscow python conf) https://www.youtube.com/user/moscowdjangoru
2. Minsk python meetup https://www.youtube.com/user/pythonMinsk 
3. Python Meetup Chelyabinsk https://www.youtube.com/channel/UCpMh_XSn7yGPabFBYzY5hKg
4. Python Новосибирск https://www.youtube.com/c/PyNSK/
5. PyCon Russia https://www.youtube.com/user/videoitpeople/videos
6. Moscow Python Conf++ https://www.youtube.com/channel/UCqC1iSQnRIDz_rOy8LHe69g
