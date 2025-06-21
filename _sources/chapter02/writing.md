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
100の鍛
=======

````{exercise}
自分の名前を表示しましょう
````

````{dropdown} 解答例

```python
print("鳳凰院 龍聖")
```
````

````{exercise}
自分の名前と星座を表示しましょう。
````

````{dropdown} 解答例

```python
print("鳳凰院 龍聖")
print("蟹座")
```
````

````{exercise}
変数 `x = 10` と `y = 20` の和を表示しましょう。
````

````{dropdown} 解答例

```python
x = 10
y = 20
print(x + y)
```
````

````{exercise}
`price`と`tax`という変数にそれぞれ値を代入し、消費税込みの価格を計算して表示しましょう。

計算式は `価格 * (1 + 税率 / 100)` です。
````

````{dropdown} 解答例

```python
price = 1200
tax = 10
print(int(price * (1 + tax / 100)))
```

````

````{exercise}
2つの変数 `a` と `b` の値を交換するプログラムを書きましょう。
例えば `a=5, b=10` なら `a=10, b=5` とします。
````

````{dropdown} 解答例

```python
a = 5
b = 10
print(f"交換前: a={a}, b={b}")
a, b = b, a
print(f"交換後: a={a}, b={b}")
```

````

````{exercise}
変数 `num = 7` が奇数か偶数かを判定して表示しましょう。
````

````{dropdown} 解答例

```python
num = 7
if num % 2 == 0:
    print("偶数")
else:
    print("奇数")
```
````

````{exercise}
`score`という変数に整数値を代入し、その値が60以上なら合格、そうでない場合は不合格と表示しましょう。
````

````{dropdown} 解答例

```python
score = 60
if score >= 60:
    print("合格")
else:
    print("不合格")
```
````

````{exercise}
`num`という変数に整数値を代入し、その数が正数、負数、ゼロのどれかを判定して表示しましょう。
````

````{dropdown} 解答例

```python
num = -5
if num > 0:
    print("正数")
elif num < 0:
    print("負数")
else:
    print("ゼロ")
```
````

````{exercise}
変数 `age`に整数値を代入し、その値が20歳未満なら「未成年」、20歳以上65歳未満なら「成人」、65歳以上なら「高齢者」と表示しましょう。
````

````{dropdown} 解答例

```python
age = 18
if age < 20:
    print("未成年")
elif age < 65:
    print("成人")
else:
    print("高齢者")
```
````

````{exercise}
3つの数値 `a = 5`, `b = 3`, `c = 8` の中で最大値を見つけて表示しましょう。
````

````{dropdown} 解答例

```python
a = 5
b = 3
c = 8
max_value = a
if b > max_value:
    max_value = b
if c > max_value:
    max_value = c
print(max_value)
```
````

````{exercise}
`score`という変数に整数値を代入し、不可、可、良、優、秀という評価を表示しましょう。
不可は60点未満、可は60点から69点、良は70点から79点、優は80点から89点、秀は90点から100点とします。
````

````{dropdown} 解答例

```python
score = 80
if score < 60:
    print("不可")
elif score < 70:
    print("可")
elif score < 80:
    print("良")
elif score < 90:
    print("優")
else:
    print("秀")
```

````

````{exercise}
変数`num`に整数値を代入し、3の倍数ならFizz、5の倍数ならBuzz、3の倍数かつ5の倍数ならFizzBuzzと表示しましょう。
````

````{dropdown} 解答例

```python
num = 15
if num % 3 == 0 and num % 5 == 0:
    print("FizzBuzz")
elif num % 3 == 0:
    print("Fizz")
elif num % 5 == 0:
    print("Buzz")
else:
    print(num)
```

````

````{exercise}
`year`という変数に整数値を代入し、その年がうるう年かどうかを表示しましょう。
うるう年は、4で割り切れる年ですが、100で割り切れる年はうるう年ではありません。ただし、400で割り切れる年はうるう年です。
````

````{dropdown} 解答例

```python
year = 2024
if year % 4 == 0 and year % 100 != 0 or year % 400 == 0:
    print("うるう年")
else:
    print("平年")
``` 
````

````{exercise}
変数 `temperature = 25` に対して、30度以上なら「暑い」、20度以上30度未満なら「快適」、20度未満なら「寒い」と表示しましょう。
````

````{dropdown} 解答例

```python
temperature = 25
if temperature >= 30:
    print("暑い")
elif temperature >= 20:
    print("快適")
else:
    print("寒い")
```
````

````{exercise}
1から5までの数を表示しましょう。
````

````{dropdown} 解答例

```python
for i in range(1, 6):
    print(i)
```
````

````{exercise}
1から10までの整数を表示しましょう。
````

````{dropdown} 解答例

```python
for i in range(1, 11):
    print(i)
```

