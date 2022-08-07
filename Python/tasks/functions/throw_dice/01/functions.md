# Functions (функции)
Основные понятия:
* `Функция` (function) - подпрограмма (subroutine)
* `Объявить функцию` (define a function)
    * `Имя функции` (function's name)
    * `Параметры, аргументы` (parameters, arguments)
        * обязательные и необязательные  
        (required and optional)
        * позиционные и именованные  
        (positional and keyword)
    * `Тело функции` (function's body)
    * `Локальные переменные` (local variables)
    * `Возвращаемое значение` (return value)
* `Основная программа` (main program)
* `Глобальные переменные` (global variables)
* `Вызвать функцию` (call a function)

## Стандартная библиотека (Standard Python Library)
### Встроенные (built-in) функции
[Официальная документация](https://docs.python.org/3/library/functions.html)

Встроенные функции могут быть вызваны в любом месте программы, их не нужно импортировать (с помощью `import`)
* `print()`
* `input()`
* `len()`
* `min()`  
и т.д.
### Функции из модулей стандартной библиотеки
Для вызова этих функций не требуется установка дополнительных модулей (входят в "комплект поставки" Python), но в отличие от встроенных их необходимо импортировать
```python
# импорт функции sqrt (square root) из модуля 
# math стандартной библиотеки Python
from math import sqrt

# вычисление квадратного корня числа 9
print(sqrt(9))
```
```python
# импорт функции randint (random integer) 
# из модуля random стандартной библиотеки Python
from random import randint

# генерация случайного числа от 1 до 10
number = randint(1, 10)
print(number)
```
### Функции, объявляемые программистом (user defined functions)

```python
# объявление функции с 2-мя обязательными 
# позиционными параметрами (text и num)
def say_hello(text, num):
    for i in range(num):
        print(text)

# при вызове обязательно передать 2 аргумента
say_hello("Привет", 2)
```
