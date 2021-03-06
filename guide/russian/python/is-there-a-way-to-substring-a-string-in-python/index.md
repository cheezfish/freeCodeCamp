---
title: Is There a Way to Substring a String in Python
localeTitle: Есть ли способ подстроить строку в Python
---
## Есть ли способ подстроить строку в Python

Python предлагает множество способов подстроки строки. Его часто называют «срезанием».

Он следует этому шаблону:

```python
string[start: end: step] 
```

Куда,

`start` : начальный индекс подстроки. Символ в этом индексе включен в подстроку. Если _старт_ не включен, предполагается, что он равен 0.

`end` : `end` индекс подстроки. Символ в этом индексе _НЕ_ входит в подстроку. Если _конец_ не включен или если указанное значение превышает длину строки, оно считается равным длине строки по умолчанию.

`step` : Каждый символ «step» после текущего символа, который будет включен. Значение по умолчанию равно 1. Если значение _шага_ опущено, предполагается, что оно равно 1.

#### шаблон

`string[start:end]` : получить все символы от _начала_ индекса до _конца-1_

`string[:end]` : получить все символы от начала строки до _конца-1_

`string[start:]` : получить все символы от _начала_ индекса до конца строки

`string[start:end:step]` : получить все символы от _начала_ до _конца-1,_ уклоняясь от каждого _шага_

#### Примеры

*   **Получить первые 5 символов строки**

```python
string = "freeCodeCamp" 
 print(string[0:5]) 
```

Вывод:

```shell
> freeC 
```

Примечание: `print(string[:5])` возвращает тот же результат, что и `print(string[0:5])`

*   **Получить подстроку длиной 4 от третьего символа строки**

```python
string = "freeCodeCamp" 
 print(string[2:6]) 
```

Вывод:

```shell
> eeCo 
```

Обратите внимание, что начальный или конечный индекс может быть отрицательным числом. Отрицательный индекс означает, что вы начинаете отсчет с конца строки вместо начала (т. Е. Справа налево). Индекс -1 представляет собой последний символ строки, -2 - второй и последний символы и т. Д. ...

*   **Получить последний символ строки**

```python
string = "freeCodeCamp" 
 print(string[-1]) 
```

Вывод:

```shell
> p 
```

*   **Получить последние 5 символов строки**

```python
string = "freeCodeCamp" 
 print(string[-5:]) 
```

Вывод:

```shell
> eCamp 
```

*   **Получить подстроку, содержащую все символы, кроме последних 4 символов, и 1-й символ**

```python
string = "freeCodeCamp" 
 print(string[1:-4]) 
```

Вывод:

```shell
> reeCode 
```

#### Дополнительные примеры

```py
str = “freeCodeCamp” 
 
 print str[-5:-2] # prints 'eCa' 
 print str[-1:-2] # prints '' (empty string) 
```

*   **Получить любой другой символ из строки**

```python
string = "freeCodeCamp" 
 print(string[::2]) 
```

Вывод:

```shell
> feCdCm 

```