## Решения различных видов задания 12

### Исполнитель Редактор

* В ``replace()`` не забывайте указывать ``1`` третьим аргументом.

#### Тип 1
> Какая стро­ка по­лу­чит­ся в ре­зуль­та­те при­ме­не­ния при­ведённой ниже про­грам­мы к стро­ке, со­сто­я­щей из 68 иду­щих под­ряд цифр 8? В от­ве­те за­пи­ши­те по­лу­чен­ную стро­ку.
```
НА­ЧА­ЛО
ПОКА на­шлось (222) ИЛИ на­шлось (888)
    ЕСЛИ на­шлось (222)
        ТО за­ме­нить (222, 8)
    ИНАЧЕ за­ме­нить (888, 2)
    КОНЕЦ ЕСЛИ
КОНЕЦ ПОКА
КОНЕЦ
```

```python
s = '8' * 68

while ('222' in s) or ('888' in s):
	if ('222' in s):
		s = s.replace('222', '8', 1)
	else:
		s = s.replace('888', '2', 1)

print(s)
```

#### Тип 2
> Дана про­грам­ма для ре­дак­то­ра:

```
НА­ЧА­ЛО
    ПОКА НЕ на­шлось (00)
        за­ме­нить (01, 210)
        за­ме­нить (02, 320)
        за­ме­нить (03, 3012)
    КОНЕЦ ПОКА
КОНЕЦ
```

> Из­вест­но, что ис­ход­ная стро­ка на­чи­на­лась с нуля и за­кан­чи­ва­лась нулём, а между ними со­дер­жа­ла толь­ко еди­ни­цы, двой­ки и трой­ки. После вы­пол­не­ния дан­ной про­грам­мы по­лу­чи­лась стро­ка, со­дер­жа­щая 26 еди­ниц, 54 двой­ки и 48 троек. Сколь­ко цифр было в ис­ход­ной стро­ке?

```python
for x in range(100):
    for y in range(100):
        for z in range(100):
            s = '0' + ('1' * x) + ('2' * y) + ('3' * z) + '0'

            while s.count('00') == 0:
                s = s.replace('01', '210', 1)
                s = s.replace('02', '320', 1)
                s = s.replace('03', '3012', 1)
            
            if s.count('1') == 26 and s.count('2') == 54 and s.count('3') == 48:
                print(len(s))
                break
```