````

````{exercise}
5回「Hello」と表示しましょう。
````

````{dropdown} 解答例

```python
for i in range(5):
    print("Hello")
```
````

````{exercise}
`num`という変数に整数値を代入し、その数だけ`#`を表示しましょう。
````

````{dropdown} 解答例

```python
num = 5
for i in range(num):
    print("#", end="")
```

これも同じ結果になります。
```python
print("#" * num)
```
````

````{exercise}
1から10までの数の合計を計算して表示しましょう。
````

````{dropdown} 解答例

```python
total = 0
for i in range(1, 11):
    total += i
print(total)
```
````

````{exercise}
1から20までの整数のうち、偶数のみを表示しましょう。
````

````{dropdown} 解答例

```python
for i in range(1, 21):
    if i % 2 == 0:
        print(i)
```

````

````{exercise}
1から20までの整数のうち、奇数のみを表示しましょう。
````

````{dropdown} 解答例

```python
for i in range(1, 21):
    if i % 2 != 0:
        print(i)
```

````

````{exercise}
1から20までの整数で、3の倍数の時だけその数を表示するプログラムを書きましょう。
````

````{dropdown} 解答例

```python
for i in range(1, 21):
    if i % 3 == 0:
        print(i)
```

````

````{exercise}
1から30までの数で、5の倍数のみを表示しましょう。
````

````{dropdown} 解答例

```python
for i in range(1, 31):
    if i % 5 == 0:
        print(i)
```
````

````{exercise}
1から15までの数で、3の倍数でも5の倍数でもない数を表示しましょう。
````

````{dropdown} 解答例

```python
for i in range(1, 16):
    if i % 3 != 0 and i % 5 != 0:
        print(i)
```
````

````{exercise}
1から100までの数で、7の倍数の個数を数えて表示しましょう。
````

````{dropdown} 解答例

```python
count = 0
for i in range(1, 101):
    if i % 7 == 0:
        count += 1
print(count)
```
````

````{exercise}
`kuku`という変数に整数値（1から9のいずれか）を代入し、その値の段の九九表を表示しましょう。

```
3 * 1 = 3
3 * 2 = 6
3 * 3 = 9
3 * 4 = 12
3 * 5 = 15
3 * 6 = 18
3 * 7 = 21
3 * 8 = 24
3 * 9 = 27
```
````

````{dropdown} 解答例

```python
kuku = 3
for i in range(9):
    print(f"{kuku} * {i + 1} = {kuku * (i + 1)}")
```

````

````{exercise}
`num`という変数に整数値を代入し、1からその値までの合計値を表示しましょう。
````

````{dropdown} 解答例

```python
num = 10
sum = 0
for i in range(num):
    sum += i + 1
print(sum)
```

````

````{exercise}
1から20までの数で、平方数（1, 4, 9, 16...）を表示しましょう。
````

````{dropdown} 解答例

```python
for i in range(1, 21):
    for j in range(1, i + 1):
        if j * j == i:
            print(i)
            break
```
````

````{exercise}
`num`という変数に整数値を代入し、その値の階乗を計算して表示しましょう。
例えば5の階乗は `5 * 4 * 3 * 2 * 1 = 120` です。
````

````{dropdown} 解答例

```python
num = 5
factorial = 1
if num > 0:
    for i in range(1, num + 1):
        factorial *= i
print(factorial)
```

````

````{exercise}
`base = 3, exponent = 4` のとき、$3^4$ を計算して表示しましょう。
````

````{dropdown} 解答例

```python
base = 3
exponent = 4
result = 1
for _ in range(exponent):
    result *= base
print(result)
```

````

````{exercise}
1から50までの数で、6または8で割り切れる数を表示しましょう。
````

````{dropdown} 解答例

```python
for i in range(1, 51):
    if i % 6 == 0 or i % 8 == 0:
        print(i)
```
````

````{exercise}
底辺の長さを`base`という変数に代入し、三角形を表示しましょう。

例えば、baseが3なら以下のような三角形を表示します。

```
^
^^
^^^
```
````

````{dropdown} 解答例

```python
base = 3
for i in range(base):
    print("^" * (i + 1))
```

````

````{exercise}
`height`という変数に整数値を代入し、その高さのピラミッド（二等辺三角形）を表示しましょう。

`height`が3なら以下のように表示します。

```
  *
 ***
*****
```
````

````{dropdown} 解答例

```python
height = 3
for i in range(height):
    spaces = " " * (height - i - 1)
    stars = "*" * (2 * i + 1)
    print(spaces + stars)
```

````

````{exercise}
5×5の数字の正方形を表示しましょう。各位置に行番号×列番号の値を表示してください。

```
1 2 3 4 5
2 4 6 8 10
3 6 9 12 15
4 8 12 16 20
5 10 15 20 25
```
````

