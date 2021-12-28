### Решения различных типов задания 22

#### Тип 1.1

> Ниже на пяти язы­ках за­пи­сан ал­го­ритм. По­лу­чив на вход число **x**, этот ал­го­ритм пе­ча­та­ет два числа: **a** и **b**. Ука­жи­те *наи­мень­шее* из таких чисел x, при вводе ко­то­ро­го ал­го­ритм пе­ча­та­ет сна­ча­ла **P**, а потом **Q**.

```python
for i in range(-10000, 10000):
	x = i
	
	# здесь расположите код
	
	if a == P and b == Q:
		print(i)
		break
```


#### Тип 1.2

> Ниже на пяти язы­ках за­пи­сан ал­го­ритм. По­лу­чив на вход число **x**, этот ал­го­ритм пе­ча­та­ет два числа: **a** и **b**. Ука­жи­те *наибольшее* из таких чисел x, при вводе ко­то­ро­го ал­го­ритм пе­ча­та­ет сна­ча­ла **P**, а потом **Q**.

```python
xmax = 0
for i in range(-10000, 10000):
	x = i
	
	# здесь расположите код
	
	if a == P and b == Q:
		xmax = i

print(xmax)
```