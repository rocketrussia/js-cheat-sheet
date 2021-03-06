# Синтаксис регулярных выражений
Регулярные выражения - это шаблоны поиска, используемые для сопоставления комбинаций символов в строках. Шаблон поиска можно использовать для операций поиска текста и замены текста.

## Модификаторы
* ```e``` — устаревший модификатор regex, который позволяет вам использовать PHP-код в вашем регулярном выражении
* ```i``` — Выполнить сопоставление без учета регистра
* ```g``` — Выполнить глобальное сопоставление
* ```m``` — Выполнить сопоставление нескольких строк
* ```s``` — Обрабатывать строки как одну строку
* ```x``` — Разрешить комментарии и пробелы в шаблоне
* ```U``` — Обрабатывать шаблон как последовательность Unicode

## Скобки
* ```[abc]``` — Найти любой из символов в скобках
* ```[^abc]``` — Найти любой символ, который не находится в скобках
* ```[0-9]``` — Используется для поиска любой цифры от 0 до 9
* ```[A-z]``` — Найти любой символ от заглавной буквы A до строчной z
* ```(a|b|c)``` — Найти любую из альтернатив, разделенных |

## Метасимволы
* ```.``` - Найти один символ, кроме символа новой строки или окончания строки
* ```\w``` - Слово персонажа
* ```\W``` - Несловарный символ
* ```\d``` - Цифра
* ```\D``` - Нецифровый символ
* ```\s``` - Символ пробела
* ```\S``` - Не пробельный символ
* ```\b``` - Найти совпадение в начале / конце слова
* ```\B``` - Совпадение не в начале / конце слова
* ```\0``` - NUL символ
* ```\n``` - Символ новой строки
* ```\f``` - Символ фида формы
* ```\r``` - Символ возврата каретки
* ```\t``` - Символ табуляции
* ```\v``` - Символ вертикальной табуляции
* ```\xxx``` - Символ, указанный восьмеричным числом xxx
* ```\xdd``` - Символ, указанный шестнадцатеричным числом dd
* ```\uxxxx``` - Символ Unicode, указанный шестнадцатеричным числом xxxx

## Квантификаторы
* ```n+``` — Соответствует любой строке, которая содержит хотя бы один n
* ```n*``` — Любая строка, которая содержит ноль или более вхождений n
* ```n?``` — Строка, которая содержит ноль или одно вхождение n
* ```n{X}``` — Строка, содержащая последовательность из X n
* ```n{X,Y}``` — Строки, содержащие последовательность от X до Y n
* ```n{X,}``` — Соответствует любой строке, которая содержит последовательность не менее X n
* ```n$``` — Любая строка с n в конце
* ```^n``` — Строка с n в начале
* ```?=n``` — Любая строка, за которой следует определенная строка n
* ```?!n``` — Строка, за которой не следует определенная строка ni
