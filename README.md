## JavaScript Cheat Sheet на русском языке
Вольный перевод JavaScript шпаргкалки с этого ресурса
https://websitesetup.org/javascript-cheat-sheet/

Возможно в будущем будет корректироваться и дополняться информацией, не представленной по ссылке выше.
Также стоит отметить, что некоторые устаревшие функции убраны из шпаргалки. Подробности: [MDN](https://developer.mozilla.org/ru/docs/Web "MDN web docs")

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
* ```split()``` — Разбивает строку на массив строк путём разделения строки указанной подстрокой
* ```substr()``` —  Возвращает указанное количество символов из строки, начиная с указанной позиции
* ```substring()``` —  Возвращает подстроку строки между двумя индексами, или от одного индекса и до конца строки
* ```toLowerCase()``` — Конвертирует значение строки в нижний регистр
* ```toUpperCase()``` — Конвертирует значение строки в верхний регистр
* ```valueOf()``` — Возвращает примитивное значение объекта String

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
* ```exp(x)``` — Кначение выражения e^x, где x — аргумент метода, а e — число Эйлера, основание натурального логарифма
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

# Работа с датами в JS
Вы также можете работать с датами и временем и изменять их с помощью JavaScript. Это следующая глава в чит-листе JavaScript.

## Установка даты
* ```Date()``` — Создает новый объект даты с текущей датой и временем
* ```Date(2017, 5, 21, 3, 23, 10, 0)``` — Создает пользовательский объект даты. Числа представляют год, месяц, день, час, минуты, секунды, миллисекунды. Вы можете опустить все, что хотите, кроме года и месяца
* ```Date("2017-06-23")``` — Объявление даты в виде строки

## Вытаскиваем дату и время
* ```getDate()``` — День месяца (1-31)
* ```getDay()``` —  День недели числом (0-6)
* ```getFullYear()``` — Четырхзначный год (yyyy)
* ```getHours()``` — Получаем час (0-23)
* ```getMilliseconds()``` — Миллисекунда (0-999)
* ```getMinutes()``` — Минуты(0-59)
* ```getMonth()``` —  Месяц (0-11)
* ```getSeconds()``` — Секунда (0-59)
* ```getTime()``` — Время в миллисекунданх с 1го января 1970 года
* ```getUTCDate()``` —  День месяца указанной даты по UTC
* ```parse()``` — разбирает строковое представление даты и возвращает количество миллисекунд, прошедших с 1го января 1970 года

##  Методы установки даты и времени
* ```setDate()``` — Устанавливает день (1-31)
* ```setFullYear()``` — Год (опционально месяц и день)
* ```setHours()``` — Час (0-23)
* ```setMilliseconds()``` — Миллисекунда (0-999)
* ```setMinutes()``` — Минута (0-59)
* ```setMonth()``` — Месяц (0-11)
* ```setSeconds()``` — Секунда (0-59)
* ```setTime()``` — Время в миллисекунданх с 1го января 1970 года
* ```setUTCDate()``` — День месяца указанной даты по UTC

# Работаем с DOM
DOM(Document Object Model) - объектная модель документа, представляет из себя структуру веб-страницы. JavaScript поставляется с множеством различных способов создания и управления HTML-элементами (называемыми узлами) - DOM API.

## Свойства Node
Node это интерфейс, от которого наследуют несколько типов DOM, он так же позволяет различным типам быть обработанными(или протестированными).

* ```attributes``` — Возвращает группу атрибутов всех узлов, зарегистрированных в указанном узле.
* ```baseURI``` — Возвращает абсолютный базовый URL узла (Свойство Node.baseURI только для чтения)
* ```childNode``` — Предоставляет коллекцию дочерних узлов элемента
* ```firstChild``` — Возвращает первый дочерний узел элемента
* ```lastChild``` — Последний дочерний узел элемента
* ```nextSibling``` — Дает вам следующий узел на том же уровне дерева узлов
* ```nodeName``` — Возвращает имя узла
* ```nodeType``` —  Возвращает тип узла
* ```nodeValue``` — Устанавливает или возвращает значение узла
* ```ownerDocument``` — Объект документа верхнего уровня для этого узла
* ```parentNode``` — Возвращает родительский узел элемента
* ```previousSibling``` — Возвращает узел, непосредственно предшествующий текущему
* ```textContent``` — Устанавливает или возвращает текстовое содержимое узла и его потомков

## Node методы
* ```appendChild()``` — Добавляет новый дочерний узел в элемент как последний дочерний узел
* ```cloneNode()``` — Клонирует элемент HTML
* ```compareDocumentPosition()``` — Сравнивает позицию текущего узла и другого узла в любом другом документе
* ```getFeature()``` — Возвращает объект, который реализует API указанной функции
* ```hasAttributes()``` — Возвращает true, если элемент имеет какие-либо атрибуты, иначе false
* ```hasChildNodes()``` — Возвращает true, если элемент имеет дочерние узлы, в противном случае false
* ```insertBefore()``` — Вставляет новый дочерний узел перед указанным существующим дочерним узлом
* ```isDefaultNamespace()``` — Возвращает true, если заданный namespaceURI является значением по умолчанию, иначе false
* ```isEqualNode()``` — Проверяет, равны ли два элемента
* ```isSameNode()``` — Проверяет, являются ли два элемента одним узлом
* ```isSupported()``` — Возвращает true, если указанная функция поддерживается для элемента
* ```lookupNamespaceURI()``` — Возвращает URI пространства имен, связанный с данным узлом
* ```lookupPrefix()``` — Возвращает DOMString, содержащую префикс для заданного URI пространства имен, если присутствует
* ```normalize()``` — Объединяет смежные текстовые узлы и удаляет пустые текстовые узлы в элементе
* ```removeChild()``` — Удаляет дочерний узел из элемента
* ```replaceChild()``` — Заменяет дочерний узел в элементе

## Element Methods
* ```getAttribute()``` - Возвращает указанное значение атрибута узла элемента
* ```getAttributeNS()``` - Возвращает строковое значение атрибута с указанным пространством имен и именем
* ```getAttributeNode()``` - Получает указанный узел атрибута
* ```getAttributeNodeNS()``` - Возвращает узел атрибута для атрибута с заданным пространством имен и именем
* ```getElementsByTagName()``` - Предоставляет коллекцию всех дочерних элементов с указанным именем тега
* ```getElementsByTagNameNS()``` - Возвращает живую коллекцию HTMLCol элементов с определенным именем тега, принадлежащим данному пространству имен
* ```hasAttribute()``` - Возвращает true, если элемент имеет какие-либо атрибуты, в противном случае false
* ```hasAttributeNS()``` - Предоставляет значение true / false, указывающее, имеет ли текущий элемент в данном пространстве имен заданный атрибут
* ```removeAttribute()``` - Удаляет указанный атрибут из элемента
* ```removeAttributeNS()``` - Удаляет указанный атрибут из элемента в определенном пространстве имен
* ```removeAttributeNode()``` - Забирает указанный узел атрибута и возвращает удаленный узел
* ```setAttribute()``` - Устанавливает или изменяет указанный атрибут на указанное значение
* ```setAttributeNS()``` - Добавляет новый атрибут или изменяет значение атрибута с заданным пространством имен и именем
* ```setAttributeNode()``` - Устанавливает или изменяет указанный атрибут узла
* ```setAttributeNodeNS()``` - Добавляет новый узел атрибута пространства имен к элементу

# Работа с браузером пользователя
Помимо элементов HTML, JavaScript также может учитывать браузер пользователя и включать его свойства в код.

## Window свойства
* ```closed``` — Проверяет, было ли окно закрыто или нет, и возвращает true или false
* ```defaultStatus``` — Устанавливает или возвращает текст по умолчанию в строке состояния окна
* ```document``` — Возвращает объект документа для окна
* ```frames``` —  Возвращает все элементы iframe в текущем окне
* ```history``` — Предоставляет объект History для окна
* ```innerHeight``` — Внутренняя высота контента данного окна
* ```innerWidth``` — Внутренняя ширина контента данного окна
* ```length``` — Количество элементов iframe в окне
* ```location``` — Возвращает местоположение объекта для данного окна
* ```name``` — Устанавливает или возвращает имя окна
* ```navigator``` — Возвращает объект Navigator для окна
* ```opener``` — Возвращает ссылку на новое окно, которая была создано в первоначальном окне(при использовании метода open())
* ```outerHeight``` — Внешняя высота окна, включая панели инструментов / полосы прокрутки
* ```outerWidth``` — Внешняя ширина окна, включая панели инструментов / полосы прокрутки
* ```pageXOffset``` — Количество пикселей, по которому текущий документ прокручивается по горизонтали
* ```pageYOffset``` — Количество пикселей, по которому текущий документ прокручивается по вертикали
* ```parent``` — Родительское окно текущего окна
* ```screen``` — Возвращает объект Screen для окна
* ```screenX``` — Горизонтальная координата окна
* ```screenY``` — Вертикальная координата окна
* ```self``` — Возвращает текущее окно
* ```status``` — Устанавливает или возвращает текст в строке состояния окна
* ```top``` — Возвращает ссылку на корневое окно в иерархии окон
    
## Window методы
* ```alert()``` — показывает диалоговое окно с опциональным сообщением и кнопкой OK.
* ```blur()``` — Убирает фокус с окна
* ```clearInterval()``` — Сбрасывает таймер, установленный с помощью setInterval ()
* ```clearTimeout()``` — Сбрасывает таймер, установленный с помощью setTimeout()
* ```close()``` — Закрывает текущее окно
* ```confirm()``` — Отображает диалоговое окно с сообщением и кнопкой ОК и Отмена
* ```focus()``` — Устанавливает фокус на текущее окно
* ```moveBy()``` — Перемещает окно относительно его текущей позиции
* ```moveTo()``` — Перемещает окно в указанную позицию
* ```open()``` — Открывает новое окно браузера
* ```print()``` — Печатает содержимое текущего окна
* ```prompt()``` — Отображает диалоговое окно, которое предлагает посетителю для ввода
* ```resizeBy()``` — Изменяет размер окна на указанное количество пикселей
* ```resizeTo()``` — Изменение размера окна до указанной ширины и высоты
* ```scrollBy()``` — Прокручивает документ на указанное количество пикселей
* ```scrollTo()``` — Прокручивает документ до указанных координат
* ```setInterval()``` — Вызывает функцию или оценивает выражение через заданные интервалы
* ```setTimeout()``` — Вызывает функцию или вычисляет выражение после указанного интервала
* ```stop()``` — Останавливает окно загрузки

## Свойства экрана
* ```availHeight``` — Высота, которую может иметь окно браузера, если она максимизирована, включая полосы браузера
* ```availWidth``` — Ширина, которую может иметь окно браузера, если она максимизирована, включая полосы браузера
* ```colorDepth``` — Возвращает битовую глубину цветовой палитры для отображения изображений
* ```height``` — Общая высота экрана
* ```pixelDepth``` — Цветовое разрешение экрана в битах на пиксель
* ```width``` — Общая ширина экрана

# События JavaScript
События могут происходить с элементами HTML и выполняются пользователем. Язык программирования может прослушивать эти события и запускать действия в коде. Чит-лист JavaScript не будет полным без них.

## Мышь
* ```onclick``` — Событие происходит, когда пользователь нажимает на элемент
* ```oncontextmenu``` — Пользователь щелкает правой кнопкой мыши элемент, чтобы открыть контекстное меню
* ```ondblclick``` — Пользователь дважды щелкает по элементу
* ```onmousedown``` — Пользователь нажимает кнопку мыши(но еще не отпускает)
* ```onmouseenter``` — Курсор перемещается в зону отображения элемента
* ```onmouseleave``` — Курсор выходит из зоны отображения элемента
* ```onmousemove``` — Курсор движется, когда он находится в зоне отображения элемента
* ```onmouseover``` — Курсор перестал двигатся, вовремя нахождения в зоне отображения элемента
* ```onmouseout``` — Пользователь перемещает указатель мыши на один из дочерних элементов элемента
* ```onmouseup``` — Пользователь отпускает кнопку мыши над элементом

## Клавиатура
* ```onkeydown``` — Пользователь нажимает клавишу вниз
* ```onkeypress``` — Момент, когда пользователь начинает нажимать клавишу
* ```onkeyup``` — Пользователь отпускает клавишу

## Фрейм
* ```onabort``` — Загрузка фаила прервана
* ```onbeforeunload``` — Событие происходит перед выгрузкой документа
* ```onerror``` — При загрузке внешнего файла возникает ошибка
* ```onhashchange``` — Произошли изменения в части привязки URL
* ```onload``` — Как только объект загружен
* ```onpagehide``` — Пользователь покидает веб-страницу
* ```onpageshow``` — Когда пользователь переходит на веб-страницу
* ```onresize``` — Отслеживает изменения размеров произвольного элемента на странице
* ```onscroll``` — Полоса прокрутки элемента прокручивается
* ```onunload``` — Когда страница не загрузилась по каким-либо причинам, либо при закрытии окна (вкладки) браузера.

## Форма
* ```onblur``` — Когда элемент теряет фокус
* ```onchange``` — Изменяется содержимое элемента формы (для input, select и textarea)
* ```onfocus``` — Элемент в фокусе
* ```onfocusin``` — Когда элемент собирается получить фокус
* ```onfocusout``` — Элемент собирается потерять фокус
* ```oninput``` — Пользовательский ввод
* ```oninvalid``` — Элемент невалиден
* ```onreset``` — Сброс формы
* ```onsearch``` — Пользователь что-то пишет в поле поиска (для input="search")
* ```onselect``` — Пользователь выбирает некоторый текст (для input и textarea)
* ```onsubmit``` — Форма отправлена
    
## Перетаскивание
* ```ondrag``` — Элемент перетаскивается
* ```ondragend``` — Пользователь закончил перетаскивание элемента
* ```ondragenter``` — Перетаскиваемый элемент входит в целевой объект
* ```ondragleave``` — Перетаскиваемый элемент покидает целевой объект
* ```ondragover``` — Перетаскиваемый элемент находится поверх цели сброса
* ```ondragstart``` — Пользователь начал перетаскивать элемент
* ```ondrop``` — Перетаскиваемый элемент сброшен в целевой объект

## Буфер обмена
* ```oncopy``` — Пользователь копирует содержимое элемента
* ```oncut``` — Пользователь вырезает содержимое элемента
* ```onpaste``` — Пользователь вставляет содержимое в элемент

## Медиа
* ```onabort``` — Загрузка медиа-фаила прервана
* ```oncanplay``` — Браузер может начать воспроизведение медиа-фаила (например, файл достаточно буферизован)
* ```oncanplaythrough``` — Браузер может воспроизводить медиа-файлы без остановки
* ```ondurationchange``` — Продолжительность воспроизведения медиа-фаила изменена
* ```onended``` — Достигнут конец медиа-фаила при воспроизведении
* ```onerror``` — Когда при загрузке внешнего файла возникает ошибка
* ```onloadeddata``` — Медиа данные загружены
* ```onloadedmetadata``` — Метаданные (например, размеры и продолжительность) загружаются
* ```onloadstart``` —  Браузер начинает поиск указанного медиа-фаила
* ```onpause``` — Воспроизведение медиа-фаила приостанавливается либо пользователем, либо автоматически
* ```onplay``` — Медиа-фаил запущен или больше не приостановлен
* ```onplaying``` — Медиа-фаил воспроизводится после того, как была приостановлена или остановлена для буферизации
* ```onprogress``` — Браузер в процессе загрузки медиа-фаила
* ```onratechange``` — Скорость воспроизведения медиа изменена
* ```onseeked``` — Когда операция поиска завершена, текущая позиция воспроизведения изменилась
* ```onseeking``` — Пользователь начинает движение / скипает
* ```onstalled``` —  Браузер пытается загрузить медиа-фаил, но он недоступен
* ```onsuspend``` — Браузер намеренно не загружает медиа-фаил
* ```ontimeupdate``` — Проигроваемая позиция изменилась (например, из-за ускоренной перемотки вперед)
* ```onvolumechange``` — Громкость медиа-фаила изменилась (включая отключение звука)
* ```onwaiting``` — Воспроизведение медиа-фаила приостановлено, но ожидается возобновление (например, буферизация)

## Анимации
* ```animationstart``` — CSS анимация началась
* ```animationiteration``` — CSS анимация повторяется
* ```animationend``` — CSS анимация завершена

## Прочее
* ```transitionend``` — Срабатывает после завершения CSS-перехода
* ```onmessage``` — Сообщение получено через источник события
* ```onoffline``` — Браузер начинает работать в автономном режиме
* ```ononline``` — Браузер начинает работать в онлайн режиме
* ```onpopstate``` — При изменении истории окна
* ```onshow``` — Элемент меню отображается в виде контекстного меню
* ```onstorage``` — Область веб-хранилища обновлена
* ```ontoggle``` — Пользователь открывает или закрывает элемент данных
* ```onwheel``` — Колесо мыши катится вверх или вниз по элементу
* ```ontouchcancel``` — Сенсорный экран прерывается
* ```ontouchend``` — Палец пользователя убран с сенсорного экрана
* ```ontouchmove``` — Палец передвигается по экрану
* ```ontouchstart``` — Палец коснулся сенсорного экрана
    
# Ошибки
При работе с JavaScript могут возникать разные ошибки. Есть несколько способов справиться с ними:

* ```try``` — Позволяет определить блок кода для проверки на ошибки
* ```catch``` — Настройте этот блок кода для выполнения в случае ошибки
* ```throw``` — Создает пользовательское сообщеное об ошибках вместо стандартных ошибок JavaScript
* ```finally``` — Позволяет выполнить код после try/catch, независимо от результата

## Значение ошибок
JavaScript также имеет встроенный инструмент(объект) для выведения ошибки. У него есть два свойства:

* ```name``` — Устанавливает или возвращает имя ошибки
* ```message``` — Устанавливает или возвращает сообщение об ошибке строкой
Свойство error может возвращать шесть разных значений в качестве своего имени:

* ```EvalError``` — в функции ```eval()``` произошла ошибка
* ```RangeError``` — Значение выходит за диапазон допустимых значений(или не входит во множество)
* ```ReferenceError``` — Обращении к несуществующей переменной
* ```SyntaxError``` — Синтаксически неправильный код
* ```TypeError``` — Значение имеет не ожидаемый тип
* ```URIError``` — Неправильное использование глобальных функций обработки URI

# Вкратце об шпаргалке JavaScript
В последние годы JavaScript приобрел большую популярность как язык программирования. Все большее число людей используют его для создания как относительно простых веб-страниц до монструозных приложений. Все это благодаря объемному послужному списку и большому числу преимуществ.

В приведенной выше шпаргалке, мы собрали множество самых основных и важных операторов, функций, принципов и методов. Она предоставляет хороший обзор языка и справку для опытных и начинающих разработчиков. Мы надеемся, что вы смогли использовать в полной мере данный материал.
