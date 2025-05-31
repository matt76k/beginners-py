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
再帰関数
=======

再帰関数は初心者にとっては難しい概念ですが、
ステップバイステップで理解すれば、それほど難しくはありません。

まず、関数から関数を呼べることを確認します。

```{code-cell}
def neko():
    print('ネコ')

def koneko():
    print('コネコ')

def main():
    neko()
    neko()
    koneko()

main()
```

では、mainから`neko`だけを呼び出して、同じ出力を得るにはどうしたらよいでしょうか。

```{code-cell}
def main():
    neko() # mainからは`neko`だけを呼び出す

main()
```

解答の1つを示します。

```{code-cell}
def neko():
    print('ネコ')
    print('ネコ')
    koneko()

def main():
    neko()

main()
```

これは1つの例であり、他にも様々な方法が考えつくでしょう。
ここで学びたいのは、関数から関数を呼べるということです。

次に、1つの関数で同じような出力をする関数を作ります。

```{code-cell}
def neko_or_koneko(b):
    if b == 0:
        print('コネコ')
    else:
        print('ネコ')

neko_or_koneko(2)
neko_or_koneko(1)
neko_or_koneko(0)
```

この関数は、0を渡したら'コネコ'を、0以外は'ネコ'を表示します。
このように与える引数で関数の動作を変えることができます。

これを`for`文で書くとどうなるでしょうか？
前のコードを見て、与えてる引数の値がカウントダウンされていることに気づきましたか？

```{code-cell}
for i in range(2, -1, -1):
    neko_or_koneko(i)
```

前のプログラムがスッキリしましたね。
0が終わりを意味しているわけです。
カウントダウンという考えではなくカウントアップにしてしまうと、
どこで終わるかの数値を指定しないといけなくなるため、関数に余分な引数を与える必要が出てきてしまいます。

さらに`for`文まで無くしてみましょう。
そのためには、`neko_or_koneko`の中で`neko_or_koneko`を呼び出すようにします。
このように、関数の中で自分自身を呼び出すことを再帰呼び出しといい、そのような関数を**再帰関数**といいます。

```{code-cell}
def neko_or_koneko(b):
    if b == 0:
        print('コネコ')
    else:
        print('ネコ')
        neko_or_koneko(b - 1)

neko_or_koneko(2)
```

再帰関数の基本的な構造は、以下の通りです。

```python
def func(n):
    if n == 0: # 終了
        return val
    else: # 継続
        #ここで何かして
        func(n - 1) # 自分自身を呼び出す
```

データ構造やアルゴリズムによっては、再帰関数が最も自然な表現方法になります。

たとえば、[フィボナッチ数列](https://ja.wikipedia.org/wiki/%E3%83%95%E3%82%A3%E3%83%9C%E3%83%8A%E3%83%83%E3%83%81%E6%95%B0)です。

```{code-cell}
def fib(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fib(n - 1) + fib(n - 2)

fib_list = [fib(i) for i in range(10)]
print(fib_list)
```

では、再帰関数に慣れるために、以下の問題をやってみましょう。

## 階乗を計算する
$n! = n \times (n-1) \times (n-2) \times \cdots \times 1$
を計算する再帰関数`factorial`を作りましょう。

<details>
<summary> 回答例 </summary>

```python
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)

print(factorial(5))
```

</details>

## 数値の各桁の和を求める

整数の各桁の数字を足し合わせる再帰関数`digit_sum`を作りましょう。
例えば、$123 \rightarrow 1+2+3 = 6$ となります。

<details>
<summary> 回答例 </summary>

```python
def digit_sum(n):
    if n < 10:
        return n
    else:
        return n % 10 + digit_sum(n // 10)

print(digit_sum(123))
print(digit_sum(9876))
```

</details>

# リストの要素の合計を求める

リストの全要素の合計を再帰的に計算する関数`list_sum`を作りましょう。

<details>
<summary> 回答例 </summary>

```python
def list_sum(lst):
    if len(lst) == 0:
        return 0
    else:
        return lst[0] + list_sum(lst[1:])

print(list_sum([1, 2, 3, 4, 5]))
```

</details>

## 文字列を逆順にする

文字列を逆順にして返す再帰関数`reverse_string`を作りましょう。

<details>
<summary> 回答例 </summary>

```python
def reverse_string(s):
    if len(s) <= 1:
        return s
    else:
        return s[-1] + reverse_string(s[:-1])

print(reverse_string("Python"))
```

</details>

## べき乗を計算する
`x` の `n` 乗を再帰的に計算する関数`power`を作りましょう。

<details>
<summary> 回答例 </summary>

```python
def power(x, n):
    if n == 0:
        return 1
    else:
        return x * power(x, n - 1)

print(power(2, 5))
print(power(3, 4))
```

</details>

## 最大公約数を求める
ユークリッドの互除法を使って、2つの数の最大公約数を求める再帰関数`gcd`を作りましょう。

<details>
<summary> 回答例 </summary>

```python
def gcd(a, b):
    if b == 0:
        return a
    else:
        return gcd(b, a % b)

print(gcd(48, 18))
print(gcd(100, 25))
```

</details>

## 回文かどうかを判定する

文字列が回文（前から読んでも後ろから読んでも同じ）かどうかを判定する再帰関数`is_palindrome`を作りましょう。

<details>
<summary> 回答例 </summary>

```python
def is_palindrome(s):
    if len(s) <= 1:
        return True
    elif s[0] != s[-1]:
        return False
    else:
        return is_palindrome(s[1:-1])

print(is_palindrome("hello"))
print(is_palindrome("きんにくぼでぃでぼくにんき"))
```

</details>

## 2進数変換を行う

10進数を2進数の文字列に変換する再帰関数`to_binary`を作成してください。

<details>
<summary> 回答例 </summary>

```python
def to_binary(n):
    if n == 0:
        return "0"
    elif n == 1:
        return "1"
    else:
        return to_binary(n // 2) + str(n % 2)
print(to_binary(10))  # "1010"が表示される
print(to_binary(7))   # "111"が表示される
```

</details>
