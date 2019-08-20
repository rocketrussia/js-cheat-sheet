# Синтаксис регулярных выражений
Извините, но перевод будет чуть позже

Regular expressions are search patterns used to match character combinations in strings. The search pattern can be used for text search and text replace operations.

## Модификаторы
* e — Evaluate replacement
* i — Perform case-insensitive matching
* g — Perform global matching
* m — Perform multiple line matching
* s — Treat strings as a single line
* x — Allow comments and whitespace in the pattern
* U — Ungreedy pattern

## Скобки
* [abc] — Find any of the characters between the brackets
* [^abc] — Find any character which are not in the brackets
* [0-9] — Used to find any digit from 0 to 9
* [A-z] — Find any character from uppercase A to lowercase z
* (a|b|c) — Find any of the alternatives separated with |

## Метасимволы
* . — Find a single character, except newline or line terminator
* \w — Word character
* \W — Non-word character
* \d — A digit
* \D — A non-digit character
* \s — Whitespace character
* \S — Non-whitespace character
* \b — Find a match at the beginning/end of a word
* \B — A match not at the beginning/end of a word
* \0 — NUL character
* \n — A new line character
* \f — Form feed character
* \r — Carriage return character
* \t — Tab character
* \v — Vertical tab character
* \xxx — The character specified by an octal number xxx
* \xdd — Character specified by a hexadecimal number dd
* \uxxxx — The Unicode character specified by a hexadecimal number xxxx

## Квантификаторы
* n+ — Matches any string that contains at least one n
* n* — Any string that contains zero or more occurrences of n
* n? — A string that contains zero or one occurrence of n
* n{X} — String that contains a sequence of X n’s
* n{X,Y} — Strings that contain a sequence of X to Y n’s
* n{X,} — Matches any string that contains a sequence of at least X n’s
* n$ — Any string with n at the end of it
* ^n — String with n at the beginning of it
* ?=n — Any string that is followed by a specific string n
* ?!n — String that is not followed by a specific string ni
