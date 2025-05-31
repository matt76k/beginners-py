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
関数
====

今までにすでに**関数**を使っています。
`print`は関数の一つです。

関数とは、特定の処理をまとめて名前を付けたもので、
必要なときに呼び出して使えます。
料理のレシピのようなもので、材料を渡すと決まった手順で処理して結果を返してくれます。

`print("こんにちは")`と書いたとき、
`print`が関数の名前で、括弧の中の`"こんにちは"`が**引数**と呼ばれるものです。
引数は、関数に「こんな材料で処理してね」と渡す値のことです。
`print`関数の場合、引数として渡された文字列や数値を画面に表示してくれます。

関数には、処理した結果を返してくれるものもあります。
この結果のことを**返り値**といいます。
例えば、`len("python")`という関数は、文字列の長さを数えて`6`という数値を返してくれます。
この`6`が返り値です。

```python
length = len("python")
print(length)
```

一方で`print`関数は、画面に文字を表示することが目的なので、特に意味のある返り値は返しません。

関数を使うと、複雑な処理を簡単な名前で呼び出せるようになり、同じ処理を何度も書く必要がなくなります。
プログラミングがとても効率的になる、とても便利な機能になります。

さて、関数は使うだけではなく、自分で作ることもできます。
2つの値を足した結果を返す関数`add`を作ってみましょう。

```python
def add(a, b):
    c = a + b
    return c

print(add(1, 2))
```

`def`は関数を定義するためのキーワードです。
`add`は関数の名前で、括弧の中の`a`と`b`は引数になります。
`:`は関数の定義の始まりを示すためのものです。
そのあと、`if`文のところでも出てきたように、インデントをつけて関数の処理内容を書きます。

この関数の処理は、引数`a`と`b`を足した結果を変数`c`に代入して、その`c`を返り値として返しています。

`return`は関数の返り値を指定するためのキーワードです。
ここでは`return c`と書くことで、変数`c`の値を関数を呼び出した元に返しています。

最後の行で、自分で定義した関数`add`を呼び出しています。
`print(add(1, 2))`のように`print`と`add`が続いていますが、内側の関数から順番に処理されます。
つまり、まず`add(1, 2)`が実行されて`3`という結果が返され、
その返り値`3`が`print`の引数として渡されて画面に表示されるという流れです。

以下の演習問題で関数の作成を練習してみましょう。

## 引き算をする
2つの数値を受け取って、1つ目の数値から2つ目の数値を引いた結果を返す関数`subtract`を作りましょう。

<details>
<summary> 回答例 </summary>

```python
def subtract(a, b):
    result = a - b
    return result

print(subtract(10, 3))
```

</details>

## 挨拶をする
名前を受け取って「こんにちは、〇〇さん！」という挨拶文を返す関数`greet`を作りましょう。

<details>
<summary> 回答例 </summary>

```python
def greet(name):
    message = "こんにちは、" + name + "さん！"
    return message

print(greet("Python"))
```

</details>

## 面積を計算する
長方形の縦の長さと横の長さを受け取って、面積を計算して返す関数`area`を作りましょう。

<details>
<summary> 回答例 </summary>

```python
def area(length, width):
    result = length * width
    return result

print(area(5, 3))
```

</details>

## 最大値を求める
数値のリストを受け取って、リストの中で最も大きい数値を返す関数`max_value`を作りましょう。

<details>
<summary> 回答例 </summary>

```python
def max_value(numbers):
    max_num = numbers[0]
    for num in numbers:
        if num > max_num:
            max_num = num
    return max_num

print(max_value([8, 5, 10, 3]))
```

</details>

## 偶数か奇数かを判定する
数値を受け取って、その数が偶数なら「True」、奇数なら「False」を返す関数`is_even`を作りましょう。

<details>
<summary> 回答例 </summary>

```python
def is_even(number):
    return number % 2 == 0

print(even_or_odd(4))
print(even_or_odd(7))
```

</details>