````{dropdown} 解答例

```python
for i in range(1, 6):
    for j in range(1, 6):
        print(i * j, end=" ")
    print()
```
````

````{exercise}
1から20までの数で、完全数を見つけて表示しましょう。
完全数とは、自分自身を除く約数の和が自分自身と等しい数です。
````

````{dropdown} 解答例

```python
for num in range(1, 21):
    divisor_sum = 0
    for i in range(1, num):
        if num % i == 0:
            divisor_sum += i
    if divisor_sum == num:
        print(num)
```
````

````{exercise}
リスト `numbers = [1, 2, 3, 4, 5]` の最初の要素と最後の要素を表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [1, 2, 3, 4, 5]
print(f"最初の要素: {numbers[0]}")
print(f"最後の要素: {numbers[-1]}")
```

````

````{exercise}
リスト `numbers = [1, 2, 3, 4, 5]` のすべての要素を表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [1, 2, 3, 4, 5]
for num in numbers:
    print(num)
```

````

````{exercise}
リスト `numbers = [1, 2, 3, 4, 5]` の要素数を表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [1, 2, 3, 4, 5]
print(len(numbers))
```

````

````{exercise}
リスト `numbers = [10, 25, 3, 17, 8]` の中で15より大きい要素を表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [10, 25, 3, 17, 8]
for num in numbers:
    if num > 15:
        print(num)
```
````

````{exercise}
リスト `numbers = [1, 2, 3, 4, 5]` の各要素にそのインデックス番号を付けて表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [1, 2, 3, 4, 5]
for i, num in enumerate(numbers):
    print(f"インデックス{i}: {num}")
```

````

````{exercise}
リスト `numbers = [2, 4, 6, 8, 10]` のすべての要素の合計を計算して表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [2, 4, 6, 8, 10]
total = 0
for num in numbers:
    total += num
print(total)
```
````

````{exercise}
`numbers = [5, 2, 8, 1, 9]` というリストの最大値を、ループで見つけて表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [5, 2, 8, 1, 9]
max_num = numbers[0]
for num in numbers:
    if num > max_num:
        max_num = num
print(max_num)
```

````

````{exercise}
`numbers = [5, 2, 8, 1, 9]` というリストの最小値を、ループで見つけて表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [5, 2, 8, 1, 9]
min_num = numbers[0]
for num in numbers:
    if num < min_num:
        min_num = num
print(min_num)
```

````

````{exercise}
リスト `numbers = [3, 7, 2, 9, 1]` の中で5より小さい要素の個数を数えましょう。
````

````{dropdown} 解答例

```python
numbers = [3, 7, 2, 9, 1]
count = 0
for num in numbers:
    if num < 5:
        count += 1
print(count)
```
````

````{exercise}
`numbers = [10, 20, 30, 40, 50]` というリストがあります。
変数`target`に値を代入し、その値がこのリストに含まれているかどうかを判定し、含まれていればそのインデックスを、含まれていなければ-1を表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [10, 20, 30, 40, 50]
target = 30
result = -1
for i in range(len(numbers)):
    if numbers[i] == target:
        result = i
        break
print(result)
```

````

````{exercise}
リスト `grades = [85, 92, 78, 96, 73]` の中で80点以上の成績の個数を数えましょう。
````

````{dropdown} 解答例

```python
grades = [85, 92, 78, 96, 73]
count = 0
for grade in grades:
    if grade >= 80:
        count += 1
print(count)
```
````

````{exercise}
`numbers = [-2, 0, 5, -8, 10]` があります。
正の数だけを合計した値を表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [-2, 0, 5, -8, 10]
sum_positives = 0
for num in numbers:
    if num > 0:
        sum_positives += num
print(sum_positives)
```

````

````{exercise}
リスト `numbers = [12, 7, 23, 8, 15]` の平均値を計算して表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [12, 7, 23, 8, 15]
total = 0
for num in numbers:
    total += num
average = total / len(numbers)
print(average)
```
````

````{exercise}
`numbers = [1, 2, 3, 4, 5]` の要素を逆順にした新しいリスト `reversed_numbers` を作成して表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [1, 2, 3, 4, 5]
reversed_numbers = []
for i in numbers:
    reversed_numbers.insert(0, i)
print(reversed_numbers)
```

````

````{exercise}
`numbers = [1, 2, 3, 4, 5]` の各要素を2倍にした新しいリスト `doubled_numbers` を作成しましょう。
````

````{dropdown} 解答例

```python
numbers = [1, 2, 3, 4, 5]
doubled_numbers = []
for num in numbers:
    doubled_numbers.append(num * 2)
print(doubled_numbers)
```

````

````{exercise}
`numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]` があります。
奇数だけを取り出した新しいリストを作成しましょう。
````

