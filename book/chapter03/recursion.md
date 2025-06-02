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

```python
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

順次で考えるとプログラムは上から下に実行されます。
`def`のあとに書いたプログラムは、定義なのでなにも実行されず、その関数が呼ばれたときに実行されます。

制御の流れをしっかり意識しましょう。
プログラムは`def neko()`、`def koneko()`、`def main()`の順番に流れます。
関数定義なので、定義はしますが、何か表示されるわけではありません。

最後の行で`main`関数が実行されると、`main`関数の中身が実行されます。
`main`関数の中身は、`neko`を2回呼び出して、`koneko`を1回呼び出しています。

`neko`の最初の呼び出しで「ネコ」を表示します。
表示し終わったら、関数は呼び出したところに戻ってくるので、
2番目の`neko`を呼び出します。
これも同様に「ネコ」を表示します。
また、呼び出したところに戻ってきて、`koneko`を呼び出します。

`main`の中身の実行が終わると、`main`関数の呼び出したところ、つまりプログラムの最後に戻ってきて、プログラムは終了します。

では、mainから`neko`だけを呼び出して、同じ出力を得るにはどうしたらよいでしょうか。

```python
def main():
    neko() # mainからは`neko`だけを呼び出す

main()
```

````{dropdown} 解答例

```python
def neko():
    print('ネコ')
    print('ネコ')
    koneko()

def main():
    neko()

main()
```

````

解答例は1つの例であり、他にも様々な方法が考えつくでしょう。
ここで学びたいのは、関数から関数を呼べるということです。

次に、1つの関数で同じような出力をする関数を作りましょう。

```python
def neko_or_koneko(b):
    if b == 0:
        print('コネコ')
    else:
        print('ネコ')

neko_or_koneko(2)
neko_or_koneko(1)
neko_or_koneko(0)
```

この関数は、0を渡したら「コネコ」を、0以外は「ネコ」を表示します。
このように与える引数で関数の動作を変えることができます。

これを`for`文で書くとどうなるでしょうか？
前のコードを見て、与えてる引数の値がカウントダウンされていることに気づきましたか？

```python
for i in range(2, -1, -1):
    neko_or_koneko(i)
```

前のプログラムがスッキリしましたね。
0が終わりを意味しています。
カウントダウンという考えではなくカウントアップにしてしまうと、
どこで終わるかの数値を指定しないといけなくなるため、関数に余分な引数を与える必要が出てきます。

さらに`for`文まで無くしてみましょう。
そのためには、`neko_or_koneko`の中で`neko_or_koneko`を呼び出すようにします。
このように、関数の中で自分自身を呼び出すことを再帰呼び出しといい、そのような関数を**再帰関数**といいます。

```python
def neko_or_koneko(b):
    if b == 0:
        print('コネコ')
    else:
        print('ネコ')
        neko_or_koneko(b - 1)

neko_or_koneko(2)
```

制御の流れを意識しましょう。紙に書いて、どのように実行されるかを確認すると良いでしょう。

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

たとえば、フィボナッチ数列は以下のような再帰的な定義になっています。

$$
F_0 = 0 \\
F_1 = 1 \\
F_n = F_{n-1} + F_{n-2}
$$

まずは`for`文で書いてみましょう。

```python
fib_list = [0, 1]
for i in range(2, 10):
    fib_list.append(fib_list[i - 1] + fib_list[i - 2])
print(fib_list)
```

これを再帰関数で書くと以下のようになります。

```python
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

再帰関数で書いた方が元の定義に近いですね。
このように、再帰関数は再帰的な定義の処理をそのまま書けるという利点があります。

では、再帰関数に慣れるために、以下の問題をやってみましょう。

## 階乗を計算する
$n! = n \times (n-1) \times (n-2) \times \cdots \times 1$
を計算する再帰関数`factorial`を作りましょう。

````{dropdown} 解答例

```python
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)

print(factorial(5))
```

````

## 数値の各桁の和を求める

整数の各桁の数字を足し合わせる再帰関数`digit_sum`を作りましょう。
例えば、$123 \rightarrow 1+2+3 = 6$ となります。

````{dropdown} 解答例

```python
def digit_sum(n):
    if n < 10:
        return n
    else:
        return n % 10 + digit_sum(n // 10)

print(digit_sum(123))
print(digit_sum(9876))
```

````

## リストの要素の合計を求める

リストの全要素の合計を再帰的に計算する関数`list_sum`を作りましょう。

````{dropdown} 解答例

```python
def list_sum(lst):
    if len(lst) == 0:
        return 0
    else:
        return lst[0] + list_sum(lst[1:])

print(list_sum([1, 2, 3, 4, 5]))
```

````

## 文字列を逆順にする

文字列を逆順にして返す再帰関数`reverse_string`を作りましょう。

````{dropdown} 解答例

```python
def reverse_string(s):
    if len(s) <= 1:
        return s
    else:
        return s[-1] + reverse_string(s[:-1])

print(reverse_string("Python"))
```

````

## べき乗を計算する
`x` の `n` 乗を再帰的に計算する関数`power`を作りましょう。

````{dropdown} 解答例

```python
def power(x, n):
    if n == 0:
        return 1
    else:
        return x * power(x, n - 1)

print(power(2, 5))
print(power(3, 4))
```

````

## 最大公約数を求める
ユークリッドの互除法を使って、2つの数の最大公約数を求める再帰関数`gcd`を作りましょう。

````{dropdown} 解答例

```python
def gcd(a, b):
    if b == 0:
        return a
    else:
        return gcd(b, a % b)

print(gcd(48, 18))
print(gcd(100, 25))
```

````

## 回文かどうかを判定する

文字列が回文（前から読んでも後ろから読んでも同じ）かどうかを判定する再帰関数`is_palindrome`を作りましょう。

````{dropdown} 解答例

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

````

## 2進数変換を行う

10進数を2進数の文字列に変換する再帰関数`to_binary`を作成してください。

````{dropdown} 解答例

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

````
