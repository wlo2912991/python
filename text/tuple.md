# tuple
```
tuple是一種與 list相似的資料結構
但tuple不能被修改

x = [11, 22, 33,44,55]   
這是list型態

x = (11, 22, 33,44,55)
這是tuple型態
```
## ()內相加
```
x = [8+9]
x會是[17]

那如果是
x = (8+9)
x會是什麼
```

## 自動打包/解包
```
tuple可以一次指定多個變數
(one, two, three, four) =  (1, 2, 3, 4)
一行程式碼就可以取代多行程式碼
```
```
>>> (one, two, three, four) =  (1, 2, 3, 4)
>>> one
1
>>> two
2


one, two, three, four = 1, 2, 3, 4
```
#### 交換數值
```
C 要交換數值需要三行代碼
temp = var1;
var1 = var2;
var2 = temp;

python只需要
var1,var2 = var2,var1
```
## list與tuple的轉換
```
list()可以將tuple轉為list
tuple()可以轉list為tuple
```
# 題目
```
將
x = (3,1,4,2)
進行排序
```