````{dropdown} 解答例

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
odd_numbers = []
for num in numbers:
    if num % 2 != 0:
        odd_numbers.append(num)
print(odd_numbers)
```

````

````{exercise}
リスト `scores = [75, 82, 90, 67, 85]` の中で80点以上の点数だけを新しいリストに入れて表示しましょう。
````

````{dropdown} 解答例

```python
scores = [75, 82, 90, 67, 85]
high_scores = []
for score in scores:
    if score >= 80:
        high_scores.append(score)
print(high_scores)
```
````

````{exercise}
リスト `[8, 3, 1, 5, 6]` の各要素に、そのインデックス番号を加えた新しいリストを作成しましょう。
例えば、`[8, 3, 1, 5, 6]` というリストがあった場合、`[8, 4, 3, 8, 10]` という新しいリストを作成しましょう。
````

````{dropdown} 解答例

```python
original = [8, 3, 1, 5, 6]
result = []
for i, n in enumerate(original):
    result.append(n + i)
print(result)
```

````

````{exercise}
`numbers = [1, 2, 2, 3, 4, 4, 5]` というリストから重複する値を取り除いた新しいリストを作成して表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [1, 2, 2, 3, 4, 4, 5]
unique_numbers = []
for i in numbers:
    if i not in unique_numbers:
        unique_numbers.append(i)
print(unique_numbers)
```

````

````{exercise}
リスト `a = [1, 2, 3]` と `b = [4, 5, 6]` を連結して、`[1, 2, 3, 4, 5, 6]` という新しいリストを作成して表示しましょう。
````

````{dropdown} 解答例

```python
a = [1, 2, 3]
b = [4, 5, 6]
for i in b:
    a.append(i)
print(a)
```

````

````{exercise}
リスト `numbers = [10, 5, 8, 3, 7]` の中で、隣接する要素の差が2以下のペアを見つけて表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [10, 5, 8, 3, 7]
for i in range(len(numbers) - 1):
    diff = abs(numbers[i] - numbers[i + 1])
    if diff <= 2:
        print(f"{numbers[i]} と {numbers[i + 1]}")
```
````

````{exercise}
九九の表（1の段から9の段まで）をすべて表示しましょう。

例えば、以下のような結果になります。
```
      1   2   3   4   5   6   7   8   9
1:    1   2   3   4   5   6   7   8   9
2:    2   4   6   8  10  12  14  16  18
3:    3   6   9  12  15  18  21  24  27
4:    4   8  12  16  20  24  28  32  36
5:    5  10  15  20  25  30  35  40  45
6:    6  12  18  24  30  36  42  48  54
7:    7  14  21  28  35  42  49  56  63
8:    8  16  24  32  40  48  56  64  72
9:    9  18  27  36  45  54  63  72  81
```
````

````{dropdown} 解答例

```python
print("   ", end="")
for j in range(1, 10):
    print(f"{j:4}", end="")
print()

for i in range(1, 10):
    print(f"{i}: ", end="")
    for j in range(1, 10):
        print(f"{i * j:4}", end="")
    print()
```

````

````{exercise}
リスト `numbers = [4, 7, 2, 9, 1]` の中で最大値と最小値の差を計算して表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [4, 7, 2, 9, 1]
max_num = numbers[0]
min_num = numbers[0]
for num in numbers:
    if num > max_num:
        max_num = num
    if num < min_num:
        min_num = num
print(max_num - min_num)
```
````

````{exercise}
1から6までの整数値をランダムに生成し、その値を表示するには以下のプログラムを実行します。

```python
import random
print(random.randint(1, 6))
```

1から6までの整数値をランダムに10回生成し、その平均値を表示しましょう。
````

````{dropdown} 解答例

```python
import random
sum = 0
for i in range(10):
    sum += random.randint(1, 6)
print(sum / 10)
```

````

````{exercise}
1から10までの整数値を3つランダムに生成し、その値を表示しましょう。

例えば、以下のような結果になります。
```
[4, 5, 1]
```
````

````{dropdown} 解答例

```python
import random
slots = [random.randint(1, 10) for _ in range(3)]
print(slots)
```
````

````{exercise}
1から10までの整数値を3つランダムに生成し、すべての値が同じなら「当たり」と表示しましょう。
````

````{dropdown} 解答例

```python
import random
slots = [random.randint(1, 10) for _ in range(3)]
if slots[0] == slots[1] == slots[2]:
    print("当たり")
```
````

````{exercise}
1から10までの整数値を3つランダムに生成し、
すべての値が同じになるまで繰り返し、同じになったら繰り返した回数とその値を表示しましょう。
ただし、繰り返す回数は10000回です。
````

````{dropdown} 解答例

