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
42の錬
======
以下の問題について

- プログラムが何をしてるか
- 出力は何になるか

を考えましょう。

## 01

```python
x = 5
y = 10
z = x + y * 2
print(z)
```

````{dropdown} 解答例

`x`に5を、`y`に10を代入しています。
そのあと、`y`を2倍した結果と`x`を足した結果を`z`に代入しています。
最後に`z`の値（25）を出力しています。

````

## 02

```python
a = 10
b = 3
print(a // b)
print(a % b)
```

````{dropdown} 解答例

このプログラムは、整数の除算と余りを求めています。

`a`に10を、`b`に3を代入しています。
そのあと、`a`を`b`で割った商を`//`で、`a`を`b`で割った余りを`%`で求めて表示しています。

````

## 03

```python
name = "Python"
age = 18
print(f"私は{age}歳で、{name}を学んでいます。")
```

````{dropdown} 解答例

`name`に"Python"を、`age`に18を代入しています。
そのあと、**f文字列**を使って変数の値を文字列に埋め込んで出力しています。

```

## 04

```python
numbers = [10, 5, 8, 3, 7]
print(numbers[0])
print(numbers[-1])
```

````{dropdown} 解答例

このプログラムは、リストの最初の要素と最後の要素を表示しています。

`numbers`に[10, 5, 8, 3, 7]というリストを代入しています。
そのあと、`numbers`の最初の要素を`numbers[0]`で、最後の要素を`numbers[-1]`で表示しています。

````

## 05

```python
numbers = [10, 20, 30, 40, 50]
numbers[2] = 99
print(numbers)
```

````{dropdown} 解答例

このプログラムは、リストの特定の位置の要素を変更して表示しています。

`numbers`に[10, 20, 30, 40, 50]というリストを代入しています。
そのあと、`numbers`の3番目の要素（インデックス2）を99に変更しています。
最後に`numbers`の値を出力しています。

````

## 06

```python
numbers = [1, 2, 3, 4, 5]
print(len(numbers))
print(sum(numbers))
```

````{dropdown} 解答例

このプログラムは、リストの要素数と合計を表示しています。

`numbers`に[1, 2, 3, 4, 5]というリストを代入しています。
そのあと、`numbers`の要素数を`len()`で、合計を`sum()`で求めて表示しています。

````

## 07

```python
numbers = [5, 2, 8, 1, 9]
print(min(numbers))
print(max(numbers))
```

````{dropdown} 解答例

このプログラムは、リストの最小値と最大値を表示しています。

`numbers`に[5, 2, 8, 1, 9]というリストを代入しています。
そのあと、`numbers`の最小値を`min()`で、最大値を`max()`で求めて表示しています。

````

## 08

```python
numbers = [3, 1, 4, 1, 5]
print(3 in numbers)
print(2 in numbers)
```

````{dropdown} 解答例

このプログラムは、リストに特定の値が含まれているかを確認しています。

`numbers`に[3, 1, 4, 1, 5]というリストを代入しています。
そのあと、`3`が`numbers`に含まれているかを`in`で、`2`が`numbers`に含まれているかを`in`で確認しています。
最後に、それぞれの結果を出力しています。

````

## 09

```python
temperature = 25
if temperature > 30:
    message = "暑いです"
elif temperature > 20:
    message = "快適です"
else:
    message = "寒いです"
print(message)
```

````{dropdown} 解答例

`temperature`に25を代入しています。
そのあと`temperature`の値によって条件分岐しています。
`temperature`が30より大きい場合は「暑いです」、20より大きい場合は「快適です」、
それ以外の場合は「寒いです」を変数`message`に代入しています。
最後に`message`の値を出力しています。

````

## 10

```python
score = 85
if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
else:
    grade = "D"
print(grade)
```

````{dropdown} 解答例

このプログラムは、点数に応じて成績を表示しています。

`score`に85を代入しています。
そのあと、`score`の値によって条件分岐しています。
`score`が90以上の場合は「A」、80以上90未満の場合は「B」、70以上80未満の場合は「C」、それ以外の場合は「D」を変数`grade`に代入しています。
最後に`grade`の値を出力しています。

````

## 11

```python
x = 15
y = 4
print(x > 10 and y < 5)
print(x > 20 or y < 5)
```

````{dropdown} 解答例

このプログラムは、論理演算子`and`と`or`を使った条件式の評価をしています。

`x`に15を、`y`に4を代入しています。
そのあと、`x`が10より大きいかつ`y`が5より小さいかを`and`で、`x`が20より大きいか`y`が5より小さいかを`or`で評価しています。
最後に、それぞれの結果を出力しています。

````

## 12

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
print(numbers[2:5])
print(numbers[5:])
```

