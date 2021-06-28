
# Обучающие материалы по питону (roadmap) 🐍

<a name="index"></a>
* [Курсы лекций](#courses)
* [Книги онлайн](#books_online)
* [По темам (+ краткий конспект)](#parts)
  * [Внутренности питона](#internals)
  * [Типы данных. Коллекции](#datatypes)
  * [Циклы, условия, операторы](#instructions)
  * [Итераторы и генераторы. Сопрограммы](#iterators)
  * [Функции. Замыкания. Декораторы. ФП](#functions)
  * [ООП. Магические методы. Протокол дескрипторов. Метаклассы. Статические методы и методы класса](#OOP)
  * [Возможности стандартной библиотеки](#stdlib)
  * [Дебаггинг](#debugging)
  * [Обработка исключений. Контекстные менеджеры](#exceptions)
  * [Пакеты и модули. Pypi. pip и easy_install. virtualenv](#modules)
  * [Многопоточность. GIL. Многопроцессные приложения](#gil)
  * [Асинхронное программирование. Event loop. Теория](#async)
  * [Асинхронные фреймворки и библиотеки](#async_libs)
  * [Работа с памятью](#memory)
  * [Вопросы производительности](#performance)
  * [Профайлинг](#profiling)
  * [Логирование и трейсинг](#logging)
  * [Модули на C и ctypes](#clang)
  * [Тестирование](#testing)
  * [Утилиты для улучшения качества кода](#quality)
  * [WCGI](#wcgi)
  * [Работа с СУБД. Драйверы. Популярные ORM](#databases)
  * [Работа с данными](#datalibs)
  * [Работа с файлами](#files)
  * [Сетевое программирование](#network)
  * [GUI](#gui)
  * [Мониторинг приложений средствами ОС](#os)
  * [Нагрузочное тестирование python-приложений](#load_testing)
* [Полезное](#useful)


<a name="courses"></a>
## Курсы лекций [^](#index "к оглавлению")

> Хорошие курсы для начала

1. Специализация Программирование на Python от МФТИ и Mail.Ru Group (все курсы хорошие) https://www.coursera.org/specializations/programming-in-python
2. Академия Яндекса, Школа бэкенд-разработки 2019 на питоне https://www.youtube.com/playlist?list=PLQC2_0cDcSKBHamFYA6ncnc_fYuEQUy0s
3. Computer Science Center, Программирование на Python, 2021, Преподаватель курса: Иван Бибилов https://www.youtube.com/playlist?list=PLlb7e2G7aSpQmGnhrxlqI4iMXNv4R7khy
4. Computer Science Center, Программирование на Python, осень 2018, Преподаватель курса: Алексей Александрович Кладов https://www.youtube.com/playlist?list=PLlb7e2G7aSpQhNphPSpcO4daaRPeVstku
5. Computer Science Center, Python, 2016, Преподаватель курса: Сергей Лебедев https://www.youtube.com/playlist?list=PLlb7e2G7aSpTTNp7HBYzCBByaE1h54ruW
6. Технострим Mail.Ru Group, Прикладной Python (осень 2018) https://www.youtube.com/playlist?list=PLrCZzMib1e9qM62lMXC90SiFy7-1-kAPJ
7. Python tricks (Intermediate and Advanced Features) от Дена Бадера https://www.youtube.com/playlist?list=PLP8GkvaIxJP0VAXF3USi9U4JnpxUvQXHx
8. Intermediate Python Programming Course (freeCodeCamp.org) https://www.youtube.com/watch?v=HGOBQPFzWKo
9. Курс "Python для сетевых инженеров" Н. Самойленко https://www.youtube.com/playlist?list=PLah0HUih_ZRnJFNdZsWr2pNWgYETauGXo
10. Небольшие видео по основным темам от Михаила Корнеева https://www.youtube.com/channel/UC2-j4-hV33hboyK1FtukJ9w/videos

<a name="books_online"></a>
## Книги онлайн [^](#index "к оглавлению")
1. Книга Intermediate Python (Obi Ike-Nwosu) онлайн https://leanpub.com/intermediatepython/read
2. The Hitchhiker’s Guide to Python https://docs.python-guide.org/

<a name="parts"></a>
## По темам (+ краткий конспект) [^](#index "к оглавлению")

<a name="internals"></a>
### Внутренности питона [^](#index "к оглавлению")

> Разбор кода на токены -> построение AST -> оптимизации -> генерация байткода -> выполнение байткода в виртуальной машине. Стандартный интерпретатор - cpython (написан на языке C https://github.com/python/cpython). Альтернативные - pypy (написан на питоне, с JIT), ironpython (C#) и jython(java) - под специфические задачи, не без проблем и особым спросом не пользуются. 
> Для решения проблем и получения ответов на свои вопросы полезно 1) уметь разбирать байткод 2) знать структуру cpython и уметь читать сишный код

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
13. Интересный разбор написания интерпретатора http://aosabook.org/en/500L/a-python-interpreter-written-in-python.html
14. Книга Inside The Python Virtual Machine (Obi Ike-Nwosu) онлайн https://leanpub.com/insidethepythonvirtualmachine/read
15. Cpython Internals - разбор внутренностей cpython со схемами https://github.com/zpoint/CPython-Internals
16. Статьи автора LinearLeopard: Реализация строкового типа в CPython (https://habr.com/ru/post/480324/), Немного внутренностей словарей в CPython (https://habr.com/ru/post/432996/), Реализация целого типа в CPython (https://habr.com/ru/post/455114/)
17. Python Developer’s Guide (ресурс про разработку интерпретатора) https://devguide.python.org/
18. Stepping Through CPython (Larry Hastings) https://www.youtube.com/watch?v=XGF3Qu4dUqk
19. Bytecodes and stacks: A look at CPython’s compiler and its execution model (Petr Viktorin) (PyCon CZ 2018) https://www.youtube.com/watch?v=rOU-W_J-zFE
20. A Deep Dive into Python Stack Frames (Nikhil Marathe) (PyCotham 2018) https://www.youtube.com/watch?v=smiL_aV1SOc
21. Dominik ‘disconnect3d’ Czarnota - Python internals - how does CPython work? https://www.youtube.com/watch?v=4QJOEeldFUc
22. CPython internals and the VM https://www.youtube.com/watch?v=cUyMnGeZ_3c

<a name="datatypes"></a>
### Типы данных. Коллекции [^](#index "к оглавлению")
> Все в питоне является объектом. Чтобы узнать тип объекта `x`, нужно вызвать `type(x)`, список методов и свойств - `dir(x)`, справку по методу - `help(x.some_method)`. Основные коллекции - list, tuple, dict, set, а также несколько интересных коллекций есть в модуле `collections`
1. Лекция про коллекции и модуль `collections` от CSC https://www.youtube.com/watch?v=kmdA7zJS9gw, лекция про строки, байты https://www.youtube.com/watch?v=VY95vgOROo8
2. Basic Data Types in Python (real python) https://realpython.com/python-data-types/
3. Dictionaries in Python (real python) https://realpython.com/python-dicts/
4. Sets in Python (real python) https://realpython.com/python-sets/
5. Lists and Tuples in Python (real python) https://realpython.com/python-lists-tuples/
6. Linked Lists in Python: An Introduction (real python) https://realpython.com/linked-lists-python/
7. Strings and Character Data in Python (real python) https://realpython.com/python-strings/ 
8. Numbers in Python https://realpython.com/python-numbers/
9. Модуль collections из стандартной библиотеки https://habr.com/ru/post/478934/
10. The Python heapq Module: Using Heaps and Priority Queues (real python) https://realpython.com/python-heapq-module/
11. Python Data Structures: Sets, Frozensets, and Multisets (real python) https://www.youtube.com/watch?v=b-K1ujf8u_k
12. When to Use a List Comprehension in Python https://realpython.com/list-comprehension-python/
13. Null in Python: Understanding Python's NoneType Object https://realpython.com/null-in-python/
14. Common Python Data Structures (Guide) https://realpython.com/python-data-structures/
15. Робот в лабиринте: обрабатываем в Python очереди с приоритетом (heapq) https://proglib.io/p/robot-v-labirinte-obrabatyvaem-ocheredi-s-prioritetom-v-python-2020-07-07
16. Очередь для использования в многопоточных приложениях https://docs.python.org/3/library/queue.html
17. Raymond Hettinger - Dataclasses: The code generator to end all code generators - PyCon 2018 https://www.youtube.com/watch?v=T-TwcmT6Rcw

<a name="instructions"></a>
### Циклы, условия, операторы [^](#index "к оглавлению")
> Поведение объектов с тем или иным оператором определяется реализацией у него соответствующего магического метода.
1. Operators and Expressions in Python (real python) https://realpython.com/python-operators-expressions/
2. Operator and Function Overloading in Custom Python Classes (real python) https://realpython.com/operator-function-overloading/
3. Conditional Statements in Python (real python) https://realpython.com/python-conditional-statements/
4. Python "while" Loops (Indefinite Iteration) (real python) https://realpython.com/python-while-loop/
5. Python "for" Loops (Definite Iteration) (real python)  https://realpython.com/python-for-loop/

<a name="iterators"></a>
### Итераторы и генераторы. Сопрограммы [^](#index "к оглавлению")
1. Лекция про итераторы, генераторы и корутины от CSC https://www.youtube.com/watch?v=Xxuy1zFCMhc
2. Корутины для самых маленьких. Иван Гончарук, DAN https://www.youtube.com/watch?v=_obr60qv6rM
3. Как устроены корутины? / Дмитрий Калугин-Балашов (Exnodes Inc.) https://www.youtube.com/watch?v=vhf5lU1suL0
4. Itertools in Python 3, By Example https://realpython.com/python-itertools/
5. How to Use Generators and yield in Python https://realpython.com/introduction-to-python-generators/ 
6. Как работает yield https://habr.com/ru/post/132554/
7. Презентации Д.Бизли по генераторам (http://dabeaz.com/generators/) и сопрограммам (http://dabeaz.com/coroutines/)
8. Python 101: iterators, generators, coroutines, Mark McDonnell https://www.integralist.co.uk/posts/python-generators/
9. What is a Coroutine Anyway? (John Reese, North Bay Python 2019) https://www.youtube.com/watch?v=GSiZkP7cI80
10. Подробно о корутинах в C++ (сравниваются стековые и бесстековые корутины) https://habr.com/ru/company/piter/blog/491996/
11. Александр Кошкин "Знай и люби свой yield. Корутины и генераторы за гранью for loop" https://www.youtube.com/watch?v=-E1V24zZJrs

<a name="functions"></a>
### Функции. Замыкания. Декораторы. ФП [^](#index "к оглавлению")
> Декоратор - часто используемый шаблон проектирования в питоне, для которого есть даже специальный синтаксический сахар `@deco\nmethod` - то же самое что `method=deco(method)` как мы написали бы на других ЯП. В декораторы можно передавать аргументы.
1. Лекция по ООП и декораторам от Акадении Яндекса https://youtu.be/Db19qjrMsYI?t=2596
2. Функциональное программирование и работа с данными (+ декораторы) (урок OTUS) https://www.youtube.com/watch?v=iHT2OlrCBgs
3. Скринкаст Олега Молчанова по декораторам https://www.youtube.com/watch?v=Ss1M32pp5Ew
4. Лекции про функции https://www.youtube.com/watch?v=VrShEItN0Jc и декораторы https://www.youtube.com/watch?v=rkjg71GJPvA от CSC
5. Optional Arguments in Python With `*args` and `**kwargs` https://www.youtube.com/watch?v=WcTXxX3vYgY
6. How to Use Python Lambda Functions https://realpython.com/python-lambda/
7. Python's map(): Processing Iterables Without a Loop https://realpython.com/python-map-function/
8. Tutorial: Geir Arne Hjelle - Introduction to Decorators: Power Up Your Python Code (Pycon US) https://www.youtube.com/watch?v=T8CQwGIsrx4
9. Reuven M. Lerner - Practical decorators - PyCon 2019 https://www.youtube.com/watch?v=MjHpMCIvwsY

<a name="OOP"></a>
### ООП. Магические методы. Протокол дескрипторов. Метаклассы. Статические методы и методы класса [^](#index "к оглавлению")
> Все в питоне является объектом. Питон поддерживает множественное наследование, при этом порядок выбора метода определяется алгоритмом MRO. Соглашение об именовании методов (`_method` - приватный атрибут, `__method` - искажение имени для избежания конфликтов наследников). Магические методы `__method__` - задают поведение объекта с операторами, стандартными функциями, при доступе к атрибутам и т.д.
1. ООП. Лекция Академии Яндекса https://www.youtube.com/watch?v=Db19qjrMsYI
2. Руководство по магическим методам в Питоне (перевод статьи Rafe Kettler) https://habr.com/ru/post/186608/
3. Магические методы и дескрипторы (урок Otus) https://www.youtube.com/watch?v=6Zd35hSvGio
4. Руководство к дескрипторам (хабр) https://habr.com/ru/post/122082/
5. Дескрипторы (В. Донец) https://www.youtube.com/watch?v=akyVo4BzYZo
6. Алексей Кузьмин. Жизненный цикл Python-объекта https://www.youtube.com/watch?v=UndKVhoMNg8
7. Лекция про классы https://www.youtube.com/watch?v=2pttEjdYJuo (ч.1) и https://www.youtube.com/watch?v=czqYT7103Eo (ч.2)
8. Лекция про метапрограммирование от Технострима https://www.youtube.com/watch?v=bt6kU1kuHWA
9. Python Descriptors: An Introduction https://realpython.com/python-descriptors/
10. Supercharge Your Classes With Python super() https://realpython.com/python-super/
11. Inheritance and Composition: A Python OOP Guide https://realpython.com/courses/inheritance-composition-python/
12. Цикл статей по ООП с подробным разбором тем https://proproprogs.ru/python_oop
13. Python Magic (Magic of Python) (урок OTUS) https://www.youtube.com/watch?v=rmIDwxyngWU
14. Luciano Ramalho - Pythonic Objects: idiomatic OOP in Python - PyCon 2019 https://www.youtube.com/watch?v=mUu_4k6a5-I
15. The Magic of Python - Darshan Markandaiah (Pyohio 2019) https://www.youtube.com/watch?v=X9poNqBfX4Q
16. Mariano Anaya - Discovering Descriptors (EuroPython 2017) https://www.youtube.com/watch?v=TAuC086NNmo
17. Ariel Ortiz - The Perils of Inheritance: Why We Should Prefer Composition - PyCon 2019 https://www.youtube.com/watch?v=YXiaWtc0cgE
18. Ariel Ortiz - Design Patterns in Python for the Untrained Eye - PyCon 2019 https://www.youtube.com/watch?v=o1FZ_Bd4DSM

<a name="stdlib"></a>
### Возможности стандартной библиотеки [^](#index "к оглавлению")
> У питона богатейшая стандартная библиотека. Там есть все, что нужно и даже больше
1. Официальная документация https://docs.python.org/3/library/
2. Python 3 Module of the Week (разбор модулей стандартной библиотеки с примерами) https://pymotw.com/3/

<a name="debugging"></a>
### Дебаггинг [^](#index "к оглавлению")
> Для питона есть консольный дебаггер - pdb, а также дебаггеры в популярных IDE
1. Python Debugging With Pdb (Real python) https://realpython.com/python-debugging-pdb/
2. Advanced Debugging in PyCharm (JetBrains) https://www.youtube.com/watch?v=k6j1NkVAsuU
3. Как устроены дебаггеры (доклад Елизаветы Шашковой на pycon) https://www.youtube.com/watch?v=jK3D77b-DXk
4. Отладка Python (статья от mail.ru с обзором дебаггеров) https://habr.com/ru/company/mailru/blog/205426/
5. Time Travel Debugging for Python (с профайлингом) https://pytrace.com/
6. Goodbye Print, Hello Debugger! - Nina Zakharenko https://www.youtube.com/watch?v=5AYIe-3cD-s
7. PySnooper - Never use print for debugging again - Ram Rachum - PyCon Israel 2019 https://www.youtube.com/watch?v=XP5imOJc_TE
8. Дока по использованию отладчика gdb для python-приложений https://devguide.python.org/gdb/
9. Introduction to Debugging with Python (PyOhio, 2017) https://www.youtube.com/watch?v=BixeKmlKOJc
10. Advanced Python Debugging Techniques Using GDB (PyOhio, 2016) https://www.youtube.com/watch?v=rB9rPdMRxIA
11. Кирилл Борисов (Яндекс) - Отладка в Python: 2016 edition https://www.youtube.com/watch?v=nHhifqUm_Qg

<a name="exceptions"></a>
### Обработка исключений. Контекстные менеджеры [^](#index "к оглавлению")
1. Python Exceptions: An Introduction https://realpython.com/python-exceptions/
2. Understanding the Python Traceback https://realpython.com/python-traceback/
3. Python KeyError Exceptions and How to Handle Them https://realpython.com/python-keyerror/
4. Devpractice Работа с исключениями https://devpractice.ru/python-lesson-11-work-with-exceptions/
5. Григорий Петров: "Работа с ошибками. Как ловить исключения и что потом с ними делать." https://www.youtube.com/watch?v=hzVECcMI8ys
6. Лекция про работу с исключениями от CSC https://www.youtube.com/watch?v=a6UtrJ4Xh-Y
7. Python Context Managers and the "with" Statement (`__enter__` & `__exit__`) (real python) https://www.youtube.com/watch?v=iba-I4CrmyA
8. How to Handle Exceptions in Python: A Detailed Visual Introduction https://www.freecodecamp.org/news/exception-handling-python/
9. Всё об исключениях и работе с ними в Python (Диджитализируй!) https://www.youtube.com/watch?v=89wpfOAgrCk
10. Mario Corchero - Exceptional Exceptions - How to properly raise, handle and create them https://www.youtube.com/watch?v=V2fGAv2R5j8
11. Python 101: Context Managers,  by Mark McDonnell https://www.integralist.co.uk/posts/python-context-managers/

<a name="modules"></a>
### Пакеты и модули. Pypi. pip и easy_install. virtualenv [^](#index "к оглавлению")
1. Ликбез по пакетам и шпаргалка по модулям в Python (Хекслет) https://ru.hexlet.io/blog/posts/likbez-po-paketam-i-shpargalka-po-modulyam-v-python
2. Python Modules and Packages – An Introduction (real python) https://realpython.com/python-modules-packages/
3. How to Publish an Open-Source Python Package to PyPI (real python) https://realpython.com/pypi-publish-python-package/
4. Dependencies Handling in Python (Julien Danjou) https://julien.danjou.info/dependencies-handling-in-python-automatic-update/
5. Лекция от CSC про модули https://www.youtube.com/watch?v=ISo-L-0xsoI
6. Installing Python Packages with pip and virtualenv / venv (Real pyrhon screencast) https://www.youtube.com/watch?v=UqkT2Ml9beg
7. Python import: Advanced Techniques and Tips https://realpython.com/python-import/
8. How to Publish an Open-Source Python Package to PyPI https://realpython.com/pypi-publish-python-package/
9. Python Virtual Environments: A Primer https://realpython.com/python-virtual-environments-a-primer/
10. Как опубликовать свою Python библиотеку на PyPI https://proglib.io/p/kak-opublikovat-svoyu-python-biblioteku-na-pypi-2020-01-28
11. How import works in Python (PyCon India 2018) https://www.youtube.com/watch?v=-mL5WBMseD4
12. What happens behind execution of an `import` statement? (Shivashis) [PyCon JP 2020] https://www.youtube.com/watch?v=0far0mS2lY8
13. Python Management and Project Dependencies, Mark McDonnell https://www.integralist.co.uk/posts/python-management/

<a name="gil"></a>
### Многопоточность. GIL. Многопроцессные приложения [^](#index "к оглавлению")
1. Многопоточность и GIL. Лекция от Computer Science center https://www.youtube.com/watch?v=nR8WhdcRJwM
2. What is the Python Global Interpreter Lock (GIL)? https://realpython.com/python-gil/
3. An Intro to Threading in Python (real python) https://realpython.com/intro-to-python-threading/
4. GIL (урок Otus) https://www.youtube.com/watch?v=hCOmbMRsJ8c
5. GIL в Python: зачем он нужен и как с этим жить - Доклад Г. Петрова https://www.youtube.com/watch?v=AWX4JnAnjBE
6. Злата Обуховская, Nvidia «Structured Concurrency. Что не так с асинхронностью в питоне?» https://www.youtube.com/watch?v=NmWzt7VdTgA
7. GIL: почему это боль и как с ним жить. Иван Меньших, RaRe Technologies https://www.youtube.com/watch?v=GGUIt1o_TNc
8. Константин Данилов. Многопоточность и синхронная/асинхронная обработка в Python https://www.youtube.com/watch?v=ZTBPpLfemaQ
9. Как устроен GIL в Python https://habr.com/ru/post/84629/
10. Global Interpreter Lock https://ru.wikipedia.org/wiki/Global_Interpreter_Lock
11. Grok the GIL: How to write fast and thread-safe Python https://opensource.com/article/17/4/grok-gil
12. Асинхронный Python: различные формы конкурентности https://habr.com/ru/post/421625/
13. Слайды доклада Д.Бизли "Understanding the Python GIL" http://www.dabeaz.com/python/UnderstandingGIL.pdf
14. Модуль `concurrent.futures` https://pymotw.com/3/concurrent.futures/
15. Speed Up Your Python Program With Concurrency https://realpython.com/python-concurrency/
16. Gevent для практикующего питониста https://vovkd.github.io/gevent-tutorial/
17. Потоки и процессы (не смешивать), Станислав Рудаков (+ пример использования gdb) [Minsk Python Meetup] https://www.youtube.com/watch?v=mrXsn3yyuDM
18. Tutorial: Santiago Basulto - Python Concurrency: from beginner to pro https://www.youtube.com/watch?v=18B1pznaU1o
19. Thread (and AsyncIO) Concurrency Visualization of JetBrains Pycharm and Idea https://www.jetbrains.com/help/pycharm/thread-concurrency-visualization.html
20. Python's Infamous GIL by Larry Hastings (для чего нужен GIL) https://www.youtube.com/watch?v=KVKufdTphKs
21. Concurrency In Python Concepts, Frameworks And Best Practices - Stefan Schwarzer (PyCon DE) https://www.youtube.com/watch?v=Do7JtnPh1Mg
22. Raymond Hettinger, Keynote on Concurrency, PyBay 2017 https://www.youtube.com/watch?v=9zinZmE3Ogk
23. Jacek Kolodziej: GIL: What's the hassle and why should I care? (PyCon CZ 2017) https://www.youtube.com/watch?v=ZvWmAIODi-s
24. Writing robust, readable, and maintainable concurrent programs in Python - PyCon APAC 2018 https://www.youtube.com/watch?v=DJnUctSQSGw
25. Concurrency vs Parallelism - PyCon APAC 2018 https://www.youtube.com/watch?v=HNjAgkybAdQ
26. Things I Wish They Told Me About The Multiprocessing Module in Python 3 (Pamela McANulty) (PyCon Cleveland 2019) https://www.youtube.com/watch?v=5dMOYf0b_20
27. Grok the GIL Write Fast And Thread Safe Python (Jesse Jiryu Davis) PyCon 2017 https://www.youtube.com/watch?v=7SSYhuk5hmc
28. Убирая ГБИ (GIL) из Питона: Гилектомия (Д. Бизли) pycon 2016, русский перевод https://www.youtube.com/watch?v=48l_HOtAqAI
29. Действительно ли Python GIL уже мертв? (перевод статьи Anthony Shaw) https://habr.com/ru/company/otus/blog/458694/
30. Многопроцессность, многопоточность, асинхронность в Python и не только. Что это и как работает? (Диджитализируй!) https://www.youtube.com/watch?v=JIp14T9bvvc
31. «Обмен данными между процессами python» Yehor Nazarkin LvivPy#5 https://www.youtube.com/watch?v=IaW-1AoGAKc
32. Chin Hwee Ong - Speed Up Your Data Processing | PyData Global 2020 https://www.youtube.com/watch?v=E9sv2B3Bb20

<a name="async"></a>
### Асинхронное программирование. Event loop. Теория [^](#index "к оглавлению")
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
11. Аsync и await в production / Сергей Борисов (ДомКлик) https://www.youtube.com/watch?v=pN9A5kD_rK8
12. Что внутри asyncio. Александр Меренков, Antida software https://www.youtube.com/watch?v=V7iecSKgWLM
13. Asyncio: understanding async and await in Python https://www.youtube.com/watch?v=a_wWnxH2o0Y
14. Новый Python: Асинхронное всё, Иван Уваров https://cmc.basealt.ru/new-python.html
15. Реализация epoll в Linux (цикл статей) https://habr.com/ru/company/ruvds/blog/523946/
16. Юрий Селиванов, EdgeDB, Asyncio «Asyncio сегодня и завтра» https://www.youtube.com/watch?v=BhqeJGTji2I
17. Асинхронное программирование в Python (Кузьмин, ДомКлик) https://www.youtube.com/watch?v=OEFsdk1tqAU
18. Асинхронщина в Python (Полищук, MoscowPython) https://www.youtube.com/watch?v=lIkA0TDX8tE
19. Understanding Concurrency in Python! - Annie Cook https://www.youtube.com/watch?v=9g5IZDkwAC0
20. Miguel Grinberg Asynchronous Python for the Complete Beginner PyCon 2017 https://www.youtube.com/watch?v=iG6fr81xHKA
21. Combining ayncio and threads in the same application (Marc-Andre Lemburg) [PyCon JP 2020] https://www.youtube.com/watch?v=ci9z1NM6F0Y&t=230s
22. An introduction to concurrent programming with asyncio, Bruce Merry (PyCon SA 2018) https://www.youtube.com/watch?v=x1RXHcE3oVI
23. Sanic: Async Python (uvloop) with a familiar flask like feel, (PyCon SA 2018) https://www.youtube.com/watch?v=QtXUwEQS2pg
24. Thinking Outside the GIL with AsyncIO and Multiprocessing, John Reese (PyCon 2018) https://www.youtube.com/watch?v=0kXaLh8Fz3k
25. Artisanal Async Adventures(Jonas Obrist) (пишем свой asyncio) (PyCon JP 2018) https://www.youtube.com/watch?v=6doZo6eySCg
26. Deep Dive into Coroutine, Daehee Kim (PyCon Korea) (разбор байткода корутин. слайды на английском, понять можно) https://www.youtube.com/watch?v=NmSeLspQoAA
27. Adopting Python Asyncio in Large Scale Project (Instagram) – Jimmy Lai – PyCon Taiwan 2018 https://www.youtube.com/watch?v=ACgMTqX5Ee4
28. Running Python code in parallel and asynchronously (Michal Wysokinski) (EuroPython 2017) https://www.youtube.com/watch?v=ZKzCx4D5c3g
29. `asyncio.get_event_loop()` → what is that? (Kamal Marhubi) (Montreal-Python 2015) https://www.youtube.com/watch?v=2DmUvBtSdnI
30. Guide to Concurrency in Python with Asyncio, Mark McDonnell  https://www.integralist.co.uk/posts/python-asyncio/
31. Async/await: асинхронные возможности в Python 3+ https://xakep.ru/2017/01/11/python-3-asyncio/
32. Лекция: Прикладной Python. Асинхронное программирование, Технострим https://www.youtube.com/watch?v=X9RRJG109a4 (+ семинар https://www.youtube.com/watch?v=h0Dm2TNXoP0)
33. Python Junior подкаст. Про асинхронность в питоне https://www.youtube.com/watch?v=Q2r76grtNeg
34. Что внутри asyncio, Александр Меренков https://habr.com/ru/post/453348/

<a name="async_libs"></a>
### Асинхронные фреймворки и библиотеки [^](#index "к оглавлению")
> Устаревшие (Twisted и Tornado), стандртные (asyncio, aiohttp), сыроватые новинки (sanic, vibora)
1. Дмитрий Ходаков, Авито «Tornado vs Aiohttp» https://www.youtube.com/watch?v=BbyVHtsIM1M (и статья https://habr.com/ru/company/avito/blog/435532/)
2. Различные асинхронные библиотеки от создателей `asyncio` https://github.com/aio-libs
3. Андрей Светлов, Python Core Developer «Aiohttp от автора» https://www.youtube.com/watch?v=5NrnBu1vcKo
4. Yury Selivanov - Asyncio in Python 3.7 and 3.8 https://www.youtube.com/watch?v=ReXxO_azV-w
5. Самые быстрые Python веб-фреймворки в 2019 (перевод статьи Maksim Larkin) https://habr.com/ru/post/440282/
6. Андрей Светлов: "Подводные камни asyncio" https://www.youtube.com/watch?v=GLN_xo4Awcc
7. Async IO in Python: A Complete Walkthrough https://realpython.com/async-io-python/
8. Asyncio: understanding async and await in Python https://www.youtube.com/watch?v=a_wWnxH2o0Y
9. uvloop — продвинутая реализация цикла событий для asyncio в Python https://habr.com/ru/post/282972/
10. Understanding Tornado fundamentals (объяснение про `@gen.coroutine`) https://bhch.github.io/posts/2017/06/understanding-tornado-fundamentals/
11. Я не люблю asyncio – Павел Камаев https://www.youtube.com/watch?v=Fj2t959Q7DA
12. Lynn Root - Advanced asyncio: Solving Real-world Production Problems - PyCon 2019 https://www.youtube.com/watch?v=bckD_GK80oY
13. Asyncio in the Wild, Ákos Hochrein (теория + обзор библиотек для asyncio) https://www.youtube.com/watch?v=EX4YsevmZBg
14. An introduction to concurrent programming with asyncio (Bruce Merry) (PyCon SA 2018) https://www.youtube.com/watch?v=x1RXHcE3oVI
15. Tornado in Depth [EuroPython 2012] (исторический доклад) https://www.youtube.com/watch?v=4Ztq-Yz1ero
16. import asyncio: Learn Python's AsyncIO (цикл подробных лекций про asyncio) https://www.youtube.com/watch?v=Xbl7XjFYsN4&list=PLhNSoGM2ik6SIkVGXWBwerucXjgP1rHmB
17. Екатерина Сударева - Асинхронность в Python. Начало https://www.youtube.com/watch?v=OmDKVuROsUM
18. Trio – асинхронное программирование для людей https://habr.com/ru/company/barsgroup/blog/490872/
19. Asyncio Coroutine Patterns (Yeray Diaz): Beyond await https://medium.com/python-pandemonium/asyncio-coroutine-patterns-beyond-await-a6121486656f и Errors and cancellation https://medium.com/@yeraydiazdiaz/asyncio-coroutine-patterns-errors-and-cancellation-3bb422e961ff 
20. Lynn Root - asyncio in Practice: We Did It Wrong https://www.youtube.com/watch?v=1lJDZx6f6tY (видео доклада)  и https://www.roguelynn.com/words/asyncio-we-did-it-wrong/ (цикл статей)
21. How to ensure asyncio task exceptions always get logged (Quantlane tech blog) https://quantlane.com/blog/ensure-asyncio-task-exceptions-get-logged/

<a name="memory"></a>
### Работа с памятью [^](#index "к оглавлению")
> Питон - очень неэкономный по памяти язык. Иногда возникают задачи, которые требуют знаний про то как питон работает с памятью (счетчик ссылок, арены и GC для циклических ссылок) и как можно эту память сэкономить.
1. «Память и Python. Что надо знать для счастья?» Алексей Кузьмин, ЦНС https://www.youtube.com/watch?v=D0vbuIDOV4c
2. Python потребляет много памяти, или как уменьшить размер объектов. (доклад З.Шибзухова) https://www.youtube.com/watch?v=qUnzGUz_YxE
3. Что внутри у питона: как устроена память (доклад З. Обуховской) https://www.youtube.com/watch?v=lSgoYx06L_s
4. В. Синицын - Python: управление памятью https://www.youtube.com/watch?v=ZxvwZ4fX_qE
5. Nina Zakharenko - Memory Management in Python - The Basics https://www.youtube.com/watch?v=URNdRl97q_0
6. Всё, что нужно знать о сборщике мусора в Python (Artem Golubin) https://habr.com/ru/post/417215/
7. Модуль GC стандартной библиотеки - официальная документация https://docs.python.org/3/library/gc.html
8. Python memory managment 101 .Deeping garbage collector (J.M. Ortega, PyCon HK) https://www.youtube.com/watch?v=MHTJQao9Ex0
9. Основы управления памятью в Python  https://webdevblog.ru/osnovy-upravleniya-pamyatju-v-python/
10. Memory Management in Python https://realpython.com/python-memory-management/ (перевод https://habr.com/ru/company/ruvds/blog/441568/)
11. Управление памятью в Python https://habr.com/ru/company/mailru/blog/336156/
12. Пару слов о профилировании памяти в Python https://otus.ru/nest/post/818/
13. Finding and Fixing Memory Leaks in Python (Peter Karb, Buzzfeed) https://tech.buzzfeed.com/finding-and-fixing-memory-leaks-in-python-413ce4266e7d
14. Pylint: о попытке снизить потребление памяти https://habr.com/ru/company/ruvds/blog/524940/
15. Эффективно работаем со сложными структурами данных в Python 3.7+ (Диджитализируй!) https://www.youtube.com/watch?v=tsEG0WM3m_M
16. Slots, slots, slots, everybody: an exploration of `__slots__` (Douglas Anderson) (PyCon Canada 2018) https://www.youtube.com/watch?v=AR3hD43HLNE
17. Python, Linkers, and Virtual Memory (PyCon US 2012) https://www.youtube.com/watch?v=twQKAoq2OPE
18. Python Tutorials - Memory size Memory management of Python data structures https://www.youtube.com/watch?v=E07JCf87_C8
19. Как работает память в Python, DomClick https://habr.com/ru/company/domclick/blog/530804/
20. Ультимативный гайд по поиску утечек памяти в Python, DomClick https://habr.com/ru/company/domclick/blog/532030/
21. How I Tried To Reduce Pylint Memory Usage https://rtpg.co/2020/10/12/pylint-usage.html
22. Python Memory Deep Dive for Speed and Efficiency, Michael Kennedy https://www.youtube.com/watch?v=d9mSIEIcTpo
23. Fabio Falzoi - An insight into Python Garbage Collection https://www.youtube.com/watch?v=pqCQ5AwCJqE
24. Помнить всё. Как работает память в Python (ProgLib) https://proglib.io/p/pomnit-vse-kak-rabotaet-pamyat-v-python-2021-03-14

<a name="performance"></a>
### Вопросы производительности [^](#index "к оглавлению")
> Несмотря на то, что питон - не самый быстрый язык, интерпретатор постоянно оптимизируют
1. Python — это медленно. Почему? https://habr.com/ru/company/ruvds/blog/418823/
2. Что я узнал про оптимизацию в Python (перевод статьи Gregory Szorc's) https://habr.com/ru/company/otus/blog/457942/
3. Which is the fastest version of Python? (статья Anthony Shaw, сравнение 2.7-3.7+pypy) https://hackernoon.com/which-is-the-fastest-version-of-python-2ae7c61a6b2b
4. Оптимизации, сделавшие Python 3.6 быстрее Python 3.5 https://www.youtube.com/watch?v=zMECweCmuA4
5. Anthony Shaw - Why is Python slow? (pycon) https://www.youtube.com/watch?v=I4nkgJdVZFA
6. Python, производительность, перспективы // Кирилл Борисов (Pytup) https://youtu.be/brA7HLZEN4w?t=8669
7. Что делать, если ваш код на Python тормозит / Григорий Бакунов (Яндекс) https://www.youtube.com/watch?v=77B2-Pk1fls

<a name="profiling"></a>
### Профайлинг [^](#index "к оглавлению")
> Как и для других ЯП, для питона существует ряд статистических (низкий оверхед и более низкая точность) и инструментальных (более высокая точность и высокий оверхед) профилировщиков
1. Flamegraph семплирующий профайлинг https://www.youtube.com/watch?v=kRA0RZoycMQ
2. PyConBY 2020: Christian Heimes - Introduction to low level profiling and tracing https://www.youtube.com/watch?v=PXEP97uU0NQ
3. Summary Of Python Profiling Tools http://pramodkumbhar.com/2019/05/summary-of-python-profiling-tools-part-i/ (на этом сайте есть еще хорошие статьи о производительности)
4. Профилирование и отладка Python (цикл статей от mail.ru): https://habr.com/ru/company/mailru/blog/201594/ (теория), https://habr.com/ru/company/mailru/blog/201778/ (ручное и статистическое), https://habr.com/ru/company/mailru/blog/202832/ (событийное)
5. Крутой sampling-профайлер (строит флеймграфы также) https://github.com/benfred/py-spy (must-have, так как pyflame больше по поддерживается)
6. Алексей Кузьмин, ДомКлик «Поиск и оптимизация узких мест в Python» (+ про память) https://www.youtube.com/watch?v=tDZHhIiACDA
7. Flamegraph that! Self-service profiling tool for Node and Python services (Ruth Grace Wong, Pinterest) https://www.youtube.com/watch?v=w97I5q0hbkw
8. Иван Ремизов "Сверхоптимизация кода на Python" (PiterPy) доклад старый, но полезный https://www.youtube.com/watch?v=4CsOOfdoU2A
9. PyTrace — Time Travel Debugger для Python https://habr.com/ru/post/504908/
10. Python Profiling and Performance Tuning in Production (Joe Gordon, Pinterest) https://www.youtube.com/watch?v=B9Kv3Fije1I, https://www.youtube.com/watch?v=bectZn_yNwg
11. Production-time Profiling for Python (Julien Danjou) https://www.youtube.com/watch?v=kLO81hMRwgI
12. Beyond cProfile: performance optimization with sampling profilers and logging https://www.youtube.com/watch?v=fOzVTPOWfQs
13. `/usr/bin/time -v python3 my_script.py` (`-l` для mac os)
14. Удобное профилирование простых скриптов в `ipython` https://jakevdp.github.io/PythonDataScienceHandbook/01.07-timing-and-profiling.html
15. Profiling Python by Example, Eyal Trabelsi (PyCon Sweden) Хороший обзор основных типов https://www.youtube.com/watch?v=9wfFXRCkkLE
16. Python Profiling and Performance Tuning - PyCon APAC 2016 (Joe Gordon ) https://www.youtube.com/watch?v=noxCqWJieB4
17. Python Profilers We Built for Efficiency – PyCon Taiwan 2019 https://www.youtube.com/watch?v=liOWqXkAy8s
18. Emin Martinian - Statistical Profiling (and other fun with the sys module) - PyCon 2019 https://www.youtube.com/watch?v=d5SGUscT2GA
19. Flame graph новый взгляд на привычное профилирование, Кирилл Борисов, Яндекс https://www.youtube.com/watch?v=pa_kAkXuOyA

<a name="logging"></a>
### Логирование и трейсинг [^](#index "к оглавлению")
1. Трейсинг в микросервисной архитектуре на Python https://www.youtube.com/watch?v=DpndyJ-CK5s
2. Читаем исходники open source Python библиотек. Библиотека Loguru (Диджитализируй!) https://www.youtube.com/watch?v=g6zzZxxifAw
3. Про Jaeger: как мы внедряли распределенную трассировку запросов, Амангельды Кыдыл https://www.youtube.com/watch?v=O5I301lYjzM
4. Mario Corchero - Effortless Logging: A deep dive into the logging module - PyCon 2018 https://www.youtube.com/watch?v=Pbz1fo7KlGg
5. OpenTracing with Jaeger - Utah Go User Group https://www.youtube.com/watch?v=GccUVCI5TkM
6. OpenTracing не только для распределенной трассировки. Константин Черкасов, Lazada https://www.youtube.com/watch?v=nHgfJ943z2I
7. OpenTelemetry // Андрей Гейн (Pytup) https://www.youtube.com/watch?v=brA7HLZEN4w&t=1864s

<a name="clang"></a>
### Модули на C (C++, Rust, Go) и ctypes [^](#index "к оглавлению")
> Когда нужно писать модуль на C: тяжелые вычисления, чтобы отпустить gil, чтобы использовать какую-либо сишную библиотеку, при работе с бинарными данными, для низкоуровневых задач, когда требуется особая работа с памятью
1. Building a Python C Extension Module (real python) https://realpython.com/build-python-c-extension-module/
2. Производительность в Python. Легкий путь (o ctypes) https://habr.com/ru/post/157537/ (дока https://docs.python.org/3/library/ctypes.html)
3. Python — Программирование расширений на C https://coderlessons.com/tutorials/python-technologies/vyuchit-piton/python-programmirovanie-rasshirenii-na-c
4. C/C++ из Python (ctypes) (хабр) https://habr.com/ru/post/466499/
5. Как писать модули для питона на C и  go (первый доклад pytup'a) https://youtu.be/tpKs4UVe3Bk?t=487
6. Андрей Светлов - Оптимизация производительности при помощи Cython https://www.youtube.com/watch?v=5-WoT4X17sk
7. Anton Zhdan-Pushkin: Under the hood of calling C/C++ from Python https://azhpushkin.me/posts/python-c-under-the-hood
8. Расширение Python на C: заставляем Python ползти быстрее // Бесплатный урок Otus https://www.youtube.com/watch?v=yUJwYluM9ao
9. Cython as a Game Changer for Efficiency (Alex Orlov) PyCon 2017 https://www.youtube.com/watch?v=_1MSX7V28Po
10. Why should you learn writing C extension? (Gavin Chan) (Hong Kong) - PyCon HK 2020 Spring https://www.youtube.com/watch?v=FOwV8apw_nQ
11. Call C code quickly and compatibly with CFFI (Zachary Voase) (PyCon Canada 2018) https://www.youtube.com/watch?v=EdUa5Sbf-4U
12. Bringing C performance to Python code, about Cython (Jan Škoda) (PyCOn CZ 2017) https://www.youtube.com/watch?v=G2yY3unaF0I
13. Pumping up Python modules using Rust - PyCon APAC 2018 https://www.youtube.com/watch?v=rqmGnggorLI
14. Любовь. Python. C++ // Александр Букин (Pytup) https://www.youtube.com/watch?v=brA7HLZEN4w&t=0s

<a name="testing"></a>
### Тестирование [^](#index "к оглавлению")
> Популярные библиотеки - pytests и unittest. Дата-провайдеры и фикстуры. Доктесты
1. Введение в автотесты. Вебинар от OTUS https://www.youtube.com/watch?v=EBMXOsCL9AA
2. Тестирование. Лекция из Академии Яндекса https://www.youtube.com/watch?v=2-EBSIRs0H4&list=PLQC2_0cDcSKBHamFYA6ncnc_fYuEQUy0s&index=4
3. Лекция про тестирование от CSC https://www.youtube.com/watch?v=VomXaukdWxo
4. TDD c pytest и без него. Урок OTUS https://www.youtube.com/watch?v=lxVv8cdSTsw
5. Эффективное тестирование с pytest (урок OTUS) https://www.youtube.com/watch?v=saf1_VmMz5U
6. Автоматизация тестирования API (pytest) https://www.youtube.com/watch?v=niDC5OlM8eI
7. Сергей Борисов, ДомКлик, мастер-класс "Тестирование асинхронных приложений" https://www.youtube.com/watch?v=BXn30wqy-og
8. Workshop: Modern Python Developer's Toolkit, Sebastian Witowski (в т.ч. про pytest) https://youtu.be/om4BSW-lpd8?t=3559
9. Pytest: введение в автотесты (урок OTUS) https://www.youtube.com/watch?v=gEkF0He5L04
10. Raphael Pierzina - Advanced pytest (EuroPython 2019) https://www.youtube.com/watch?v=gJtE-anbcww
11. Productive pytest with PyCharm (JetBrainsTV) https://www.youtube.com/watch?v=ixqeebhUa-w
12. How to Write Pytest Plugins - Darlene Wong (PyBay 2019) https://www.youtube.com/watch?v=QwDhzFkE9J4
13. Automated testing with pytest and fixtures (PyGotham 2017) https://www.youtube.com/watch?v=8mp_1Jt-xHQ
14. Mocking in Python, Mark McDonnell https://www.integralist.co.uk/posts/mocking-in-python/

<a name="quality"></a>
### Утилиты для улучшения качества кода [^](#index "к оглавлению")
1. Python Code Quality: Tools & Best Practices https://realpython.com/python-code-quality/
2. Как прокачать линтер. Максим Мазаев https://www.youtube.com/watch?v=HZPRoz8V6jk (этот же доклад https://www.youtube.com/watch?v=ZKoBZkdYLiM и статья https://habr.com/ru/company/oleg-bunin/blog/433474/)
3. Презентация "HOW TO WRITE PYLINT PLUGINS" Александра Тодорова https://piterpy.com/system/attachments/files/000/001/519/original/how_to_write_pylint_plugins_PiterPy_2018.pdf  
4. Аннотации типов в Python 3 (урок OTUS) https://youtu.be/I09iX8aoCsw?t=313
5. «Модифицируй это!» или «Больше магии Python с помощью изменения AST» (А. Маршалов) https://www.youtube.com/watch?v=Zv6yT-ytIvg
6. Инструменты для анализа кода Python https://proglib.io/p/python-code-analysis (ч.1), https://proglib.io/p/python-code-analysis-tools (ч.2)
7. Г. Петров PyRe: еще один type checker https://www.youtube.com/watch?v=-Lz81ex3jP8
8. Разработка плагинов к mypy / Владимир Пузаков https://www.youtube.com/watch?v=l7hDWA5uC0A
9. Python Type Checking (Guide) https://realpython.com/python-type-checking/
10. Bernat Gabor - Type hinting (and mypy) - PyCon 2019 https://www.youtube.com/watch?v=hTrjTAPnA_k
11. Максим Мазаев, ЦИАН "Проверка типов в большом проекте" https://www.youtube.com/watch?v=iEuTGu1ks7I
12. Łukasz Langa - Life Is Better Painted Black, or: How to Stop Worrying and Embrace Auto-Formatting https://www.youtube.com/watch?v=esZLCuWs_2Y
13. Dustin Ingram - Static Typing in Python (pycon) https://www.youtube.com/watch?v=ST33zDM9vOE
14. Как работать с типизацией в Python (tproger) https://tproger.ru/articles/python-typing/
15. Alexander Todorov: "How to write pylint plugins" / #PiterPy https://www.youtube.com/watch?v=3CkSKUNMLJc
16. Добровольная типизация в Python 3 (и не только), Максим Кольцов / PiterPy Meetup #12 https://www.youtube.com/watch?v=EU9DoJD1olo
17. Refactoring Code With the Standard Library (AST/CST), John Reese, PyCon AU 2018 https://www.youtube.com/watch?v=9USGh4Uy-xQ
18. A flake8 plugin from scratch (intermediate) anthony explains https://www.youtube.com/watch?v=ot5Z4KQPBL8

<a name="wcgi"></a>
### WCGI [^](#index "к оглавлению")
1. Введение в WSGI-серверы: Часть первая https://habr.com/ru/post/426957/
2. Анализ производительности WSGI-серверов: Часть вторая https://habr.com/ru/post/427217/
3. WSGI Servers (Full Stack Python) https://www.fullstackpython.com/wsgi-servers.html

<a name="databases"></a>
### Работа с СУБД. Драйверы. Популярные ORM [^](#index "к оглавлению")
> Самые популярные ORM для питона - SQLAlchemy и Django ORM, pewee. 
1. Introduction to Python SQL Libraries (real python) https://realpython.com/python-sql-libraries/
2. "Let's Build an ORM" - Greg Back (Pyohio 2019) https://www.youtube.com/watch?v=6rw0p9AOYb8
3. Object-relational Mappers (ORMs) (обзор, fullstackpython) https://www.fullstackpython.com/object-relational-mappers-orms.html
4. Python: Работа с базой данных (хабр) https://habr.com/ru/post/321510/ (db-api), https://habr.com/ru/post/322086/ (orm)
5. Асинхронные драйверы для работы с различными БД от создателей `asyncio` https://github.com/aio-libs
6. Список асинхронных драйверов для БД https://github.com/timofurrer/awesome-asyncio#database-drivers
7. SQLAlchemy ORM: удобная работа с базами данных на Python (ITVDN) https://www.youtube.com/watch?v=PAKJpfxeXjc
8. Сравнение технологий aiopg & asyncpg, Алексей Фирсов / PyDaCon meetup https://www.youtube.com/watch?v=bY6ZU0-26TA
9. "SQLAlchemy: Python vs Raw SQL" Денис Катаев https://www.youtube.com/watch?v=jUGK-CtM-Mk
10. "Пишем приложения на SQLAlchemy" Денис Катаев https://www.youtube.com/watch?v=vXBlOvmzs_0

<a name="datalibs"></a>
### Работа с данными [^](#index "к оглавлению")
1. Python NumPy Tutorial for Beginners (Freecodecamp.org) https://www.youtube.com/watch?v=QUT1VHiLmmI
2. Pandas: How to Read and Write Files https://realpython.com/pandas-read-write-files/
3. The Pandas DataFrame: Make Working With Data Delightful https://realpython.com/pandas-dataframe/
4. Using Pandas and Python to Explore Your Dataset https://realpython.com/pandas-python-explore-dataset/
5. NumPy, SciPy, and Pandas: Correlation With Python https://realpython.com/numpy-scipy-pandas-correlation-python/
6. Python Statistics Fundamentals: How to Describe Your Data https://realpython.com/python-statistics/
7. Data Analysis with Python - Full Course for Beginners (Numpy, Pandas, Matplotlib, Seaborn) https://www.youtube.com/watch?v=r-uOLxNrNk8
8. 6 способов значительно ускорить pandas с помощью пары строк кода https://habr.com/ru/post/503726/
9. A Beginner’s Guide to Optimizing Pandas Code for Speed https://engineering.upside.com/a-beginners-guide-to-optimizing-pandas-code-for-speed-c09ef2c6a4d6
10. Kevin Markham - Data Science Best Practices with pandas - PyCon 2019 https://www.youtube.com/watch?v=ZjrUmNq41Eo

<a name="files"></a>
### Работа с файлами [^](#index "к оглавлению")
1. Working With Files in Python https://realpython.com/working-with-files-in-python/

<a name="network"></a>
### Сетевое программирование [^](#index "к оглавлению")
1. Python 3 — Сетевое программирование https://coderlessons.com/tutorials/python-technologies/izuchite-python-3/python-3-setevoe-programmirovanie
2. Network Programming with Python Course (freeCodeCamp.org) https://www.youtube.com/watch?v=FGdiSJakIS4
3. Сокеты в Python для начинающих https://habr.com/ru/post/149077/

<a name="gui"></a>
### GUI [^](#index "к оглавлению")
> На питоне можно разрабатывать программы с графическим интерфейсом - для этого есть несколько популярных библиотек
1. Серия статей Python GUI Programming (RealPython). Обзор библиотек PySimpleGUI, Tkinter, PyQt, wxPython https://realpython.com/learning-paths/python-gui-programming/ 
2. Python GUI: создаём простое приложение с PyQt и Qt Designer (tproger) https://tproger.ru/translations/python-gui-pyqt/
3. 13 GUI-библиотек Python https://techrocks.ru/2018/04/26/13-python-gui-frameworks/
4. Серия статей о PyQT5 с примерами http://zetcode.com/gui/pyqt5/
5. Tkinter Course - Create Graphic User Interfaces in Python Tutorial (freecodecamp) https://www.youtube.com/watch?v=YXPyB4XeYLA
6. Создание desktop-приложений на Python (доклад на MoscowPython) https://www.youtube.com/watch?v=nz6G_ta3of0
7. PyQt Layouts: Create Professional-Looking GUI Applications (realpython) https://realpython.com/python-pyqt-layout/

<a name="os"></a>
### Мониторинг приложений средствами ОС [^](#index "к оглавлению")
1. Более чем 80 средств мониторинга системы Linux https://habr.com/ru/company/ua-hosting/blog/281519/
2. Strace в Linux: история, устройство и использование https://habr.com/ru/company/badoo/blog/493856/
3. Краткий гайд по использованию GDB https://habr.com/ru/post/491534/
4. Sysdig — инструмент для диагностики Linux-систем https://habr.com/ru/company/selectel/blog/222839/
5. Perf и flamegraphs https://habr.com/ru/company/selectel/blog/437808/
6. perf-tools by Brendan Gregg https://github.com/brendangregg/perf-tools, http://www.brendangregg.com/perf.html
7. htop и многое другое на пальцах https://habr.com/ru/post/316806/
8. Как посмотреть потоки процесса в Linux https://losst.ru/kak-posmotret-potoki-protsessa-v-linux
9. Удивительно полезный инструмент: lsof https://habr.com/ru/company/ruvds/blog/337934/
10. Brebdan Gregg: perf Examples (профилирующая тулза) http://www.brendangregg.com/perf.html
11. Sysdig — инструмент для диагностики Linux-систем https://habr.com/ru/company/selectel/blog/222839/
12. Отлаживаем развертывание ПО со strace https://habr.com/ru/company/southbridge/blog/478626/
13. Как узнать оперативную память Linux https://losst.ru/ispolzovanie-operativnoj-pamyati-linux
14. Чудеса трассировки: Решение проблем с приложениями при помощи утилиты strace https://xakep.ru/2011/01/13/54477/
15. Файловая система proc в Linux https://losst.ru/fajlovaya-sistema-proc-v-linux
16. Перевод комиксов Джулии Эванс про системные утилиты https://firstvds.ru/blog/julia_evans
17. Изучаем трассировку с помощью eBPF: Руководство и примеры https://habr.com/ru/post/435142/
18. Трассировка и профайлинг в Linux с помощью bcc/eBPF https://eax.me/bcc-ebpf/
19. BpfTrace - наконец, полноценная замена Dtrace в Linux / Пётр Зайцев (Percona) https://www.youtube.com/watch?v=6ExXwQecMrs
20. Introduction to profiling python performance with USDT https://www.youtube.com/watch?v=Zv3--YaaIe0
21. Установка и простые примеры использования SystemTap https://eax.me/systemtap/
22. Instrumenting CPython with DTrace and SystemTap https://docs.python.org/3/howto/instrumentation.html
23. Dive into BPF performance tools using python Андрей Солдатенко https://www.youtube.com/watch?v=8S8zwJBOD0w
24. Tracing, Profiling & Debugging in Production (eBPF) - Trent Lloyd (PyCon AU 2019) https://www.youtube.com/watch?v=jXzEzmz-oag
25. Команда top в Linux https://losst.ru/komanda-top-v-linux
26. Полнофункциональная динамическая трассировка в Linux с использованием eBPF и bpftrace https://www.itsumma.ru/knowledges/blog/tracing
27. Velocity 2017: Performance Analysis Superpowers with Linux eBPF https://www.youtube.com/watch?v=bj3qdEDbCD4
28. Jesús Cea Avión - Python and DTrace https://www.youtube.com/watch?v=HwqvHUGyGTE
29. Root Cause Analysis with eBPF & Python - Pavel Rogovoy - PyCon Israel 2019 https://www.youtube.com/watch?v=hEBZ_htE0IQ
30. Using Python to make sense of system traces (Jérémie Galarneau) (PyCon Canada 2017) (демки https://github.com/jgalar/PyConCanada2017) https://www.youtube.com/watch?v=gKmtmPqr6H8
31. Вглубь ядра: знакомство с LTTng https://habr.com/ru/company/selectel/blog/300966/
32. BPF code with Python: A Gentle Introduction to BPF part 2 (Michael Mullin) https://www.youtube.com/watch?v=ayxHANt1YaI

<a name="load_testing"></a>
### Нагрузочное тестирование python-приложений [^](#index "к оглавлению")
1. Python инструменты для нагрузочного тестирования https://www.youtube.com/watch?v=-kWm5V9pyCY
2. Открытые бенчмарки для нагрузочного тестирования серверов и веб-приложений https://habr.com/ru/company/1cloud/blog/474474/
3. Load Testing with Vegeta https://www.scaleway.com/en/docs/vegeta-load-testing/
4. Locust: нагрузочное тестирование веб-сервисов / Алексей Романов https://www.youtube.com/watch?v=65Xa__DMhAw

<a name="useful"></a>
## Полезное [^](#index "к оглавлению")

### Must-read книги [^](#index "к оглавлению")
1. Лучано Рамальо: Python. К вершинам мастерства (Fluent Python) https://www.ozon.ru/context/detail/id/135305378/
2. Данжу Джульен: Путь Python. Черный пояс по разработке, масштабированию, тестированию и развертыванию https://www.ozon.ru/context/detail/id/158868396/
3. Бейдер Дэн: Чистый Python. Тонкости программирования для профи https://www.ozon.ru/context/detail/id/146393762/
4. Mohamed Mustapha Tahrioui: asyncio Recipes. A Problem-Solution Approach https://www.apress.com/gp/book/9781484244005
5. Caleb Hattingh: Using Asyncio in Python https://www.oreilly.com/library/view/using-asyncio-in/9781492075325/

### Telegram-каналы [^](#index "к оглавлению")
1. pythonist.ru (статьи и задачки для собеседований) https://t.me/pythonist_ru
2. Книги https://t.me/python_textbooks
3. Задачки, в основном несложные https://t.me/pythonquestions
4. Англоязычный канал со статьями https://t.me/pythonl
5. Тесты https://t.me/pythontesti
6. Proglib (статьи, не только питон) https://t.me/proglibrary
7. Лучшие статьи https://t.me/zen_of_python

### Тесты и задачки для проверки знаний [^](#index "к оглавлению")
1. Real Python Quizzes https://realpython.com/quizzes/
2. PYnative Python Quizes https://pynative.com/python-quizzes/

### Рассылки
1. Еженедельная рассылка со свежими новостями и полезностями https://pycoders.com/

###  Митапы и конференции [^](#index "к оглавлению")
1. Moscow python meetup (+ Moscow python conf) https://www.youtube.com/user/moscowdjangoru
2. Minsk python meetup https://www.youtube.com/user/pythonMinsk 
3. Python Meetup Chelyabinsk https://www.youtube.com/channel/UCpMh_XSn7yGPabFBYzY5hKg
4. Python Новосибирск https://www.youtube.com/c/PyNSK/
5. PyCon Russia https://www.youtube.com/user/videoitpeople/videos
6. Moscow Python Conf++ https://www.youtube.com/channel/UCqC1iSQnRIDz_rOy8LHe69g
7. EuroPython Conference https://www.youtube.com/c/EuroPythonConference