```python
import random
for i in range(10000):
    slots = [random.randint(1, 10) for _ in range(3)]
    if slots[0] == slots[1] == slots[2]:
        print(f"{i + 1} {slots}")
        break
```

````

````{exercise}
0から9までの数字がランダムな順序で入ったリストを作成しましょう。
````

````{dropdown} 解答例

```python
import random
numbers = list(range(10))
random.shuffle(numbers)
print(numbers)
```

````

````{exercise}
`num`という変数に整数値を代入し、その数が素数かどうかを判定して表示しましょう。
（素数：1とその数自身以外に約数を持たない正の整数）
````

````{dropdown} 解答例

```python
num = 13
is_prime = True

if num <= 1:
    is_prime = False
else:
    for i in range(2, num):
        if num % i == 0:
            is_prime = False
            break

if is_prime:
    print(f"{num}は素数です")
else:
    print(f"{num}は素数ではありません")
```

````

````{exercise}
フィボナッチ数列の最初の10項を表示するプログラムを作成しましょう。
フィボナッチ数列は、`F(0)=0`, `F(1)=1`, `F(n)=F(n-1)+F(n-2)`で定義されます。
````

````{dropdown} 解答例

```python
a, b = 0, 1
for _ in range(10):
    print(a)
    a, b = b, a + b
```

````

````{exercise}
`base2`というリストに0か1の値が入っています。
これを2進数と考え、その値を10進数に変換して表示しましょう。

例えば、`base2 = [1, 0, 1, 1]`なら、10進数の11を表示します。

計算式は、以下の通り。

$
1011_2 = 1 \times 2^3 + 0 \times 2^2 + 1 \times 2^1 + 1 \times 2^0 = 11_{10}
$
````

````{dropdown} 解答例

```python
base2 = [1, 0, 1, 1]
base10 = 0
for i in range(len(base2)):
    power = len(base2) - i - 1
    base10 += base2[i] * (2 ** power)
print(base10)
```

````

````{exercise}
`base10`という変数に10進数の値を代入し、それを2進数を表すリストに変換して表示しましょう。

例えば、`base10 = 11`なら、`[1, 0, 1, 1]`を表示します。
````

````{dropdown} 解答例

```python
base10 = 11
base2 = []
while base10 > 0:
    base2.append(base10 % 2)
    base10 //= 2
base2.reverse()
print(base2)
```

````

````{exercise}
1から100までの整数のうち、偶数のみを要素とするリストを作成しましょう。
リスト内包表記を使うと一行で書けます。
````

````{dropdown} 解答例

```python
even_numbers = [i for i in range(1, 101) if i % 2 == 0]
print(even_numbers)
```

````

````{exercise}
`numbers = [1, 2, 3, 4, 5]` の各要素を2倍にした新しいリスト `doubled_numbers` を作成しましょう。
リスト内包表記を使って書いてみましょう。
````

````{dropdown} 解答例

```python
numbers = [1, 2, 3, 4, 5]
doubled_numbers = [num * 2 for num in numbers]
print(doubled_numbers)
```

````

````{exercise}
`numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]` があります。
奇数だけを取り出した新しいリストをリスト内包表記で作成しましょう。
````

````{dropdown} 解答例

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
odd_numbers = [num for num in numbers if num % 2 != 0]
print(odd_numbers)
```

````

````{exercise}
`a = [1, 2, 3, 4]` と `b = [3, 4, 5, 6]` という2つのリストがあります。
これらの積集合（intersection）を求めて表示しましょう。
````

````{dropdown} 解答例

```python
a = [1, 2, 3, 4]
b = [3, 4, 5, 6]
intersection = []

for i in a:
    if i in b:
        intersection.append(i)

print(intersection)
```

````

````{exercise}
`a = [1, 2, 3, 4]` と `b = [3, 4, 5, 6]` という2つのリストがあります。
これらの和集合（union）を求めて表示しましょう。
````

````{dropdown} 解答例

```python
a = [1, 2, 3, 4]
b = [3, 4, 5, 6]
union = []

for i in a:
    if i not in union:
        union.append(i)

for i in b:
    if i not in union:
        union.append(i)

print(union)
```

````

````{exercise}
リスト `numbers = [3, 1, 4]` があります。
インデックス`0`の要素とインデックス`1`の要素を交換して `[1, 3, 4]` となるようにし、表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [3, 1, 4]
print(f"交換前: {numbers}")
numbers[0], numbers[1] = numbers[1], numbers[0]
print(f"交換後: {numbers}")
```

````

````{exercise}
`n`という変数に整数値を代入し、`n x n` の単位行列（対角成分が1で、他は0）を2次元リストで作成しましょう。
````

````{dropdown} 解答例