````{dropdown} 解答例

このプログラムは、リストの3番目から5番目の要素と、5番目以降の要素を表示しています。

`numbers`に[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]というリストを代入しています。
そのあと、`numbers`の3番目から5番目の要素を`numbers[2:5]`で、5番目以降の要素を`numbers[5:]`で表示しています。

````

## 13

```python
data = [10, 20, 30, 40, 50]
print(data[1:4])
print(data[::2])
```

````{dropdown} 解答例

このプログラムは、リストのスライス記法で部分リストと飛び飛びの要素を取得して表示しています。

`data`に[10, 20, 30, 40, 50]というリストを代入しています。
そのあと、`data`の1番目から4番目の要素を`data[1:4]`で、
2つ飛びで要素を`data[::2]`で取得して表示しています。

````

## 14

```python
original = [1, 2, 3]
multiplied = original * 3
print(multiplied)
print(len(multiplied))
```

````{dropdown} 解答例

このプログラムは、リストを3回繰り返した新しいリストを作成し、その内容と長さを表示しています。

`original`に[1, 2, 3]というリストを代入しています。
`multiplied`に`original`を3回繰り返したリストを代入しています。
そのあと、`multiplied`の値とその長さを出力しています。

````

## 15

```python
numbers = [2, 4, 6, 8]
total = 0
for num in numbers:
    total += num
print(total)
```

````{dropdown} 解答例

`numbers`に[2, 4, 6, 8]というリストを、`total`に0を代入しています。
そのあと、`numbers`の要素を順番に取り出して、それぞれを`total`に足しています。
最後に`total`の値を出力しています。

````

## 16

```python
count = 0
for i in range(1, 11):
    if i % 3 == 0:
        count += 1
print(count)
```

````{dropdown} 解答例

このプログラムは、1から10までの中で3の倍数の個数を数えています。

`count`に0を代入しています。
そのあと、`i`に1から10までの数を順番に代入しています。
`i`が3の倍数の場合は`count`に1を足しています。
最後に`count`の値を出力しています。

````

## 17

```python
text = "apple"
count = 0
for char in text:
    if char == 'p':
        count += 1
print(count)
```

````{dropdown} 解答例

このプログラムは、文字列の中に'p'が何個あるかを数えて表示しています。

`text`に"apple"という文字列を代入しています。
`count`に0を代入しています。
そのあと、`text`の要素を順番に取り出して、`char`に代入しています。
`char`が'p'の場合は`count`に1を足しています。
最後に`count`の値を出力しています。

````

## 18

```python
text = "programming"
vowels = "aeiou"
count = 0
for char in text:
    if char in vowels:
        count += 1
print(count)
```

````{dropdown} 解答例

このプログラムは、文字列の中の母音の個数を数えています。

`text`に"programming"という文字列を、`vowels`に"aeiou"という文字列を代入しています。
`count`に0を代入しています。
そのあと、`text`の要素を順番に取り出して、`char`に代入しています。
`char`が`vowels`に含まれている場合は`count`に1を足しています。
最後に`count`の値を出力しています。

````

## 19

```python
data = [1, 5, 3, 9, 2, 8]
count = 0
for num in data:
    if 3 <= num <= 7:
        count += 1
print(count)
```

````{dropdown} 解答例

このプログラムは、リストの中から3以上7以下の数の個数を数えて表示しています。

`data`に[1, 5, 3, 9, 2, 8]というリストを代入しています。
`count`に0を代入しています。
そのあと、`data`の要素を順番に取り出して、`num`に代入しています。
`num`が3以上7以下の場合は`count`に1を足しています。
最後に`count`の値を出力しています。

````

## 20

```python
numbers = [10, 5, 15, 3, 12]
count = 0
for num in numbers:
    if num > 8:
        count += 1
print(count)
```

````{dropdown} 解答例

このプログラムは、リストの中から8より大きい数の個数を数えて表示しています。

