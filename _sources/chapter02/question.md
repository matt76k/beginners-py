---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.5
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---
理解度チェック50
===========

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
x = [1, 2, 3]
y = x
y.append(4)
print(len(x))
```

A. 3  
B. 4  
C. エラーが発生する
````

````{dropdown} 解答
**正解：B. 4**

yとxは同じリストを指しているため、yにappendした要素がxにも反映されます。
````

````{exercise}

次のPythonコードの出力結果は何でしょうか？

```python
a = 15
b = 7
result = a // b
print(result)
```

A. 2  
B. 2.142857...  
C. 3
````

````{dropdown} 解答
**正解：A. 2**

`//`は整数除算演算子です。15を7で割った商の整数部分は2です。
````

````{exercise}

次のPythonコードの出力結果は何でしょうか？

```python
x = 20
if x > 25:
    print("A")
elif x > 15:
    print("B")
else:
    print("C")
```

A. A  
B. B  
C. C
````

````{dropdown} 解答
**正解：B. B**

x = 20は25より小さいので最初の条件は偽、15より大きいので2番目の条件が真となり、"B"が出力されます。
````

````{exercise}

次のPythonコードの出力結果は何でしょうか？

```python
count = 0
for i in range(3):
    count += i
print(count)
```

A. 0  
B. 3  
C. 2
````

````{dropdown} 解答
**正解：B. 3**

range(3)は0, 1, 2を生成し、count = 0 + 1 + 2 = 3となります。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
numbers = [10, 20, 30]
numbers[1] = 99
print(numbers[0] + numbers[2])
```

A. 40  
B. 129  
C. 139
````

````{dropdown} 解答
**正解：A. 40**

numbers[1]を変更しても、numbers[0]とnumbers[2]は変わらないため、10 + 30 = 40です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
x = 12
y = 5
print(x % y)
```

A. 2  
B. 3  
C. 7
````

````{dropdown} 解答
**正解：A. 2**

12を5で割った余りは2です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
data = [1, 2, 3, 4, 5]
result = data[1:4]
print(len(result))
```

A. 2  
B. 3  
C. 4
````

````{dropdown} 解答
**正解：B. 3**

data[1:4]は[2, 3, 4]を取得し、その長さは3です。
````

````{exercise}

次のPythonコードの出力結果は何でしょうか？

```python
total = 0
i = 1
while i <= 4:
    total += i
    i += 2
print(total)
```

A. 4  
B. 6  
C. 10
````

````{dropdown} 解答
**正解：A. 4**

i=1でtotal=1、i=3でtotal=4、i=5で条件を満たさず終了。結果は4です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
nums = [5, 10, 15, 20]
nums.pop()
nums.append(25)
print(nums[-1])
```

A. 20  
B. 25  
C. 15
````

````{dropdown} 解答
**正解：B. 25**

pop()で20を削除、append(25)で25を追加。nums[-1]は最後の要素25です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
x = 8
if x > 10 or x < 5:
    print("Yes")
else:
    print("No")
```

A. Yes  
B. No  
C. エラーが発生する
````

````{dropdown} 解答
**正解：B. No**

x=8は10より小さく、かつ5以上なので、条件(x > 10 or x < 5)は偽となり"No"が出力されます。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
values = [2, 4, 6, 8]
sum_val = 0
for v in values:
    if v > 5:
        sum_val += v
print(sum_val)
```

A. 14  
B. 20  
C. 6
````

````{dropdown} 解答
**正解：A. 14**

5より大きい値は6と8なので、6 + 8 = 14です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
a = [1, 2, 3]
b = [4, 5]
c = a + b
print(c[3])
```

A. 4  
B. 5  
C. エラーが発生する
````

````{dropdown} 解答
**正解：A. 4**

a + bは[1, 2, 3, 4, 5]となり、c[3]は4です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
num = 17
if num % 2 == 1 and num > 10:
    print("A")
elif num % 2 == 0:
    print("B")
else:
    print("C")
```