```python
n = 5
identity_matrix = [[0 for _ in range(n)] for _ in range(n)]
for i in range(n):
    identity_matrix[i][i] = 1
    
for row in identity_matrix:
    print(row)
```

````

````{exercise}
`matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]` という2次元リスト（行列）があります。
この行列のすべての要素を表示しましょう。
````

````{dropdown} 解答例

```python
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
for row in matrix:
    for element in row:
        print(element, end=" ")
    print()
```

````

````{exercise}
`matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]` という2次元リスト（行列）があります。
この行列の対角成分（左上から右下への要素）を表示しましょう。
````

````{dropdown} 解答例

```python
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
for i in range(len(matrix)):
    print(matrix[i][i])
```

````

````{exercise}
`a`というリストに[1, 2, 3, 4, 5]が入っています。
これを1つずつ右にずらして表示しましょう。
一番最後の値は一番最初に移動します。

例えば、以下のような結果になります。
```
[5, 1, 2, 3, 4]
[4, 5, 1, 2, 3]
[3, 4, 5, 1, 2]
[2, 3, 4, 5, 1]
[1, 2, 3, 4, 5]
```
````

````{dropdown} 解答例

```python
a = [1, 2, 3, 4, 5]
for i in range(len(a)):
    a.insert(0, a.pop())
    print(a)
```

````

````{exercise}
リスト `my_list = [1, 2, 3, 4, 5]` があります。
`mylist2 = mylist` という代入をして、mylist2の先頭の値を`99`にして、`mylist`を表示してみましょう。
````

````{dropdown} 解答例

```python
my_list = [1, 2, 3, 4, 5]
mylist2 = my_list
mylist2[0] = 99
print(my_list)
```

このように、リストを代入すると、同じリストを参照していることになります。

````

````{exercise}
リスト `my_list = [1, 2, 3, 4, 5]` があります。
リストのコピーを作成し、コピーしたリストの最初の要素を`99`に変更し、
`my_list`と`copied_list`を表示してみましょう。
コピーには`copy()`メソッドを使いましょう。
````

````{dropdown} 解答例

```python
my_list = [1, 2, 3, 4, 5]
copied_list = my_list.copy()

copied_list[0] = 99

print(f"元のリスト: {my_list}")
print(f"コピーしたリスト: {copied_list}")
```

````

````{exercise}
`numbers`という変数にリストを代入し、このリストが昇順（小さい順）にソートされているかどうかを判定する真偽値を表示しましょう。
例えば、 `[1, 10, 5, 8, 2, 9]` を代入した場合、`False`が表示されます。
````

````{dropdown} 解答例

```python
numbers = [1, 10, 5, 8, 2, 9]
is_sorted = True
for i in range(len(numbers) - 1):
    if numbers[i] > numbers[i+1]:
        is_sorted = False
        break
print(is_sorted)
```

````

````{exercise}
リスト `numbers = [5, 2, 8, 1, 9]` があります。
このリストから**最小値を見つけ**、その値と**リストの最初の要素を交換**するプログラムを書きましょう。
````

````{dropdown} 解答例

```python
numbers = [5, 2, 8, 1, 9]
min_val = numbers[0]
min_idx = 0

for i in range(1, len(numbers)):
    if numbers[i] < min_val:
        min_val = numbers[i]
        min_idx = i

numbers[0], numbers[min_idx] = numbers[min_idx], numbers[0]

print(numbers)
```

````

````{exercise}
リスト `numbers = [3, 5, 1, 2, 4]` があります。
隣り合う要素を比較し、もし左が右より大きければ交換するという処理を、リストの先頭から末尾まで一度だけ行い、その結果を表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [3, 5, 1, 2, 4]
for i in range(len(numbers) - 1):
    if numbers[i] > numbers[i+1]:
        numbers[i], numbers[i+1] = numbers[i+1], numbers[i]
print(numbers)
```

````

````{exercise}
リスト `numbers = [3, 5, 1, 2, 4]` があります。
隣り合う要素を比較し、もし右が左より大きければ交換するという処理を、リストの先頭から末尾まで一度だけ行い、その結果を表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [3, 5, 1, 2, 4]
n = len(numbers)
for i in range(len(numbers) - 1):
    if numbers[i] < numbers[i+1]:
        numbers[i], numbers[i+1] = numbers[i+1], numbers[i]
print(numbers)
```

````

````{exercise}
`sorted_list = [1, 3, 5, 7]` と `new_value = 4` があります。
`sorted_list` のソートされた順序を保ったまま `new_value` を挿入し、結果を表示しましょう。
````

````{dropdown} 解答例

```python
sorted_list = [1, 3, 5, 7]
new_value = 4

inserted = False
for i in range(len(sorted_list)):
    if new_value < sorted_list[i]:
        sorted_list.insert(i, new_value)
        inserted = True
        break
if not inserted:
    sorted_list.append(new_value)

print(sorted_list)
```

