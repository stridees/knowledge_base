# Генератор списков (List comprehension)

## Создание списка без использования List comprehension

Представьте, что Вам необходимо создать список, содержащий 8 случайных чисел от 1 до 100 каждое.

_Пример 1_
```
[13, 25, 8, 78, 16, 67, 1, 99]
```
_Пример 2_
```
[3, 28, 33, 100, 90, 16, 85, 48]
```

Ниже представлен вариант решения данной задачи:
```python
from random import randint

numbers = []
for i in range(8):    
    numbers.append(randint(1, 100))
```

Рассмотрим представленный код построчно.

**1.** Импортируем функцию `randint` из модуля `random`: 
```python
from random import randint
```
Эта функция необходима для генерации случайных чисел, она не является встроенной (в отличие от `print()`, `len()` и т.д.), её нужно импортировать. Модуль `random` входит в стандартную библиотеку Питона, его не требуется устанавливать дополнительно.

**2.** Создаем пустой список и присваиваем его переменной `numbers`
```python
numbers = []
```
В этот список будут помещаться генерируемые случайные числа

**3.** Рассмотрим пошагово код для добавления в список `numbers` 8 случайных чисел:

```python
for i in range(8):    
    numbers.append(randint(1, 100))
```
  3.1. Чтобы сгенерировать случайное число от 1 до 100, вызываем функцию `randint`:

```python
randint(1, 100)
```
  3.2. Получившийся результат добавляем в список `numbers`, используя метод `.append()`:

```python
numbers.append(randint(1, 100))
```
  3.3. Повторяем эту операцию 8 раз (цикл `for`, в котором тело цикла выполняется для каждого элемента диапазона `range`):

```python
for i in range(8):    
    numbers.append(randint(1, 100))
```

## Создание списка с использованием List comprehension

Python позволяет реализовать рассмотренную выше задачу в одну строку (не считая строки импорта):

```python 
from random import randint

numbers = [randint(1, 100) for i in range(1, 100)]
```