# 第4章 絕對的基礎

### 4.1 縮排及區塊結構

```
/* 以下是 C 程式碼 */
int n,r;
n=9;
r=1;
while ( n > 0 ){
    r *= n;
    n--;
}
```

```
/* 以下是任意縮排的 C 程式碼*/
    int n,r;
       n=9;
       r=1;
   while ( n > 0 ){
r *= n;
n--;
}
```
```
# 這是 python 程式碼
n = 9
r = 1
while n > 0 :
    r = r * n  <-----Python 也支援類似 C 的語法 : r *= n
    n = n - 1  <-----Python 也支援類似 C 的語法 : n -= 1
```

```
for i in range(1 , 10):
    for j in range(1 , 10):
        print(f'{j}x{i}={j*i:2d}', end=' ')  <----這行屬於第二個迴圈
    print()  <------這行屬於第一個迴圈

```

```
    多了一個空格會出現 unexpected indent
>>> a=2
    File "<stdin>", line 1
        a=2
        ^
IndentationError: unexpcted indent
```
##### 但在 Iptython 環境下並不會發生錯誤

```
In[1]; a=2  <----- 前面多一個空格在 Iptython 不會出現錯誤訊息
```


### 4.2 註解
```
# 設定 x 變數的值為 5
x = 5
x = 3   # 現在 x 變數值等於 3
x = "# This is not a comment"  <-------此行的 # 只是字串中的一個字元
```

### 4.3 變數及其設定

``` 
x = 5
```

```
>>> x  = "Hello" <---建立字串物件 "Hello" ，　讓變數 x 參照到該物件
>>> print(x)
Hello

>>> x = 5   <--------建立整數物件 5 ，讓變數 x 參照到該物件
>>> x
5
```
```
>>> x = 5
>>>print(x)
5

>>> del x
>>> print(x)
Traceback (most recent call last):
    File "<stdin>", line 1, in <module>
NameError : name'x' is not defined
>>>
```
### 4.4 運算式
```
x = 3
y = 5
z = (x + y) / 2
```
```
>>> 3 / 2
1.5
>>> 3 // 2
1
>>> -1 // 2
-1     <--------------- -1 除以 2 等於 -0.5 ， 而小於 -0.5 的最大整數為 -1 。
                           注意!! 不是四捨五入喔!!
```
### 4.5 字串
```
x = "Hello, World"
```
```
x = "\t 這個字串開頭是一個 \"tab\" 字元."
x = "這個字串包含一個反斜線 (\\) 字元."
```
```
x = "Hello , world"
x = "Hello , world'
```
```
x = ' you can leave the " alone'
x = ' Don't need a backslash"
x = ' Can \'t get by without a backslash'
x = " Backslash your \" character!"
```
##### 不能將字串拆成多行 以下程式碼無法正常操作
```
x = This is a misguided attempt to
put a newline into a string without using backslash-n"
```

```
x = """Starting and ending a string with triple " characters permits embedded newlines , and the use of " and ' without backslashes"""
```

### 4.6 數字
```
>>> 5 + 2 - 3 * 2 
1

>>> 5 / 2  # 除法(/)運算結果為浮點數
2.5

>>> 5 / 2.0
2.5

>>> 5 // 2 # 使用(//)除法的結果是小於商數的最大整數
2

>>> 5.0  // 2 # 5.0是浮點數，所以運算結果變成浮點數
2.0

>>> 3000000000 # 很多程式語言中這個數值通常會超出整數型別的範圍
3000000000

>>> 3000000000 * 3 
9000000000

>>> 3000000000 *3.0  #3.0是浮點數 所以結果是浮點數
9000000000.0

>>> 2.0e-8 #用科學計數法表示一個浮點數
2e-08

>>> 3000000 * 3000000
9000000000000

>>> int( 200.2 )
200

>>> int()2e2
200

>>> float (200)
200.0

```
### 4.7 None值



### 4.8 取得使用者的輸入

### 4.9 內建算符

### 4.10 基本Python風格與名稱命名慣例


# 第5章 基本資料結構：list、tuple、set

### 5.1 list類似陣列

### 5.2 list的索引與切片

### 5.3 修改list

### 5.4 list的排序

### 5.5 其他常用的list操作

### 5.6 多層list和深層副本

### 5.7 tuple

### 5.8 set
