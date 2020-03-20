### 1.使用Python內建的array()建立陣列
```
import numpy as np
ar2=np.array([[0,3,5],[2,8,7]])
ar2.shape # 顯示出是幾x幾的陣列
ar2.ndim  # 顯示出是幾維陣列

> 2
```
### 2.使用numpy提供的創建函數建立陣列
```
import numpy as np
ar=np.array([2,4,6,8]); 
ar.dtype  #顯示出是甚麼類型   int64是整數

> dtype('int64')
```
```
import numpy as np
f_ar = np.array([13,-3,8.88])
f_ar

intf_ar=f_ar.astype(int)   #轉換類型成為整數
intf_ar

> array([13, -3,  8])
```
```
import numpy as np
x = np.array([[1,2.0],[0,0],(1+1j,3.)])  # 複數陣列
x

> array([[1.+0.j, 2.+0.j],
        [0.+0.j, 0.+0.j],
        [1.+1.j, 3.+0.j]])
```
##### eye
```
import numpy as np
ar9 = np.eye(3);  #製造一個幾層的單位矩陣
ar9

>  array([[1., 0., 0.],
         [0., 1., 0.],
         [0., 0., 1.]])
```
##### zeros
```
import numpy as np
np.zeros((2, 3))  #製造一個零的幾乘幾矩陣

> array([[0., 0., 0.],
        [0., 0., 0.]])
```
##### ones
```
import numpy as np
np.ones((4, 7))  #製造一個全部為1的幾乘幾矩陣
 
> array([[1., 1., 1., 1., 1., 1., 1.],
         [1., 1., 1., 1., 1., 1., 1.],
         [1., 1., 1., 1., 1., 1., 1.],
         [1., 1., 1., 1., 1., 1., 1.]])
```
##### arange
```
import numpy as np
np.arange(2, 3, 0.1) # 從2開始, 3結束, 每次增加0.1
 
> array([2. , 2.1, 2.2, 2.3, 2.4, 2.5, 2.6, 2.7, 2.8, 2.9])
```
##### linspace
```
import numpy as np
np.linspace(1., 4., 6) # 從1.開始 到4.結束 每次加0.6

> array([1. , 1.6, 2.2, 2.8, 3.4, 4. ])
```
```
import numpy as np
np.linspace(2.0, 3.0, num=5)  從2.0開始 到3.0結束 5個數字的等差數列

> array([2.  , 2.25, 2.5 , 2.75, 3.  ])
```
```
import numpy as np
np.linspace(2.0, 3.0, num=5, endpoint=False) 從2.0開始 到3.0結束 5個數字的等差數列 不包含結束的數字
 
> array([2. , 2.2, 2.4, 2.6, 2.8])
```
```
import numpy as np
np.linspace(2.0, 3.0, num=5, retstep=True)  從2.0開始 到3.0結束 5個數字的等差數列  retstep代表打出差是多少
 
> (array([2.  , 2.25, 2.5 , 2.75, 3.  ]), 0.25)
```
##### indices
```
import numpy as np
np.indices((3, 3))  #製造幾乘幾的陣列 並且填上第幾維的數字

> array([[[0, 0, 0],
          [1, 1, 1],
          [2, 2, 2]],
         [[0, 1, 2],
          [0, 1, 2],
          [0, 1, 2]]])
```
##### tile
```
import numpy as np
a = np.array([0, 1, 2])
np.tile(a, 2)     #將某個陣列複製幾次

> array([0, 1, 2, 0, 1, 2])
```
```
import numpy as np
a = np.array([0, 1, 2])
np.tile(a, (2, 2))   #將某個陣列複製成幾乘幾的陣列

> array([[0, 1, 2, 0, 1, 2],
         [0, 1, 2, 0, 1, 2]])
```
```
import numpy as np
a = np.array([0, 1, 2])
np.tile(a, (2, 1, 2))   #將某個陣列複製成幾乘幾的陣列

>  array([[[0, 1, 2, 0, 1, 2]],

          [[0, 1, 2, 0, 1, 2]]])
```
### 3.直接生成使用genfromtxt()方法建立陣列

```
import csv
import numpy as np

x = '''1,3,2,3,1,2,3,4
2,4,5,0.6,5,6,7,8
3,7,8,9,9,10,11,12
4,1,1.1,1.2,13,14,15,16

with open("abc.txt",mode="w",encoding="utf-8") as file:
  file.write(x)
file.close()

np.genfromtxt('abc.txt', delimiter=',', invalid_raise = False)  #從文字檔中讀取訊息

>  array([[ 1. ,  3. ,  2. ,  3. ,  1. ,  2. ,  3. ,  4. ],
         [ 2. ,  4. ,  5. ,  0.6,  5. ,  6. ,  7. ,  8. ],
         [ 3. ,  7. ,  8. ,  9. ,  9. , 10. , 11. , 12. ],
         [ 4. ,  1. ,  1.1,  1.2, 13. , 14. , 15. , 16. ]])
```
##### tile
```
import numpy as np
np.tile(np.array([[1,2],[6,7]]),3)  #將陣列放大成三倍

> array([[1, 2, 1, 2, 1, 2],
         [6, 7, 6, 7, 6, 7]])
```
```
import numpy as np
np.tile(np.array([[1,2],[6,7]]),(2,2))  #將陣列放大成2x2的

> array([[1, 2, 1, 2],
         [6, 7, 6, 7],
         [1, 2, 1, 2],
         [6, 7, 6, 7]])

```
```
import numpy as np
np.array([range(i, i + 3) for i in [2, 4, 6]])

> array([[2, 3, 4],
         [4, 5, 6],
         [6, 7, 8]])
```
##### arange
```
import numpy as np
x = np.arange(2,10).reshape(2,4) #做出一個2~10的陣列 再分成2x4的陣列
x

>  array([[2, 3, 4, 5],
         [6, 7, 8, 9]])
```
```
import numpy as np
y = np.arange(2,10).reshape(4,2)  #做出一個2~10的陣列 再分成4x2的陣列
y

>  array([[2, 3],
          [4, 5],
          [6, 7],
          [8, 9]])
```
```
import numpy as np
ar=np.array([np.arange(1,6),np.arange(10,15)]);  #在陣列裡面 做出一個1~6的陣列跟一個10~15的陣列
ar

>  array([[ 1,  2,  3,  4,  5],
         [10, 11, 12, 13, 14]])
```
##### ravel
```
import numpy as np
ar=np.array([np.arange(1,6),np.arange(10,15)]) #在陣列裡面 做出一個1~6的陣列跟一個10~15的陣列
ar.ravel()          #將陣列變成一維陣列

> array([ 1,  2,  3,  4,  5, 10, 11, 12, 13, 14])
```
##### T
```
import numpy as np
ar=np.array([np.arange(1,6),np.arange(10,15)])  #在陣列裡面 做出一個1~6的陣列跟一個10~15的陣列
ar.T  #將陣列反轉

>   array([[ 1, 10],
           [ 2, 11],
           [ 3, 12],
           [ 4, 13],
           [ 5, 14]])
```
```
import numpy as np
ar=np.array([np.arange(1,6),np.arange(10,15)])  #在陣列裡面 做出一個1~6的陣列跟一個10~15的陣列
ar.T.ravel()         #將陣列反轉後拆開成一維陣列

>  array([ 1, 10,  2, 11,  3, 12,  4, 13,  5, 14])
```
##### newaxis
```
import numpy as np
ar=np.array([14,15,16])
ar=ar[:, np.newaxis]  #轉換陣列方向
ar.shape

>  (3, 1)
```
