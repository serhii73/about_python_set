# About Python Set

```
In [1]: a = {'a', 'b', 'c'}

In [2]: a.add('d')

In [3]: a
Out[3]: {'a', 'b', 'c', 'd'}

In [4]: # add добавляет значение в множество

In [5]: a.clear()

In [6]: a
Out[6]: set()

In [7]: a = {'a', 'b', 'c'}

In [8]: b = a

In [9]: a.add('d')

In [10]: b
Out[10]: {'a', 'b', 'c', 'd'}

In [11]: c = a.copy()

In [12]: x = {1, 2, 3}

In [13]: y = {3, 4, 5}

In [14]: x.difference(y)
Out[14]: {1, 2}

In [15]: y.difference(x)
Out[15]: {4, 5}

In [16]: # difference - элементы сета, которых нет в другом сете

In [17]: x.difference_update(y)

In [18]: x
Out[18]: {1, 2}

In [19]: y
Out[19]: {3, 4, 5}

In [20]: z = {4, 5, 6}

In [21]: z.difference_update(y)

In [22]: z
Out[22]: {6}

In [23]: # difference_update обновляет сеты, показвает того, чего нет во втором 
    ...: сете и оставляет это

In [24]: x = {1, 2, 3}

In [25]: y = {3, 4, 5}

In [26]: z
Out[26]: {6}

In [27]: z.discard(5)

In [28]: z
Out[28]: {6}

In [29]: z.discard(6)

In [30]: z
Out[30]: set()

In [31]: # discard удаляет элемент, если он есть в множестве

In [32]: x
Out[32]: {1, 2, 3}

In [33]: z
Out[33]: set()

In [34]: y
Out[34]: {3, 4, 5}

In [35]: x.intersection(y)
Out[35]: {3}

In [36]: # intersection - показывает сет данных, общий для двух остальных

In [37]: x
Out[37]: {1, 2, 3}

In [38]: y
Out[38]: {3, 4, 5}

In [39]: x.intersection_update(y)

In [40]: z
Out[40]: set()

In [41]: x
Out[41]: {3}

In [42]: # intersection_update еще и обновляет множество

In [43]: x = {1, 2, 3}

In [44]: y
Out[44]: {3, 4, 5}

In [45]: x.isdisjoint(y)
Out[45]: False

In [46]: z = {6, 7, 8}

In [47]: x.isdisjoint(z)
Out[47]: True

In [48]: # isdisjoint - истина, если set и other не имеют общих элементов.

In [49]: x
Out[49]: {1, 2, 3}

In [50]: y
Out[50]: {3, 4, 5}

In [51]: x.issubset(y)
Out[51]: False

In [52]: z = {3,2,1}

In [53]: x.issubset(z)
Out[53]: True

In [54]: # issubset - все элементы set принадлежат other.

In [55]: x
Out[55]: {1, 2, 3}

In [56]: y
Out[56]: {3, 4, 5}

In [57]: x.issuperset(y)
Out[57]: False

In [58]: x.issuperset(z)
Out[58]: True

In [59]: # set >= other

In [60]: x
Out[60]: {1, 2, 3}

In [61]: x.pop()
Out[61]: 1

In [62]: x
Out[62]: {2, 3}

In [63]: # pop - удаляет первый элемент множества

In [64]: z
Out[64]: {1, 2, 3}

In [65]: z.remove(2)

In [66]: z
Out[66]: {1, 3}

In [67]: # remove - удаляет нужный элемент

In [68]: z.remove(2)
---------------------------------------------------------------------------
KeyError                                  Traceback (most recent call last)
<ipython-input-68-baeee67eb7b3> in <module>()
----> 1 z.remove(2)

KeyError: 2

In [69]: x = {1, 2, 3}

In [70]: y = {3, 4, 5}

In [71]: x.symmetric_difference(y)
Out[71]: {1, 2, 4, 5}

In [72]: # symmetric_difference собирает различия двух сетов в один сет

In [73]: x.symmetric_difference(y)
Out[73]: {1, 2, 4, 5}

...

In [75]: x
Out[75]: {1, 2, 3}

In [76]: y
Out[76]: {3, 4, 5}

In [77]: x.symmetric_difference_update(y)

In [78]: x
Out[78]: {1, 2, 4, 5}

In [79]: # тоже самое, только обновляет сет

In [80]: y
Out[80]: {3, 4, 5}

In [81]: x = {1, 2, 3}

In [82]: x.union(y)
Out[82]: {1, 2, 3, 4, 5}

In [83]: x + y
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-83-cd60f97aa77f> in <module>()
----> 1 x + y

TypeError: unsupported operand type(s) for +: 'set' and 'set'

In [84]: x += y
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-84-3fa90755daf3> in <module>()
----> 1 x += y

TypeError: unsupported operand type(s) for +=: 'set' and 'set'

In [85]: # union объединяет два сета в один

In [86]: x.union(y)
Out[86]: {1, 2, 3, 4, 5}

In [87]: x.update(y)

In [88]: x
Out[88]: {1, 2, 3, 4, 5}

In [89]: # update тот же union, только изменяет сет
```