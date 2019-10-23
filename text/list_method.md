# method(方法)
```
pethon跟C都是以物件導向的語言

c有函數可以使用

pethon用的是methon(方法)
```
### 使用append()、extend()在list 添加元素
```
用append添加
如果是list添加到list裡面的話會完整不變的添加進去

而用extend()添加則會拆開再添加
```
```
>>> x = [1, 2, 3, 4]
>>> y = [5, 6, 7]
>>> x.append(y)  
>>> x
[1, 2, 3, 4, [5, 6, 7]]
```
```
>>> x = [1, 2, 3, 4]
>>> y = [5, 6, 7]
>>> x.extend(y)  
>>> x
[1, 2, 3, 4, 5, 6, 7] 
```
### insert
```
insert可以選擇在list哪裡添加元素
insert(位置,添加的元素)
```
```
>>> x = [1, 2, 3]
>>> x.insert(2, "hello")
>>> print(x)
[1, 2, 'hello', 3]
>>> x.insert(0, "start")
>>> print(x)
['start', 1, 2, 'hello', 3]
```
### Del、remove
```
del可以刪除list裡面的元素
del能刪除任何有名稱的物件
del(位置)

remove可以指定刪除哪個元素
remove(要刪除的元素)

```
```
>>> x = ['a', 2, 'c', 7, 9, 11]
>>> del x[1]
>>> x
['a', 'c', 7, 9, 11]
>>> del x[:2]
>>> x
[7, 9, 11]
```
```
>>> x = [1, 2, 3, 4, 3, 5]
>>> x.remove(3)
>>> x
[1, 2, 4, 3, 5]
>>> x.remove(3)
>>> x
[1, 2, 4, 5]
>>> x.remove(3)
Traceback (innermost last):
 File "<stdin>", line 1, in ?
ValueError: list.remove(x): x not in list
```
## 排序
#### 反轉整個序列
```
reverse()
這個mothod可以翻轉整個序列
```
```
>>> x = [1, 3, 5, 6, 7]
>>> x.reverse()
>>> x
[7, 6, 5, 3, 1]
```
## sort
```
sort可以依照大小排序序列 數字由小到大
如果sort排序的list是字串
那會比較第一個字母大小
```
```
>>> x = [2, 4, 1, 3]
>>> y = x[:]
>>> y.sort()
>>> y
[1, 2, 3, 4]
>>> x
[2, 4, 1, 3]
```
```
>>> x = ["Life", "Is", "Enchanting"]
>>> x.sort()
>>> x
['Enchanting', 'Is', 'Life']
```
# 題目
```
>>> x = [1, 2, 'hello', 3]
>>> x.sort()
這一段代碼會發生什麼
```
#### sortde
```
sortde跟sort差不多
可是sortde是傳一個新的排序好的list

如果要反向排序
()裡面添加reverse=True即可
```
>>> x = (4, 3, 1, 2)
>>> y = sorted(x)
>>> y
[1, 2, 3, 4] 
>>> z = sorted(x, reverse=True)
>>> z
[4, 3, 2, 1]
```
# in
```
in 可以用來測試某個序列裡面有沒有包括某個元素
如果有 回傳true
如果無 回傳false
```
```
>>> 3 in [1, 3, 4, 5]
True
>>> 3 not in [1, 3, 4, 5]
False
>>> 3 in ["one", "two", "three"]
False
>>> 3 not in ["one", "two", "three"]
True
```
##  + 、 *
```
+算符可以把兩個list串起
跟extend一樣會拆開

*算符會將元素變成四個
list數量不變
```
```
>>> z = [1, 2, 3] + [4, 5]
>>> z
[1, 2, 3, 4, 5]
```
```
>>> z = [None] * 4
>>> z
[None, None, None, None]
```