`numbers`に[10, 5, 15, 3, 12]というリストを代入しています。
`count`に0を代入しています。
そのあと、`numbers`の要素を順番に取り出して、`num`に代入しています。
`num`が8より大きい場合は`count`に1を足しています。
最後に`count`の値を出力しています。

````

## 21

```python
result = ""
for i in range(5):
    result += str(i)
print(result)
```

````{dropdown} 解答例

このプログラムは、0から4までの数値を文字列に変換して連結して表示しています。

`result`に空の文字列を代入しています。
そのあと、`i`に0,1,2,3,4を順番に代入しています。
`result`に`i`を文字列に変換して連結しています。
最後に`result`の値を出力しています。

````

## 22

```python
total = 0
for i in range(1, 6):
    total += i * i
print(total)
```

````{dropdown} 解答例

このプログラムは、1から5までの数の2乗の合計を求めて表示しています。

`total`に0を代入しています。
そのあと、`i`に1,2,3,4,5を順番に代入しています。
`total`に`i`の2乗を足しています。
最後に`total`の値を出力しています。

````

## 23

```python
numbers = [1, 2, 3, 4, 5]
even_numbers = []
for num in numbers:
    if num % 2 == 0:
        even_numbers.append(num)
print(even_numbers)
```

````{dropdown} 解答例

このプログラムは、リストの中から偶数だけを取り出して新しいリストを作成し、表示しています。

`numbers`に[1, 2, 3, 4, 5]というリストを代入しています。
`even_numbers`に空のリストを代入しています。
そのあと、`numbers`の要素を順番に取り出して、`num`に代入しています。
`num`が偶数の場合は`even_numbers`に`num`を追加しています。
最後に`even_numbers`の値を出力しています。

````

## 24

```python
numbers = [1, 2, 3]
doubled = []
for num in numbers:
    doubled.append(num * 2)
print(doubled)
```

````{dropdown} 解答例

このプログラムは、リストの各要素を2倍にした新しいリストを作成し、表示しています。

`numbers`に[1, 2, 3]というリストを代入しています。
`doubled`に空のリストを代入しています。
そのあと、`numbers`の要素を順番に取り出して、`num`に代入しています。
`num`を2倍にして`doubled`に追加しています。
最後に`doubled`の値を出力しています。

````

## 25

```python
numbers = [5, 2, 8, 1, 9]
max_num = numbers[0]
for num in numbers:
    if num > max_num:
        max_num = num
print(max_num)
```

````{dropdown} 解答例

このプログラムは、リストの中から最大値を見つけて表示しています。

`numbers`に[5, 2, 8, 1, 9]というリストを代入しています。
`max_num`に`numbers`の最初の要素を代入しています。
そのあと、`numbers`の要素を順番に取り出して、`num`に代入しています。
`num`が`max_num`より大きい場合は`max_num`に`num`を代入しています。
最後に`max_num`の値を出力しています。

````

## 26

```python
base = 2
exponent = 4
result = 1
for i in range(exponent):
    result *= base
print(result)
```

````{dropdown} 解答例

このプログラムは、2の4乗を計算して表示しています。

`base`に2を、`exponent`に4を代入しています。
`result`に1を代入しています。
そのあと、`i`に0,1,2,3を順番に代入しています。
`result`に`base`を掛けています。
最後に`result`の値を出力しています。

````

## 27

```python
numbers = [2, 4, 6, 8, 10]
product = 1
for num in numbers:
    product *= num
print(product)
```

````{dropdown} 解答例

このプログラムは、リストの全要素の積を計算して表示しています。

`numbers`に[2, 4, 6, 8, 10]というリストを代入しています。
`product`に1を代入しています。
そのあと、`numbers`の要素を順番に取り出して、`num`に代入しています。
`product`に`product`に`num`を掛けています。
最後に`product`の値を出力しています。

````

## 28

```python
words = ["cat", "elephant", "dog", "tiger"]
longest = words[0]
for word in words:
    if len(word) > len(longest):
        longest = word
print(longest)
```

````{dropdown} 解答例

このプログラムは、リストの中から最も長い文字列を見つけて表示しています。

`words`に["cat", "elephant", "dog", "tiger"]というリストを代入しています。
`longest`に`words`の最初の要素を代入しています。
そのあと、`words`の要素を順番に取り出して、`word`に代入しています。
`word`の長さが`longest`の長さより長い場合は`longest`に`word`を代入しています。
最後に`longest`の値を出力しています。

````