````

````{exercise}
リスト `numbers = [5, 2, 8, 1, 9]` があります。
リストを2つに分割して、各部分で最小値を見つけ、それらを表示しましょう。
分割位置は中央(`len(numbers) // 2`)とします。
````

````{dropdown} 解答例

```python
numbers = [5, 2, 8, 1, 9]
mid = len(numbers) // 2
left_half = numbers[:mid]
right_half = numbers[mid:]

left_min = left_half[0]
for num in left_half:
    if num < left_min:
        left_min = num

right_min = right_half[0]
for num in right_half:
    if num < right_min:
        right_min = num

print(f"左半分の最小値: {left_min}")
print(f"右半分の最小値: {right_min}")
```

````

````{exercise}
リスト `numbers = [4, 2, 2, 8, 3, 3, 1]` があります。
各数値が何回現れるかをカウントして表示しましょう。

以下のような結果になるでしょう。
```
4: 1回
2: 2回
8: 1回
3: 2回
1: 1回
```
````

````{dropdown} 解答例

```python
numbers = [4, 2, 2, 8, 3, 3, 1]
counts = {}

for num in numbers:
    if num in counts:
        counts[num] += 1
    else:
        counts[num] = 1

for num, count in counts.items():
    print(f"{num}: {count}回")
```

````

````{exercise}
リスト `matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]` があります。
この行列を転置（行と列を入れ替え）して表示しましょう。
````

````{dropdown} 解答例

```python
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
rows = len(matrix)
cols = len(matrix[0])

transposed = [[0 for _ in range(rows)] for _ in range(cols)]

for i in range(rows):
    for j in range(cols):
        transposed[j][i] = matrix[i][j]

for row in transposed:
    print(row)
```

````

````{exercise}
リスト `numbers = [1, 2, 3, 2, 4, 3, 5]` があります。
最初に重複する要素のペアを見つけて、そのインデックスを表示しましょう。

以下のような結果になるでしょう。
```
重複: 値2, インデックス1と3
```
````

````{dropdown} 解答例

```python
numbers = [1, 2, 3, 2, 4, 3, 5]
found = False

for i in range(len(numbers)):
    for j in range(i + 1, len(numbers)):
        if numbers[i] == numbers[j]:
            print(f"重複: 値{numbers[i]}, インデックス{i}と{j}")
            found = True
            break
    if found:
        break
```

````

````{exercise}
リスト `numbers = [5, 3, 8, 4, 2, 7, 1, 6]` があります。
このリストから、偶数が前半、奇数が後半になるように並び替えて表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [5, 3, 8, 4, 2, 7, 1, 6]
evens = []
odds = []

for num in numbers:
    if num % 2 == 0:
        evens.append(num)
    else:
        odds.append(num)

result = evens + odds
print(result)
```

````

````{exercise}
リスト `numbers = [1, 2, 3, 4, 5]` があります。
すべての要素のペアの積を計算し、それらの合計を表示しましょう。

計算は、以下のようになり、
```
1 * 2 = 2
1 * 3 = 3
1 * 4 = 4
1 * 5 = 5
2 * 3 = 6
2 * 4 = 8
2 * 5 = 10
3 * 4 = 12
3 * 5 = 15
4 * 5 = 20
```
合計は、$2 + 3 + 4 + 5 + 6 + 8 + 10 + 12 + 15 + 20 = 85$ になります。
````

````{dropdown} 解答例

```python
numbers = [1, 2, 3, 4, 5]
total = 0

for i in range(len(numbers)):
    for j in range(i + 1, len(numbers)):
        product = numbers[i] * numbers[j]
        total += product
        print(f"{numbers[i]} * {numbers[j]} = {product}")

print(f"合計: {total}")
```

````

````{exercise}
リスト `numbers = [2, 7, 11, 15]` と `target = 9` があります。
2つの数の和が`target`になる組み合わせのインデックスを見つけて表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [2, 7, 11, 15]
target = 9
found = False

for i in range(len(numbers)):
    for j in range(i + 1, len(numbers)):
        if numbers[i] + numbers[j] == target:
            print(f"インデックス {i} と {j}: {numbers[i]} + {numbers[j]} = {target}")
            found = True
            break
    if found:
        break

if not found:
    print("組み合わせが見つかりませんでした")
```

````

````{exercise}
リスト `numbers = [1, 2, 3, 4]` があります。
このリストから3つの要素を選ぶすべての組み合わせを生成しましょう。
````

````{dropdown} 解答例

```python
numbers = [1, 2, 3, 4]
combinations = []

for i in range(len(numbers)):
    for j in range(i + 1, len(numbers)):
        for k in range(j + 1, len(numbers)):
            combinations.append([numbers[i], numbers[j], numbers[k]])

for combo in combinations:
    print(combo)
```

