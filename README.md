# Pythonを極めて無双した件

プログラミング初心者向けのPython入門書です。

## 概要

本書は、プログラミングをはじめて学ぶ人向けに書かれた入門書です。Pythonを使って、プログラミングの基礎（逐次・分岐・反復）からアルゴリズムとデータ構造まで学びます。

## 内容

- **第1章: プログラミングの基本**
  - データ型（文字列、数値、リスト）
  - 変数
  - 制御構造（逐次・分岐・反復）
  - 変数スコープ

- **第2章: 演習問題**
  - 100の鍛：プログラムを書く能力を鍛える問題
  - 42の錬：プログラムを読む能力を鍛える問題
  - 理解度チェック50：理解度を確認する3択問題

- **第3章: 関数**
  - 関数の作り方と使い方
  - 再帰関数

## 開発環境

本プロジェクトは[uv](https://github.com/astral-sh/uv)で管理されています。

### 必要なもの

- Python 3.9以上
- uv

### セットアップ

```bash
uv sync
```

### ローカルでのビルド

HTML形式でビルド：

```bash
uv run jupyter-book build book
```

ビルドされたHTMLは `book/_build/html/` に生成されます。

### EPUB形式のビルド

```bash
uv run sphinx-build book book/_build/epub -b epub
```

### Kindle用カバー画像の生成

```bash
magick book/cover.png -resize 1600x2560 cover_kindle.jpg
```

## GitHub Pages

このプロジェクトは、`main`ブランチの`book/**`に変更があると、自動的にGitHub Pagesにデプロイされます。

## ライセンス

Copyright 2025, 鳳凰院 龍聖