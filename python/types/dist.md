# Словари
Словари в Python - неупорядоченные коллекции произвольных объектов с доступом по ключу. Их иногда ещё называют ассоциативными массивами или хеш-таблицами. Создать словарь можно несколькими способами, через функцию `dict(arg1=value, arg2=value)`.
```python
d = dict(short='dict', long='dictionary')
#{'short': 'dict', 'long': 'dictionary'}
```
или через литерал
```python
d = {'dict': 1, 'dictionary': 2}
#{'dict': 1, 'dictionary': 2}
```
или через генератор словаря, который очень похож на генератор списка.
```python
d = {a: a ** 2 for a in range(7)}
#{0: 0, 1: 1, 2: 4, 3: 9, 4: 16, 5: 25, 6: 36}
```

Извлечение из словаря
```python
d = {'dict': 1, 'dictionary': 2}
d['dict'] # -> Обращение к элементу словаря
d['dict_ru': 'Словарь'] # -> Элементы словаря могут быть различных типов, плюс здесь продемонстрирован способ добавления нового элемента в словарь
d['dict_en'] # -> Обращение к несуществующему элементу вызывает ошибку. Для избежания исключения есть специальный метод (см. ниже)
>>> Traceback (most recent call last):
>>>   File "", line 3, in
>>>     d['dict_en']
>>> KeyError: 'dict_en'
```

### Методы словарей
|Метод                            |Что делает |
|:-------------------------------:|:---------:|
| dict.clear()                    |  очищает словарь. |
| dict.copy()                     | возвращает копию словаря. |
| dict.fromkeys(seq[, value])     | создает словарь с ключами из seq и значением value (по умолчанию None). |
| dict.get(key[, default])        | возвращает значение ключа, но если его нет, не бросает исключение, а возвращает default (по умолчанию None). |
| dict.items()                    | возвращает пары (ключ, значение). |
| dict.keys() | возвращает ключи в словаре. |
| dict.pop(key[, default])        | удаляет ключ и возвращает значение. Если ключа нет, возвращает default (по умолчанию бросает исключение). |
| dict.popitem()                  | удаляет и возвращает пару (ключ, значение). Если словарь пуст, бросает исключение KeyError. Помните, что словари неупорядочены. |
| dict.setdefault(key[, default]) | возвращает значение ключа, но если его нет, не бросает исключение, а создает ключ с значением default (по умолчанию None). |
| dict.update([other])            | обновляет словарь, добавляя пары (ключ, значение) из other. Существующие ключи перезаписываются. Возвращает None (не новый словарь!). |
| dict.values()                   | возвращает значения в словаре. |