## JavaScript Cheat Sheet на русском языке
Вольный перевод JavaScript шпаргкалки с этого ресурса
https://websitesetup.org/javascript-cheat-sheet/

Возможно в будущем будет корректироваться и дополняться информацией, не представленной по ссылке выше.

# Основы JavaScript
Начнем с простых вещей - как подключить JavaScript к веб-сайту

## Добавление JavaScript на HTML страницу
Чтобы подключить JavaScript к странице, следует обернуть JS-код в тег <script>:
```
<script type="text/javascript">
//JS code goes here
</script>
```

## Вызываем JavaScript-фаил извне
JavaScript код можно разместить в своем собственном файле и вызвать его изнутри HTML. Так делают, когда следует разделить скрипты, выполняющие разные функции, чтобы избежать путаницы. Если ваш код находится в файле с именем myscript.js, его можно подключить таким образом:
```
<script src="myscript.js"></script><code></code>
```

## Добавляем комментарии к коду
Комментарии помогают понять, что происходит в вашем коде. Помните, что они должны быть помечены правильно, чтобы браузер не пытался их выполнить.

JavaScript предлагает вам две опции:
* Однострочные комментарии - комментируют лишь одну строку с помощью ```//```
* Многострочные комментарии - если вы хотите написать более длинные комментарии, поместите их в ```/ *``` и ```* /```, чтобы избежать их выполнения браузером.

# Переменные в JS
Переменная - зарезервированное место в памяти компьютера, которое можно использовать для сохранения некоторых данных и в последующем, выполнять нужные операций. Они могут быть вам знакомы со школьной скамьи. Как пример x, y, z использующиеся в уравнениях, в которые можно было подставить число для вычисления нужных значений.

## var, const, let
У вас есть три различных способа объявления переменной в JavaScript, каждая из которых имеет свои особенности:

* var — Переменная часто использующася в старых проектах. Может быть переназначена, но только внутри функции. Переменные типа ```var``` могут производить всплытие. Всплытие позволяет запускать объявленные функции выше, чем они объявлены в контексте функции.
* const — Не может быть переназначена, объявленна повторно и не подвержена всплытию.
* let — В отличии от ```const```, переменная ```let``` может быть переназначена, но не может быть объявлена повторно и тоже не подвержена всплытию.

## Типы данных
Переменные могут содержать различные типы значений и типов данных. Используйте знак равенства ```=```, чтобы присвоить их:

* Числа — ```var age = 23```
* Переменные — ```var x```
* Текст (строки) — ```var a = "init"```
* Операции — ```var b = 1 + 2 + 3```
* Истинные или ложные значения — ```var c = true```
* Константы — ```const PI = 3.14```
* Объекты — ```var name = {firstName:"John", lastName:"Doe"}```

Обратите внимание, что переменные чувствительны к регистру. Это означает, что ```lastname``` и ``` lastName``` будут обрабатываться как две разные переменные.

## Объекты
Объекты - определенный вид переменных, которые могут иметь свои собственные значения и методы. Последние являются действиями, которые вы можете совершать над объектами.
```
var person = {
    firstName:"John",
    lastName:"Doe",
    age:20,
    nationality:"German"
};
```

# Следующий уровень: Массивы
Далее в нашей шпаргалке JavaScript находятся массивы. Массивы являются частью разных языков программирования. Они помогают группировать переменные и свойства. Вот как это делается в JS:
```
var fruit = ["Banana", "Apple", "Pear"];
```
Теперь у вас есть массив с именем ```fruit```, который содержит три элемента, которые вы можете использовать в последующих операциях.

## Методы для работы с массивами
После того, как вы создали массивы, вы можете применить следующие методы:

* ```concat()``` — Объединяет несколько массивов в один
* ```indexOf()``` — Ищет индекс элемента в массиве, если элемента нет - возращает -1
* ```join()``` — Объединяет элементы массива в одну строку и возращает эту строку
* ```lastIndexOf()``` — Ищет последний встречающийся индекс элемента в массиве
* ```pop()``` — Удаляет последний элемент массива
* ```push()``` — Добавляет новый элемент в конце
* ```reverse()``` — Сортировка элементов в обратном порядке
* ```shift()``` — Удаляет первый элемент массива
* ```slice()``` — Возвращает новый массив, содержащий копию части исходного массива
* ```sort()``` — Сортирует элементы по алфавиту
* ```splice()``` — Изменяет содержимое массива, удаляя существующие элементы и/или добавляя новые.
* ```toString()``` — Преобразует элементы в строку
* ```unshift()``` — Добавляет новый элемент в начало массива
* ```valueOf()``` — Возвращает примитивное значение указанного объекта, чаще всего используется для преобразования в число