## 29

```python
numbers = [1, 2, 2, 3, 3, 3, 4]
unique = []
for num in numbers:
    if num not in unique:
        unique.append(num)
print(unique)
```

````{dropdown} 解答例

このプログラムは、リストの重複を除いた要素だけを新しいリストに追加して表示しています。

`numbers`に[1, 2, 2, 3, 3, 3, 4]というリストを代入しています。
`unique`に空のリストを代入しています。
そのあと、`numbers`の要素を順番に取り出して、`num`に代入しています。
`num`が`unique`に含まれていない場合は`unique`に`num`を追加しています。
最後に`unique`の値を出力しています。

````

## 30

```python
numbers = [15, 25, 35, 45, 55]
target = 35
index = -1
for i in range(len(numbers)):
    if numbers[i] == target:
        index = i
        break
print(index)
```

````{dropdown} 解答例

このプログラムは、リストの中から特定の値を検索し、そのインデックスを見つけて表示しています。

`numbers`に[15, 25, 35, 45, 55]というリストを代入しています。
`target`に35を代入しています。
`index`に-1を代入しています。
そのあと、`i`に0,1,2,3,4を順番に代入しています。
`numbers[i]`が`target`と等しい場合は`index`に`i`を代入してループを抜けています。
最後に`index`の値を出力しています。

````

## 31

```python
data = [1, 2, 3, 4, 5]
result = [x * 2 for x in data if x % 2 == 1]
print(result)
```

````{dropdown} 解答例

このプログラムは、リストの中から奇数だけを取り出して2倍にした新しいリストを作成し、表示しています。

`data`に[1, 2, 3, 4, 5]というリストを代入しています。
そのあと、`data`の要素を順番に取り出して、`x`に代入しています。
`x`が奇数の場合は`result`に`x`を2倍した値を追加しています。
最後に`result`の値を出力しています。

````

## 32

```python
for i in range(3):
    for j in range(2):
        print(f"{i}-{j}")
```

````{dropdown} 解答例

このプログラムは、二重ループで、外側の`i`が0,1,2、内側の`j`が0,1を取り、それぞれの組み合わせを表示しています。

`i`に0,1,2を順番に代入しています。
`j`に0,1を順番に代入しています。
そのあと、`i`と`j`を表示しています。

内側のループが先に処理されているのを確認しましょう。

````

## 33

```python
matrix = [[1, 2], [3, 4], [5, 6]]
for row in matrix:
    print(row[1])
```

````{dropdown} 解答例

このプログラムは、2次元リストの各行の2番目の要素（インデックス1）を表示しています。

`matrix`に[[1, 2], [3, 4], [5, 6]]という2次元リストを代入しています。
そのあと、`matrix`の要素を順番に取り出して、`row`に代入しています。
`row`の2番目の要素を表示しています。

````

## 34

```python
matrix = [[1, 2, 3], [4, 5, 6]]
for row in matrix:
    for element in row:
        print(element, end=" ")
    print()
```

````{dropdown} 解答例

このプログラムは、2次元リストの全要素を行ごとに表示しています。

`matrix`に[[1, 2, 3], [4, 5, 6]]という2次元リストを代入しています。
そのあと、`matrix`の要素を順番に取り出して、`row`に代入しています。
`row`の要素を順番に取り出して、`element`に代入しています。
`element`を表示しています。

````

## 35

```python
matrix = [[2, 4], [6, 8], [10, 12]]
column_sum = 0
for row in matrix:
    column_sum += row[0]
print(column_sum)
```

````{dropdown} 解答例

このプログラムは、2次元リストの最初の列（0番目のインデックス）の合計を計算して表示しています。

`matrix`に[[2, 4], [6, 8], [10, 12]]という2次元リストを代入しています。
`column_sum`に0を代入しています。
そのあと、`matrix`の要素を順番に取り出して、`row`に代入しています。
`column_sum`に`row`の最初の要素を足しています。
最後に`column_sum`の値を出力しています。

````

## 36

```python
words = ["apple", "banana", "cherry"]
for i, word in enumerate(words):
    print(f"{i}: {word}")
```

````{dropdown} 解答例

このプログラムは、リストの要素とインデックスを表示しています。

`words`に["apple", "banana", "cherry"]というリストを代入しています。
そのあと、`words`の要素を順番に取り出して、`word`に代入しています。
`i`と`word`を表示しています。

