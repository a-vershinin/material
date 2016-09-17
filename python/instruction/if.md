# Условные конструкции
Стандартное оформление условия
```python
  if условие:
    операции
# Так же можно оформлять с круглыми скобками
  if (условие):
    операции
```
Но оформление с круглыми скобками не приветствуются

Оператор множественных условий elif
```python
  x = 2
  if x == 1:
    print('x = 1')
  elif x == 2:
    print('x = 2')
  elif x == 3:
    print('x = 3')
```
Тк в python отсутствует оператор switch, то следует использовать elif и в этом нет ничего плохого.

Оператор else при ложности условий
```python
  x = 3
  if x == 1:
    print('x = 1')
  elif x == 2:
    print('x = 2')
  else:
    print('x = 3')
```

## Тернарный оператор или Трехместное выражение if/else
Оформляется довольно просто
```python
  (операция) if (условие) else (операция при ложном условии)

  x = 1
  print('x = 1') if x == 1 else print ('x != 1')
```