````

````{exercise}
リスト `numbers = [3, 8, 1, 6, 2]` があります。
このリストの中で2番目に大きい値を見つけて表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [3, 8, 1, 6, 2]
max_val = numbers[0]
second_max = numbers[0]

for num in numbers:
    if num > max_val:
        second_max = max_val
        max_val = num
    elif num > second_max and num != max_val:
        second_max = num

print(second_max)
```
````

````{exercise}
リスト `numbers = [1, 4, 2, 8, 5, 7]` があります。
隣接する要素の差の絶対値が最小となるペアを見つけて表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [1, 4, 2, 8, 5, 7]
min_diff = abs(numbers[1] - numbers[0])
best_pair = (numbers[0], numbers[1])

for i in range(len(numbers)):
    for j in range(i + 1, len(numbers)):
        diff = abs(numbers[i] - numbers[j])
        if diff < min_diff:
            min_diff = diff
            best_pair = (numbers[i], numbers[j])

print(f"最小差のペア: {best_pair[0]}と{best_pair[1]}, 差: {min_diff}")
```
````

````{exercise}
リスト `numbers = [12, 7, 23, 8, 15, 9]` があります。
このリストの中で最大値から何番目に大きいかの順位を各要素について表示しましょう。

以下のような結果になるでしょう。
```
12は3番目に大きい
7は6番目に大きい
23は1番目に大きい
8は5番目に大きい
15は2番目に大きい
9は4番目に大きい
```
````

````{dropdown} 解答例

```python
numbers = [12, 7, 23, 8, 15, 9]
for num in numbers:
    rank = 1
    for other_num in numbers:
        if other_num > num:
            rank += 1
    print(f"{num}は{rank}番目に大きい")
```
````

````{exercise}
リスト `matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]` があります。
この行列の各行の合計と各列の合計を表示しましょう。
````

````{dropdown} 解答例

```python
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

# 各行の合計
print("各行の合計:")
for i, row in enumerate(matrix):
    row_sum = 0
    for element in row:
        row_sum += element
    print(f"行{i+1}: {row_sum}")

# 各列の合計
print("各列の合計:")
for j in range(len(matrix[0])):
    col_sum = 0
    for i in range(len(matrix)):
        col_sum += matrix[i][j]
    print(f"列{j+1}: {col_sum}")
```
````

````{exercise}
リスト `numbers = [5, 3, 8, 3, 1, 8, 5]` があります。
最も頻繁に出現する数値とその出現回数を表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [5, 3, 8, 3, 1, 8, 5]
counts = {}

for num in numbers:
    if num in counts:
        counts[num] += 1
    else:
        counts[num] = 1

max_count = 0
most_frequent = None
for num, count in counts.items():
    if count > max_count:
        max_count = count
        most_frequent = num

print(f"最頻出の数値: {most_frequent}, 出現回数: {max_count}")
```
````

````{exercise}
リスト `numbers = [5, 12, 3, 8, 15]` があります。
このリストの中で10以上の数値だけを集めて新しいリストを作り、表示しましょう。
````

````{dropdown} 解答例

```python
numbers = [5, 12, 3, 8, 15]
big_numbers = []
for num in numbers:
    if num >= 10:
        big_numbers.append(num)
print(big_numbers)
```
````

````{exercise}
リスト `prices = [100, 250, 80, 300, 150]` があります。
全ての価格に消費税10%を加えた新しいリストを作って表示しましょう。
````

````{dropdown} 解答例

```python
prices = [100, 250, 80, 300, 150]
tax_included = []
for price in prices:
    new_price = int(price * 1.1)
    tax_included.append(new_price)
print(tax_included)
```
````

````{exercise}
クラスの点数管理をしましょう。
学生のリスト `students = [["田中", 85], ["佐藤", 92], ["鈴木", 78]]` があります。
以下を実装してください。

1. 全学生の点数を表示
2. 80点以上の学生の名前を表示
3. 全体の平均点を計算して表示
````

````{dropdown} 解答例

```python
students = [["田中", 85], ["佐藤", 92], ["鈴木", 78]]

# 1. 全学生の点数を表示
print("=== 全学生の点数 ===")
for student in students:
    name = student[0]
    score = student[1]
    print(f"{name}: {score}点")

# 2. 80点以上の学生の名前を表示
print("\n=== 80点以上の学生 ===")
for student in students:
    name = student[0]
    score = student[1]
    if score >= 80:
        print(name)

# 3. 全体の平均点を計算
print("\n=== 平均点 ===")
total = 0
count = 0
for student in students:
    total += student[1]
    count += 1
average = total / count
print(f"平均点: {average:.1f}点")
```

````