# Операторы
Если у вас есть переменные, вы можете использовать их для выполнения различных видов операций:

## Простые операторы
* ```+``` — Сложение
* ```-``` — Вычитание
* ```*``` — Умножение
* ```/``` — Деление
* ```(...)``` — Скобки - оператор группировки, операции в них выполняются раньше остальных внутри выражения
* ```%``` — Остаток от деления
* ```++``` — Инкремент числа (+1 к значению)
* ```--``` — Декремент числа (-1 от значения)

## Операторы сравнения
* ```==``` — Возвращает true, если операнды равны.
* ```===``` — Строгое равенство. Возвращает true, если операнды равны и имеют одинаковый тип.
* ```!=``` — Возвращает true, если операнды не равны.
* ```!==``` — Строгое неравенство. Возвращает true, если операнды не равны и/или имеют разный тип.
* ```>``` — Больше
* ```<``` — Меньше
* ```>=``` — Больше или равно
* ```<=``` — Меньше или равно
* ```?``` — Тернарный оператор (условие ? возращает значение если истина : возращает значение если ложь)

## Логические операторы
* ```&&``` — Логический оператор И
* ```||``` — Логический оператор ИЛИ
* ```!``` — Логическое НЕ

## Битовые операторы
* ```&``` — Возвращает единицу в каждой битовой позиции, для которой соответствующие биты обеих операндов являются единицами.
* ```|``` — Возвращает единицу в каждой битовой позиции, для которой один из соответствующих битов или оба бита операндов являются единицами.
* ```~``` — Заменяет биты операнда на противоположные
* ```^``` — Возвращает единицу в каждой битовой позиции, для которой только один из соответствующих битов операндов является единицей.
* ```<<``` — Сдвигает в двоичном представлении на бит влево
* ```>>``` — Сдвигает в двоичном представлении на бит вправо
* ```>>>``` — Сдвигает в двоичном представлении на бит вправо, отбрасывая сдвигаемые биты

# Функции
Функции JavaScript - блоки кода, которые выполняют определенную задачу. Простейшая функция выглядит следующим образом:
```
function name(parameter1, parameter2, parameter3) {
    // то, что должна выполнить функция
}
```
Как видите, она состоит из ключевого слова ```function``` и ее имени. Параметры функции находятся в скобках, а в фигурных скобках - то что функция выполняет. Вы можете создать свою собственную функцию, но чтобы сделать вашу жизнь чуть проще - есть ряд функций и методов встроенных в JS.

## Вывод данных
Используйте следующие функции для вывода данных:

* ```alert()``` — Вывод данных в окне браузера (по идее должно использоваться как окно предупреждения, но чаще используется начинающими разработчиками для разработки первых программ)
* ```confirm()``` — Открывает диалоговое окно с выбором "да / нет" и возвращает true / false в зависимости от клика пользователя
* ```console.log()``` — Записывает информацию в консоль браузера, довольно неплохо подходит для отладки кода
* ```document.write()``` — Дописывает текст в текущее место HTML ещё до того, как браузер построит из него DOM.
* ```prompt()``` — Создает диалоговое окно для пользовательского ввода

## Глобальные функции
Глобальные функции - функции встроенные в каждый браузерподдерживающий JavaScript.