A. A  
B. B  
C. C
````

````{dropdown} 解答
**正解：A. A**

17は奇数(17%2==1)かつ10より大きいので、最初の条件が真となり"A"が出力されます。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
items = [10, 20, 30, 40]
items.insert(2, 99)
print(items[3])
```

A. 30  
B. 40  
C. 99
````

````{dropdown} 解答
**正解：A. 30**

insert(2, 99)でインデックス2に99を挿入。リストは[10, 20, 99, 30, 40]となり、items[3]は30です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
x = 0
for i in range(5):
    if i == 2:
        continue
    x += i
print(x)
```

A. 6  
B. 8  
C. 10
````

````{dropdown} 解答
**正解：B. 8**

i=2のときcontinueでスキップされるため、0+1+3+4=8です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
data = [1, 2, 3, 4, 5]
new_data = data[:3]
new_data[0] = 99
print(data[0])
```

A. 1  
B. 99  
C. エラーが発生する
````

````{dropdown} 解答
**正解：A. 1**

data[:3]はスライスによる新しいリストの作成なので、new_dataの変更はdataに影響しません。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
counter = 0
for i in range(10):
    if i % 3 == 0:
        counter += 1
print(counter)
```

A. 3  
B. 4  
C. 5
````

````{dropdown} 解答
**正解：B. 4**

0から9の中で3の倍数は0, 3, 6, 9の4個です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
numbers = [5, 2, 8, 1]
max_num = numbers[0]
for num in numbers[1:]:
    if num > max_num:
        max_num = num
print(max_num)
```

A. 5  
B. 8  
C. 1
````

````{dropdown} 解答
**正解：B. 8**

リストの中で最大値を求めるアルゴリズムで、最大値8が見つかります。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
result = []
for i in range(4):
    result.append(i * 2)
print(result[2])
```

A. 2  
B. 4  
C. 6
````

````{dropdown} 解答
**正解：B. 4**

resultは[0, 2, 4, 6]となり、result[2]は4です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
x = 30
y = x // 7
z = x % 7
print(y + z)
```

A. 6  
B. 7  
C. 5
````

````{dropdown} 解答
**正解：A. 6**

30 // 7 = 4, 30 % 7 = 2なので、4+2=6です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
values = [3, 1, 4, 1, 5]
count = 0
for v in values:
    if v <= 3:
        count += 1
print(count)
```

A. 2  
B. 3  
C. 4
````

````{dropdown} 解答
**正解：B. 3**

3以下の値は3, 1, 1の3個です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
nums = [10, 20, 30]
nums.reverse()
print(nums[0])
```

A. 10  
B. 20  
C. 30
````

````{dropdown} 解答
**正解：C. 30**

reverse()でリストが[30, 20, 10]となり、nums[0]は30です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
total = 0
for i in range(1, 6):
    if i % 2 == 0:
        total += i
    else:
        total -= i
print(total)
```

A. -3  
B. 3  
C. -9
````

````{dropdown} 解答
**正解：A. -3**

-1+2-3+4-5 = -3です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
data = [2, 4, 6, 8, 10]
index = 0
while index < len(data) and data[index] < 7:
    index += 1
print(index)
```

A. 2  
B. 3  
C. 4
````

````{dropdown} 解答
**正解：B. 3**

7未満の要素は2, 4, 6で、その次のインデックスは3です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
matrix = [[1, 2], [3, 4], [5, 6]]
print(matrix[1][0])
```

A. 2  
B. 3  
C. 4
````

````{dropdown} 解答
**正解：B. 3**

matrix[1]は[3, 4]で、その0番目の要素は3です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
x = 45
if x > 50:
    result = "High"
elif x > 30:
    result = "Medium"
elif x > 10:
    result = "Low"
else:
    result = "Very Low"