`enumerate()`でインデックスと値を同時に取得しています。

````

## 37

```python
numbers = [1, 2, 3, 4, 5]
sum_odd = 0
sum_even = 0
for num in numbers:
    if num % 2 == 0:
        sum_even += num
    else:
        sum_odd += num
print(sum_odd)
print(sum_even)
```

````{dropdown} 解答例

このプログラムは、リストの中から奇数の合計と偶数の合計を別々に計算して表示しています。

`numbers`に[1, 2, 3, 4, 5]というリストを代入しています。
`sum_odd`に0を代入しています。
`sum_even`に0を代入しています。
そのあと、`numbers`の要素を順番に取り出して、`num`に代入しています。
`num`が偶数の場合は`sum_even`に`num`を足しています。

````

## 38

```python
grades = [85, 92, 78, 96, 88]
above_90 = []
below_80 = []
for grade in grades:
    if grade >= 90:
        above_90.append(grade)
    elif grade < 80:
        below_80.append(grade)
print(above_90)
print(below_80)
```

````{dropdown} 解答例

このプログラムは、点数リストを90点以上と80点未満に分けて表示しています。

`grades`に[85, 92, 78, 96, 88]というリストを代入しています。
`above_90`と`below_80`に空のリストを代入しています。
そのあと、`grades`の要素を順番に取り出して、`grade`に代入しています。
`grade`が90以上の場合は`above_90`に、80未満の場合は`below_80`に追加しています。
最後に両方のリストの値を出力しています。

````

## 39

```python
text = "Python"
vowels = "aeiou"
consonants = ""
for char in text.lower():
    if char not in vowels:
        consonants += char
print(consonants)
```

````{dropdown} 解答例

このプログラムは、文字列の中から母音以外の文字（子音）だけを取り出して表示しています。

`text`に"Python"という文字列を代入しています。
`vowels`に"aeiou"という文字列を代入しています。
`consonants`に空の文字列を代入しています。
そのあと、`text`の要素を順番に取り出して、`char`に代入しています。
`char`が`vowels`に含まれていない場合は`consonants`に`char`を追加しています。
最後に`consonants`の値を出力しています。

````

## 40

```python
numbers = [1, 3, 5, 7, 9]
total = 0
for i in range(len(numbers)):
    total += numbers[i] * (i + 1)
print(total)
```

````{dropdown} 解答例

このプログラムは、リストの各要素に(インデックス+1)を掛けて合計して表示しています。

`numbers`に[1, 3, 5, 7, 9]というリストを代入しています。
`total`に0を代入しています。
そのあと、`i`に0,1,2,3,4を順番に代入しています。
`total`に`numbers[i]`に`(i + 1)`を掛けた値を足しています。
最後に`total`の値を出力しています。

````

## 41

```python
numbers = [3, 7, 2, 9, 1, 5]
differences = []
for i in range(len(numbers) - 1):
    diff = numbers[i + 1] - numbers[i]
    differences.append(diff)
print(differences)
```

````{dropdown} 解答例

このプログラムは、リストの隣り合う要素の差を計算した新しいリストを作成して表示しています。

`numbers`に[3, 7, 2, 9, 1, 5]というリストを代入しています。
`differences`に空のリストを代入しています。
そのあと、`i`に0,1,2,3,4を順番に代入しています。
`diff`に`numbers[i + 1]`から`numbers[i]`を引いた値を代入しています。
`differences`に`diff`を追加しています。
最後に`differences`の値を出力しています。

````

## 42

```python
numbers = [5, 3, 8, 1, 9, 2]
pairs = []
for i in range(len(numbers)):
    for j in range(i + 1, len(numbers)):
        if numbers[i] + numbers[j] == 10:
            pairs.append((numbers[i], numbers[j]))
print(pairs)
```

````{dropdown} 解答例

このプログラムは、リストの中から2つの数の和が10になるペアを見つけて表示しています。

`numbers`に[5, 3, 8, 1, 9, 2]というリストを代入しています。
`pairs`に空のリストを代入しています。
そのあと、`i`に0,1,2,3,4,5を順番に代入しています。
`j`に`i`+1,2,3,4,5を順番に代入しています。
`numbers[i]`と`numbers[j]`の和が10になる場合は`pairs`に`(numbers[i], numbers[j])`を追加しています。
最後に`pairs`の値を出力しています。

````