* ```decodeURI()``` — Декодирует [Uniform Resource Identifier](https://ru.wikipedia.org/wiki/URI "Википедия url") в читабельный вид
* ```decodeURIComponent()``` — Декодирует последовательности символов в URI компоненте
* ```encodeURI()``` — Кодирует URI в UTF-8
* ```encodeURIComponent()``` — Тоже самое только для URI компонентов
* ```eval()``` — Выполняет код JavaScript, представленный в виде строки (например, eval('2 + 2') вернет 4)
* ```isFinite()``` — Определяет, является ли переданное значение конечным числом
* ```isNaN()``` — Определяет, является ли значение NaN или нет
* ```Number()``` — Возвращает число, преобразованное из его аргумента
* ```parseFloat()``` — Принимает строку в качестве аргумента и возвращает десятичное число
* ```parseInt()``` — принимает строку в качестве аргумента и возвращает целое число

# Циклы в JavaScript
Циклы являются частью большинства языков программирования. Они позволяют выполнять блоки кода нужное количество раз с разными значениями:
```
for (значение до запуска; условие прерывания; изменение значения после совершения итерации) {
    // необходимые действия во время цикла
}
```
У вас есть несколько параметров для создания циклов:

* ```for``` — Самый распространенный способ создания цикла в JavaScript
* ```while``` — Устанавливает условия, при которых выполняется цикл
* ```do while``` — Похожий на ```while``` цикл, но он выполняется по крайней мере один раз и в конце выполняет проверку, чтобы проверить, выполнено ли условие для повторного выполнения
* ```break``` — Используется для остановки и выхода из цикла при определенных условиях
* ```continue``` — Пропускает части цикла, если соблюдены определенные условия

# Оператор If - Else
Используя ```if``` и ```else```, вы cможете установить условия, для выполнения вашего кода. Если применяются определенные условия, что-то выполняется, если нет - выполняется что-то другое.
```
if (условие) {
    // выполняется, если условие выполнено
} else {
    // выполняется, если условие не выполнено
}
```
Концепция, похожая на ```if else```, - это выражение ``` switch```. Однако, используя ``` switch```, вы выбираете один из нескольких блоков кода для выполнения.
```
switch (состояние) {
  case state1:
    // выполняется, если состояние = state1
    break;
  case state2:
    // выполняется, если состояние = state2
    break;
  default:
    // выполняется, по умолчанию
}
```

# Строки
Строками в JS являются любые текстовые данные.
```
var person = "John Doe";
```
В этом случае, ```John Doe``` является строкой.

## Спецсимволы
В JavaScript строки помечаются одинарными или двойными кавычками. Если вы хотите использовать кавычки в строке, вам нужно использовать специальные символы:

* ```\'``` — Ординарная кавычка
* ```\"``` — Двойная кавычка

Помимо этого у вас также есть дополнительные спецсимволы:
* ```\\``` - Обратная косая черта
* ```\n``` - Новая строка
* ```\r``` - возврат каретки
* ```\t``` - Горизонтальный табулятор

## Методы работы со строками

* ```charAt()``` — Возвращает символ в указанной позиции внутри строки
* ```charCodeAt()``` — Дает вам юникод символа в этой позиции
* ```concat()``` — Объединяет (объединяет) две или более строки в одну
* ```fromCharCode()``` — Возвращает строку, созданную из указанной последовательности единиц кода UTF-16
* ```indexOf()``` — Предоставляет индекс первого вхождения указанного текста в строке
* ```lastIndexOf()``` — То же, что ```indexOf ()```, но с последним вхождением, поиск в обратном направлении
* ```match()``` — Возвращает получившиеся совпадения при сопоставлении строки с регулярным выражением.
* ```replace()``` — Найти и заменить определенный текст в строке
* ```search()``` — Выполняет поиск сопоставления между регулярным выражением и строкой
* ```slice()``` — Извлекает часть строки и возвращает ее как новую строку
* ```split()``` — Разбивает строку на массив строк путём разделения строки указанной подстрокой.
* ```substr()``` —  Возвращает указанное количество символов из строки, начиная с указанной позиции.
* ```substring()``` —  Возвращает подстроку строки между двумя индексами, или от одного индекса и до конца строки.
* ```toLowerCase()``` — Конвертирует значение строки в нижний регистр
* ```toUpperCase()``` — Конвертирует значение строки в верхний регистр
* ```valueOf()``` — Возвращает примитивное значение объекта String.

# Регулярные выражения
Важная тема, но как будто бы не так сильно, относящаяся к JS. 
По этому я создал отдельный фаил где будет хранится перевод с регулярными выражениями:
https://github.com/rocketrussia/js-cheat-sheet/blob/master/REGEX.md

# Числа и Вычисления
В JavaScript вы  можете работать с числами, константами и выполнять математические функции.

## Свойства чисел
* ```MAX_VALUE``` — Максимальное числовое значение
* ```MIN_VALUE``` — Наименьшее положительное числовое значение, представимое в JavaScript
* ```NaN``` — Значение "Не число". Является числом &#129335;&zwj;&#9794;
* ```NEGATIVE_INFINITY``` — Отрицательное значение бесконечности
* ```POSITIVE_INFINITY``` — Положительное значение бесконечности

## Числовые методы
* ```toExponential()``` — Возвращает строку с округленным числом, записанным в виде экспоненциальной записи
* ```toFixed()``` — Возвращает строку числа с указанным количеством десятичных знаков
* ```toPrecision()``` — Строка числа, написанного с указанной длиной
* ```toString()``` — Возвращает число в виде строки
* ```valueOf()``` — Возвращает число как число

## Математические свойства
* ```E``` — Основание натурального логарифма, математическая константа, иррациональное и трансцендентное число
* ```LN2``` — Натуральный логарифм в степени 2
* ```LN10``` — Натуральный логарифм в степени 10
* ```LOG2E``` — Двоичный логарифм из e
* ```LOG10E``` — Десятичный логарифм из e
* ```PI``` — Число "Пи"
* ```SQRT1_2``` — Квадратный корень из 1/2
* ```SQRT2``` — Квадратный корень из 2

## Математические методы
* ```abs(x)``` — Абсолютное значение числа от x
* ```acos(x)``` — Арккосинус числа (в радианах) от x
* ```asin(x)``` — Арксинус числа (в радианах) от x
* ```atan(x)``` — Арктангенс числа (в радианах) от x
* ```atan2(y,x)``` — Аарктангенс от частного аргументов y и x
* ```ceil(x)``` — Округляет аргумент x до ближайшего большего целого
* ```cos(x)``` — Косинус числа x
* ```exp(x)``` — Кначение выражения e^x, где x — аргумент метода, а e — число Эйлера, основание натурального логарифма.
* ```floor(x)``` — Целое число, которое меньше или равно числу x.
* ```log(x)``` — Натуральный логарифм от x
* ```max(x,y,z,...,n)``` — Возращает максимальное число
* ```min(x,y,z,...,n)``` — Возращает минимальное число
* ```pow(x,y)``` — Возводит x в степень y
* ```random()``` — Возращает рандомное число от 0 до 1
* ```round(x)``` — Возвращает число, округлённое к ближайшему целому
* ```sin(x)``` — Синус числа (в радианах) от x
* ```sqrt(x)``` — Квадратный корень от x
* ```tan(x)``` — Тангенс числа x

# Dealing with Dates in JavaScript
You can also work with and modify dates and time with JavaScript. This is the next chapter in the JavaScript cheat sheet.

## Setting Dates
* ```Date()``` — Creates a new date object with the current date and time
* ```Date(2017, 5, 21, 3, 23, 10, 0)``` — Create a custom date object. The numbers represent a year, month, day, hour, minutes, seconds, milliseconds. You can omit anything you want except for year and month.
* ```Date("2017-06-23")``` — Date declaration as a string

## Pulling Date and Time Values
* ```getDate()``` — Get the day of the month as a number (1-31)
* ```getDay()``` —  The weekday as a number (0-6)
* ```getFullYear()``` — Year as a four-digit number (yyyy)
* ```getHours()``` — Get the hour (0-23)
* ```getMilliseconds()``` — The millisecond (0-999)
* ```getMinutes()``` — Get the minute (0-59)
* ```getMonth()``` —  Month as a number (0-11)
* ```getSeconds()``` — Get the second (0-59)
* ```getTime()``` — Get the milliseconds since January 1, 1970
* ```getUTCDate()``` — The day (date) of the month in the specified date according to universal time (also available for day, month, full year, hours, minutes etc.)
* ```parse()``` — Parses a string representation of a date and returns the number of milliseconds since January 1, 1970

## Set Part of a Date
* ```setDate()``` — Set the day as a number (1-31)
* ```setFullYear()``` — Sets the year (optionally month and day)
* ```setHours()``` — Set the hour (0-23)
* ```setMilliseconds()``` — Set milliseconds (0-999)
* ```setMinutes()``` — Sets the minutes (0-59)
* ```setMonth()``` — Set the month (0-11)
* ```setSeconds()``` — Sets the seconds (0-59)
* ```setTime()``` — Set the time (milliseconds since January 1, 1970)
* ```setUTCDate()``` — Sets the day of the month for a specified date according to universal time (also available for day, month, full year, hours, minutes etc.)

# Внимание
Информация следующая далее находится в процессе перевода на русский язык

```
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
```

# DOM Mode
The DOM is the Document Object Model of a page. It is the code of the structure of a webpage. JavaScript comes with a lot of different ways to create and manipulate HTML elements (called nodes).

## Node Properties
* ```attributes``` — Returns a live collection of all attributes registered to an element
* ```baseURI``` — Provides the absolute base URL of an HTML element
* ```childNodes``` — Gives a collection of an element’s child nodes
* ```firstChild``` — Returns the first child node of an element
* ```lastChild``` — The last child node of an element
* ```nextSibling``` — Gives you the next node at the same node tree level
* ```nodeName``` — Returns the name of a node
* ```nodeType``` —  Returns the type of a node
* ```nodeValue``` — Sets or returns the value of a node
* ```ownerDocument``` — The top-level document object for this node
* ```parentNode``` — Returns the parent node of an element
* ```previousSibling``` — Returns the node immediately preceding the current one
* ```textContent``` — Sets or returns the textual content of a node and its descendants

## Node Methods
* ```appendChild()``` — Adds a new child node to an element as the last child node
* ```cloneNode()``` — Clones an HTML element
* ```compareDocumentPosition()``` — Compares the document position of two elements
* ```getFeature()``` — Returns an object which implements the APIs of a specified feature
* ```hasAttributes()``` — Returns true if an element has any attributes, otherwise false
* ```hasChildNodes()``` — Returns true if an element has any child nodes, otherwise false
* ```insertBefore()``` — Inserts a new child node before a specified, existing child node
* ```isDefaultNamespace()``` — Returns true if a specified namespaceURI is the default, otherwise false
* ```isEqualNode()``` — Checks if two elements are equal
* ```isSameNode()``` — Checks if two elements are the same node
* ```isSupported()``` — Returns true if a specified feature is supported on the element
* ```lookupNamespaceURI()``` — Returns the namespace URI associated with a given node
* ```lookupPrefix()``` — Returns a DOMString containing the prefix for a given namespace URI, if present
* ```normalize()``` — Joins adjacent text nodes and removes empty text nodes in an element
* ```removeChild()``` — Removes a child node from an element
* ```replaceChild()``` — Replaces a child node in an element

## Element Methods
* ```getAttribute()``` — Returns the specified attribute value of an element node
* ```getAttributeNS()``` — Returns string value of the attribute with the specified namespace and name
* ```getAttributeNode()``` — Gets the specified attribute node
* ```getAttributeNodeNS()``` — Returns the attribute node for the attribute with the given namespace and name
* ```getElementsByTagName()``` — Provides a collection of all child elements with the specified tag name
* ```getElementsByTagNameNS()``` —  Returns a live HTMLCollection of elements with a certain tag name belonging to the given namespace
* ```hasAttribute()``` — Returns true if an element has any attributes, otherwise false
* ```hasAttributeNS()``` — Provides a true/false value indicating whether the current element in a given namespace has the specified attribute
* ```removeAttribute()``` — Removes a specified attribute from an element
* ```removeAttributeNS()``` — Removes the specified attribute from an element within a certain namespace
* ```removeAttributeNode()``` — Takes away a specified attribute node and returns the removed node
* ```setAttribute()``` — Sets or changes the specified attribute to a specified value
* ```setAttributeNS()``` —  Adds a new attribute or changes the value of an attribute with the given namespace and name
* ```setAttributeNode()``` — Sets or changes the specified attribute node
* ```setAttributeNodeNS()``` — Adds a new namespaced attribute node to an element

# Working with the User Browser
Besides HTML elements, JavaScript is also able to take into account the user browser and incorporate its properties into the code.

## Window Properties
* ```closed``` — Checks whether a window has been closed or not and returns true or false
* ```defaultStatus``` — Sets or returns the default text in the status bar of a window
* ```document``` — Returns the document object for the window
* ```frames``` — Returns all iframe elements in the current window
* ```history``` — Provides the History object for the window
* ```innerHeight``` — The inner height of a window’s content area
* ```innerWidth``` — The inner width of the content area
* ```length``` — Find out the number of  iframe elements in the window
* ```location``` — Returns the location object for the window
* ```name``` — Sets or returns the name of a window
* ```navigator``` — Returns the Navigator object for the window
* ```opener``` — Returns a reference to the window that created the window
* ```outerHeight``` — The outer height of a window, including toolbars/scrollbars
* ```outerWidth``` — The outer width of a window, including toolbars/scrollbars
* ```pageXOffset``` — Number of pixels the current document has been scrolled horizontally
* ```pageYOffset``` — Number of pixels the document has been scrolled vertically
* ```parent``` — The parent window of the current window
* ```screen``` — Returns the Screen object for the window
* ```screenLeft``` — The horizontal coordinate of the window (relative to the screen)
* ```screenTop``` — The vertical coordinate of the window
* ```screenX``` — Same as screenLeft but needed for some browsers
* ```screenY``` — Same as screenTop but needed for some browsers
* ```self``` — Returns the current window
* ```status``` — Sets or returns the text in the status bar of a window
* ```top``` — Returns the topmost browser window
    
## Window Methods
* ```alert()``` — Displays an alert box with a message and an OK button
* ```blur()``` — Removes focus from the current window
* ```clearInterval()``` — Clears a timer set with setInterval()
* ```clearTimeout()``` — Clears a timer set with setTimeout()
* ```close()``` — Closes the current window
* ```confirm()``` — Displays a dialogue box with a message and an OK and Cancel button
* ```focus()``` — Sets focus to the current window
* ```moveBy()``` — Moves a window relative to its current position
* ```moveTo()``` — Moves a window to a specified position
* ```open()``` — Opens a new browser window
* ```print()``` — Prints the content of the current window
* ```prompt()``` — Displays a dialogue box that prompts the visitor for input
* ```resizeBy()``` — Resizes the window by the specified number of pixels
* ```resizeTo()``` — Resizes the window to a specified width and height
* ```scrollBy()``` — Scrolls the document by a specified number of pixels
* ```scrollTo()``` — Scrolls the document to specified coordinates
* ```setInterval()``` — Calls a function or evaluates an expression at specified intervals
* ```setTimeout()``` — Calls a function or evaluates an expression after a specified interval
* ```stop()``` — Stops the window from loading

## Screen Properties
* ```availHeight``` — Returns the height of the screen (excluding the Windows Taskbar)
* ```availWidth``` — Returns the width of the screen (excluding the Windows Taskbar)
* ```colorDepth``` — Returns the bit depth of the color palette for displaying images
* ```height``` — The total height of the screen
* ```pixelDepth``` — The color resolution of the screen in bits per pixel
* ```width``` — The total width of the screen

# JavaScript Events
Events are things that can happen to HTML elements and are performed by the user. The programming language can listen for these events and trigger actions in the code. No JavaScript cheat sheet would be complete without them.

## Mouse
* ```onclick``` — The event occurs when the user clicks on an element
* ```oncontextmenu``` — User right-clicks on an element to open a context menu
* ```ondblclick``` — The user double-clicks on an element
* ```onmousedown``` — User presses a mouse button over an element
* ```onmouseenter``` — The pointer moves onto an element
* ```onmouseleave``` — Pointer moves out of an element
* ```onmousemove``` — The pointer is moving while it is over an element
* ```onmouseover``` — When the pointer is moved onto an element or one of its children
* ```onmouseout``` — User moves the mouse pointer out of an element or one of its children
* ```onmouseup``` — The user releases a mouse button while over an element

##Keyboard
* ```onkeydown``` — When the user is pressing a key down
* ```onkeypress``` — The moment the user starts pressing a key
* ```onkeyup``` — The user releases a key

## Frame
* ```onabort``` — The loading of a media is aborted
* ```onbeforeunload``` — Event occurs before the document is about to be unloaded
* ```onerror``` — An error occurs while loading an external file
* ```onhashchange``` — There have been changes to the anchor part of a URL
* ```onload``` — When an object has loaded
* ```onpagehide``` — The user navigates away from a webpage
* ```onpageshow``` — When the user navigates to a webpage
* ```onresize``` — The document view is resized
* ```onscroll``` — An element’s scrollbar is being scrolled
* ```onunload``` — Event occurs when a page has unloaded

## Form
* ```onblur``` — When an element loses focus
* ```onchange``` — The content of a form element changes (for input, select and textarea)
* ```onfocus``` — An element gets focus
* ```onfocusin``` — When an element is about to get focus
* ```onfocusout``` — The element is about to lose focus
* ```oninput``` — User input on an element
* ```oninvalid``` — An element is invalid
* ```onreset``` — A form is reset
* ```onsearch``` — The user writes something in a search field (for input="search")
* ```onselect``` — The user selects some text (for input and textarea)
* ```onsubmit``` — A form is submitted
    
## Drag
* ```ondrag``` — An element is dragged
* ```ondragend``` — The user has finished dragging the element
* ```ondragenter``` — The dragged element enters a drop target
* ```ondragleave``` — A dragged element leaves the drop target
* ```ondragover``` — The dragged element is on top of the drop target
* ```ondragstart``` — User starts to drag an element
* ```ondrop``` — Dragged element is dropped on the drop target

## Clipboard
* ```oncopy``` — User copies the content of an element
* ```oncut``` — The user cuts an element’s content
* ```onpaste``` — A user pastes content in an element

## Media
* ```onabort``` — Media loading is aborted
* ```oncanplay``` — The browser can start playing media (e.g. a file has buffered enough)
* ```oncanplaythrough``` — The browser can play through media without stopping
* ```ondurationchange``` — The duration of the media changes
* ```onended``` — The media has reached its end
* ```onerror``` — Happens when an error occurs while loading an external file
* ```onloadeddata``` — Media data is loaded
* ```onloadedmetadata``` — Metadata (like dimensions and duration) are loaded
* ```onloadstart``` —  The browser starts looking for specified media
* ```onpause``` — Media is paused either by the user or automatically
* ```onplay``` — The media has been started or is no longer paused
* ```onplaying``` — Media is playing after having been paused or stopped for buffering
* ```onprogress``` — The browser is in the process of downloading the media
* ```onratechange``` — The playing speed of the media changes
* ```onseeked``` — User is finished moving/skipping to a new position in the media
* ```onseeking``` — The user starts moving/skipping
* ```onstalled``` — The browser is trying to load the media but it is not available
* ```onsuspend``` — The browser is intentionally not loading media
* ```ontimeupdate``` — The playing position has changed (e.g. because of fast forward)
* ```onvolumechange``` — Media volume has changed (including mute)
* ```onwaiting``` — Media paused but expected to resume (for example, buffering)

## Animation
* ```animationend``` — A CSS animation is complete
* ```animationiteration``` — CSS animation is repeated
* ```animationstart``` — CSS animation has started

## Other
* ```transitionend``` — Fired when a CSS transition has completed
* ```onmessage``` — A message is received through the event source
* ```onoffline``` — The browser starts to work offline
* ```ononline``` — The browser starts to work online
* ```onpopstate``` — When the window’s history changes
* ```onshow``` — A menu element is shown as a context menu
* ```onstorage``` — A Web Storage area is updated
* ```ontoggle``` — The user opens or closes the details element
* ```onwheel``` — Mouse wheel rolls up or down over an element
* ```ontouchcancel``` — Screen-touch is interrupted
* ```ontouchend``` — User’s finger is removed from a touch-screen
* ```ontouchmove``` — A finger is dragged across the screen
* ```ontouchstart``` — A finger is placed on the touch-screen
    
# Errors
When working with JavaScript, different errors can occur. There are several ways of handling them:

* ```try``` — Lets you define a block of code to test for errors
* ```catch``` — Set up a block of code to execute in case of an error
* ```throw``` — Create custom error messages instead of the standard JavaScript errors
* ```finally``` — Lets you execute code, after try and catch, regardless of the result

## Error Name Values
JavaScript also has a built-in error object. It has two properties:

* ```name``` — Sets or returns the error name
* ```message``` — Sets or returns an error message in string from
The error property can return six different values as its name:

* ```EvalError``` — An error has occurred in the ```eval()``` function
* ```RangeError``` — A number is “out of range”
* ```ReferenceError``` — An illegal reference has occurred
* ```SyntaxError``` — A syntax error has occurred
* ```TypeError``` — A type error has occurred
* ```URIError``` — An ```encodeURI()``` error has occurred

# Вкратце об шпаргалке JavaScript
В последние годы JavaScript приобрел большую популярность как язык программирования. Все большее число людей используют его для создания как относительно простых веб-страниц до монструозных приложений. Все это благодаря объемному послужному списку и большому числу преимуществ.

В приведенной выше шпаргалке, мы собрали множество самых основных и важных операторов, функций, принципов и методов. Она предоставляет хороший обзор языка и справку для опытных и начинающих разработчиков. Мы надеемся, что вы смогли использовать в полной мере данный материал.
