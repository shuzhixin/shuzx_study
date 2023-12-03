https://tzcoder.cn/acmhome/problemdetail.do?method=showdetail&id=7345



要表示n种不同的信息，需要的二进制位数至少为多少。





输入条件：

输入为一整数，表示要表示的信息种数$(1<=n<=10^6)$。

1个整数：

数据类型：

1. 字符  ‘a'   (1Byte)
2. 整型  2     (2Byte)
3. 浮点型  2.000 (4Byte)
4. 实数   2.00000
5. 字符串 'abcd'， "abcd"
6. 

1 Byte = 8 bits

笔记本硬盘：

X86-64   Intel + AMD

1TB= 1024GB = 1024 * 1024 MB = 1024 * 1024 *1024KB = 1024 * 1024 * 1024 * 1024 B



CPU: ARM





计算机CPU的发展：

4位机（max integer） == $2^4$ - 1 = 15

CPU -- 8086 :8位机= 1Byte (max integer) == $2^8$ - 1 = 255

16位机(max integer) == $2^{16}$ - 1 = 65535 

32位机(max integer) ==$2^{32} -1$ = 4294967296 - 1 = 4, 294, 967, 295 = $4.29 * 10^9$

CPU: I7  64位机(max integer) == $ 2^{64} - 1 $ = $1.8446744073709552* 10^{19} - 1$





解题：

1. 1  -- （0）  0                                    $ 2^0 = 1$
2. 2 --   （0，1） 0, 1                          $ 2^1 = 2$
3. 3 -- (0, 1, 2)    00, 01, 10                  $ 2^1 + 1 = 3$
4. 4 -- （0，1,2,3） 00, 01, 10, 11    $ 2^2 = 4 $
5. 5                                                        $ 2^2 + 1 = 5$
6. 6                                                         $ 2^2 + 2 = 5 $
7. 7                                                         $ 2^2 + 3 = 7 $ 
8. 8 -- (0, 1, 2, 3, 4, 5, 6, 7)   000, 001, 010, 011, 100, 101, 110, 111   $ 2^3 = 8 $
9. 9 - 



import math

$ y = a^ x $ ==> $ x = log_{a} {y} $

math.log(1, 2)

1  ==  math.log(1, 2)     0               1

2 == math.log(2, 2)      1                1

3 == math.log(3, 2)     > 1              2

4 == math.log(4, 2)    = 2               2

5 == math.log(5, 2)  > 2                3

8 == math.log(8, 2)   = 3               3

9 == math.log(9, 2)   > 3               4



100                                                  7

通用公式：

输入：n       

位数：math.log(n, 2)  向上取整

math.ceil( math.log(n, 2))



![image-20231118205417954](/Users/shuzx/Library/Application Support/typora-user-images/image-20231118205417954.png)



if n == 1:

​     bits = 1

else 

​    bits = math.ceil( math.log(n, 2) )    



```python
import math
n=int(input())
bits = 0
if n == 1:
    bits = 1
else:
    bits = math.ceil( math.log(n , 2) )
print(bits)

```