print(result)
```

A. High  
B. Medium  
C. Low
````

````{dropdown} 解答
**正解：B. Medium**

x=45は50以下だが30より大きいので、"Medium"になります。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
arr = [1, 3, 5, 7, 9]
sum_even_indices = 0
for i in range(len(arr)):
    if i % 2 == 0:
        sum_even_indices += arr[i]
print(sum_even_indices)
```

A. 15  
B. 25  
C. 9
````

````{dropdown} 解答
**正解：A. 15**

偶数インデックス（0, 2, 4）の要素は1, 5, 9で、1 + 5 + 9 = 15です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
numbers = [8, 3, 12, 7]
numbers.sort()
print(numbers[1])
```

A. 3  
B. 7  
C. 8
````

````{dropdown} 解答
**正解：B. 7**

ソート後は[3, 7, 8, 12]となり、numbers[1]は7です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
product = 1
for i in range(1, 5):
    product *= i
print(product)
```

A. 10  
B. 24  
C. 120
````

````{dropdown} 解答
**正解：B. 24**

1×2×3×4 = 24です（4の階乗）。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
items = [5, 10, 15, 20, 25]
filtered = []
for item in items:
    if item > 10 and item < 25:
        filtered.append(item)
print(len(filtered))
```

A. 1  
B. 2  
C. 3
````

````{dropdown} 解答
**正解：B. 2**

10より大きく25未満の要素は15と20の2個です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
a = 16
b = 3
print(a ** b)
```

A. 48  
B. 4096  
C. 64
````

````{dropdown} 解答
**正解：B. 4096**

16の3乗は16×16×16 = 4096です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
data = [2, 4, 6, 8]
for i, value in enumerate(data):
    if i == 2:
        break
print(i)
```

A. 1  
B. 2  
C. 6
````

````{dropdown} 解答
**正解：B. 2**

i=2でbreakされるため、iの値は2です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
nums = [1, 2, 3, 4, 5]
total = 0
for num in nums[:3]:
    total += num ** 2
print(total)
```

A. 14  
B. 55  
C. 30
````

````{dropdown} 解答
**正解：A. 14**

最初の3要素の2乗の合計：$1^2 + 2^2 + 3^2 = 1 + 4 + 9 = 14$です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
x = 18
result = 0
while x > 0:
    result += x % 10
    x //= 10
print(result)
```

A. 9  
B. 18  
C. 1
````

````{dropdown} 解答
**正解：A. 9**

18の各桁の合計：1 + 8 = 9です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
scores = [85, 92, 78, 96, 88]
above_90 = 0
for score in scores:
    if score >= 90:
        above_90 += 1
print(above_90)
```

A. 2  
B. 3  
C. 4
````

````{dropdown} 解答
**正解：A. 2**

90以上のスコアは92と96の2個です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
values = [3, 7, 2, 9, 1, 8]
min_val = values[0]
for val in values:
    if val < min_val:
        min_val = val
print(min_val)
```

A. 1  
B. 2  
C. 3
````

````{dropdown} 解答
**正解：A. 1**

リストの最小値は1です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
n = 5
triangle = []
for i in range(n):
    triangle.append(i + 1)
print(triangle[3])
```

A. 3  
B. 4  
C. 5
````

````{dropdown} 解答
**正解：B. 4**

triangleは[1, 2, 3, 4, 5]となり、triangle[3]は4です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
lst = [10, 20, 30, 40, 50]
del lst[2]
print(lst[2])
```

A. 30  
B. 40  
C. 50
````

````{dropdown} 解答
**正解：B. 40**

インデックス2の要素30を削除後、lstは[10, 20, 40, 50]となり、lst[2]は40です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
count = 0
for i in range(20):
    if i % 4 == 0 and i > 0:
        count += 1
print(count)
```

A. 4  
B. 5  
C. 6
````

````{dropdown} 解答
**正解：A. 4**

0より大きい4の倍数は4, 8, 12, 16の4個です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
grid = [[1, 2, 3], [4, 5, 6]]
total = 0
for row in grid:
    for cell in row:
        total += cell
print(total)
```

A. 15  
B. 21  
C. 6
````

````{dropdown} 解答
**正解：B. 21**

すべての要素の合計：$1 + 2 + 3 + 4 + 5 + 6 = 21$です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
x = 25
y = 4
print(x // y, x % y)
```

A. 6 1  
B. 6.25 0  
C. 6 1
````

````{dropdown} 解答
**正解：A. 6 1**

25//4=6, 25%4=1なので、出力は「6 1」です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
numbers = [2, 5, 8, 11, 14]
result = []
for i in range(0, len(numbers), 2):
    result.append(numbers[i])
print(result)
```

A. [2, 8, 14]  
B. [5, 11]  
C. [2, 5, 8]
````

````{dropdown} 解答
**正解：A. [2, 8, 14]**

range(0, 5, 2)は0, 2, 4を生成し、対応する要素は2, 8, 14です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
temp = 0
values = [1, 3, 5, 7]
for v in values:
    temp = temp * 2 + v
print(temp)
```

A. 16  
B. 46  
C. 37
````

````{dropdown} 解答
**正解：C. 37**

temp = ((((0*2+1)*2+3)*2+5)*2+7) = ((1*2+3)*2+5)*2+7 = (5*2+5)*2+7 = 15*2+7 = 37です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
words = ["apple", "banana", "cherry"]
count = 0
for word in words:
    if len(word) > 5:
        count += 1
print(count)
```

A. 1  
B. 2  
C. 3
````

````{dropdown} 解答
**正解：B. 2**

文字数が5より多いのは"banana"(6文字)と"cherry"(6文字)の2個です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
arr = [8, 3, 6, 1, 4]
target = 5
closest = arr[0]
for num in arr:
    if abs(num - target) < abs(closest - target):
        closest = num
print(closest)
```

A. 3  
B. 4  
C. 6
````

````{dropdown} 解答
**正解：C. 6**

5に最も近い値は6です（差は1）。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
total = 0
for i in range(6):
    if i * 2 > 5:
        total += i
print(total)
```

A. 9  
B. 12  
C. 15
````

````{dropdown} 解答
**正解：B. 12**

i * 2 > 5を満たすのはi=3,4,5で、3 + 4 + 5 = 12です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
data = [6, 3, 9, 2, 8]
even_count = 0
odd_count = 0
for num in data:
    if num % 2 == 0:
        even_count += 1
    else:
        odd_count += 1
print(even_count - odd_count)
```

A. -1  
B. 0  
C. 1
````

````{dropdown} 解答
**正解：C. 1**

偶数は6, 2, 8の3個、奇数は3, 9の2個。3 - 2 = 1です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
nums = [1, 4, 2, 8, 5]
target = 6
found = False
for num in nums:
    if num == target:
        found = True
        break
print(found)
```

A. True  
B. False  
C. 6
````

````{dropdown} 解答
**正解：B. False**

リストに6は含まれていないため、foundはFalseのままです。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
sequence = []
for i in range(5):
    if i == 0:
        sequence.append(1)
    else:
        sequence.append(sequence[i-1] * 2)
print(sequence[3])
```

A. 4  
B. 8  
C. 16
````

````{dropdown} 解答
**正解：B. 8**

sequenceは[1, 2, 4, 8, 16]となり、sequence[3]は8です。
````

````{exercise}
次のPythonコードの出力結果は何でしょうか？

```python
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
diagonal_sum = 0
for i in range(len(matrix)):
    diagonal_sum += matrix[i][i]
print(diagonal_sum)
```

A. 15  
B. 45  
C. 12
````

````{dropdown} 解答
**正解：A. 15**

対角線要素1, 5, 9の合計：$1 + 5 + 9 = 15$です。
````